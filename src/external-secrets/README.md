# Deploy External secrets


## Configuração

Antes de começar, você precisa ter o 'kubectl' e o 'helm' instalados e configurados para o seu cluster Kubernetes. Além disso, certifique-se de ter as permissões necessárias para criar namespaces e instalar recursos no cluster.

## Instalação

Para instalar o projeto, siga estas etapas:

1. Clone o repositório

2. Crie e instale o External Secrets:
   ```sh
   make create-install
   ```

## Uso

Após a instalação, você pode usar o projeto da seguinte maneira:

1. Faça algo incrível:
   ```sh
   make install-all
   ```

2. Aproveite os resultados!

## Desinstalação

Se você precisar desinstalar o projeto, você pode fazê-lo com o seguinte comando:
   ```sh
   make uninstall-external-secrets
   ```