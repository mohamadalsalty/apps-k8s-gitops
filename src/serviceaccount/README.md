# Arquivo main.yaml

Este arquivo contém as definições YAML para criar um ServiceAccount, um ClusterRole, um ClusterRoleBinding e um Secret no Kubernetes.

## ServiceAccount

O ServiceAccount `sa-k8s-api` é criado para ser usado por aplicativos que precisam interagir com a API do Kubernetes.

## ClusterRole

O ClusterRole `list-all-resources-clusterrole` define as permissões para listar vários recursos no cluster, incluindo pods, serviços, deployments, entre outros.

## ClusterRoleBinding

O ClusterRoleBinding `bind-sa-k8s-api-clusterrole` associa o ServiceAccount `sa-k8s-api` ao ClusterRole `list-all-resources-clusterrole`, concedendo as permissões definidas no ClusterRole ao ServiceAccount.

## Secret

O Secret `sa-k8s-api-token` é criado para armazenar o token de autenticação do ServiceAccount `sa-k8s-api`. Esse token pode ser usado para autenticar o ServiceAccount ao acessar a API do Kubernetes.

## Aplicando e Removendo as Configurações

Para aplicar as configurações definidas no arquivo `main.yaml`, execute o seguinte comando:

```sh
make apply
