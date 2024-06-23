# Namespace where External Secrets will be installed
NAMESPACE := ext-secrets

# Helm repository URL for External Secrets
HELM_REPO_URL := https://charts.external-secrets.io

# Name of the Helm repository
HELM_REPO_NAME := external-secrets

# Create the Kubernetes namespace, add the Helm repository, and install External Secrets
install-all: create-namespace add-helm-repo install-external-secrets

# Create the Kubernetes namespace, add the Helm repository, and install External Secrets
create-install: create-namespace add-helm-repo install-external-secrets

# Create the Kubernetes namespace
create-namespace:
	kubectl create namespace $(NAMESPACE)

# Add the Helm repository for External Secrets
add-helm-repo:
	helm repo add $(HELM_REPO_NAME) $(HELM_REPO_URL)

# Install the External Secrets Helm chart
install-external-secrets:
	helm install external-secrets $(HELM_REPO_NAME)/external-secrets --namespace $(NAMESPACE)

# Remove the External Secrets Helm chart
uninstall-external-secrets:
	helm uninstall external-secrets -n $(NAMESPACE)

# Update the Helm repositories
update-helm-repos:
	helm repo update

# List Helm repositories
list-helm-repos:
	helm repo list
