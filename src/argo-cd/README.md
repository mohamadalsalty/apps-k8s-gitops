# Guia de Instalação do ArgoCD

Este é um guia simples para instalar o ArgoCD no Kubernetes usando o arquivo 'install.yaml'.

## Pré-requisitos

- 'kubectl' configurado para acessar seu cluster Kubernetes.

## Instalação

Para instalar o ArgoCD, siga os seguintes passos:

1. Clone este repositório

2. Execute o seguinte comando para instalar o ArgoCD:

   '''sh
   make install-argocd
   '''

Isso irá criar um namespace 'argocd' e instalar o ArgoCD usando o arquivo 'install.yaml'.

Para mais informações, consulte a [documentação oficial do ArgoCD](https://argoproj.github.io/argo-cd/).
