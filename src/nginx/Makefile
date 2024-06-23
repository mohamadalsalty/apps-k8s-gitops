# Makefile to deploy NGINX Ingress controller

NAMESPACE=ingress-nginx
INGRESS_YAML=deploy.yaml

.PHONY: all create-namespace deploy-ingress verify-ingress clean help

all: create-namespace deploy-ingress verify-ingress

create-namespace:
	kubectl create namespace $(NAMESPACE) || true

deploy-ingress:
	kubectl apply -f $(INGRESS_YAML)

verify-ingress:
	@echo "Waiting for NGINX Ingress controller pods to be ready..."
	kubectl wait --namespace $(NAMESPACE) \
	  --for=condition=ready pod \
	  --selector=app.kubernetes.io/component=controller \
	  --timeout=120s

clean:
	@echo "Cleaning up..."
	kubectl delete namespace $(NAMESPACE)

help:
	@echo "Makefile to deploy NGINX Ingress controller"
	@echo ""
	@echo "Usage:"
	@echo "  make all                - Deploy NGINX Ingress controller"
	@echo "  make create-namespace   - Create namespace for NGINX Ingress controller"
	@echo "  make deploy-ingress     - Deploy NGINX Ingress controller"
	@echo "  make verify-ingress     - Verify NGINX Ingress controller pods are ready"
	@echo "  make clean              - Clean up resources"
	@echo "  make help               - Display this help message"
