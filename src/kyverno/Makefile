NAMESPACE = kyverno

install-kyverno:
	helm repo add kyverno https://kyverno.github.io/kyverno/
	helm repo update
	kubectl get namespace $(NAMESPACE) || kubectl create namespace $(NAMESPACE)
	helm install kyverno kyverno/kyverno --namespace $(NAMESPACE)


.PHONY: install-kyverno	