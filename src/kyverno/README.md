# Instalação do Kyverno

Este é um guia simples para instalar o Kyverno usando o Helm.

## Adicionar o repositório do Helm

Antes de instalar o Kyverno, é necessário adicionar o repositório do Helm.

```sh
helm repo add kyverno https://kyverno.github.io/kyverno/
helm repo update
```

## Instalar o Kyverno

Execute o seguinte comando para instalar o Kyverno:

```sh
kubectl create namespace kyverno
helm install kyverno kyverno/kyverno --namespace kyverno
```

Isso instalará o Kyverno na namespace 'kyverno' do seu cluster Kubernetes.

## Verificar a instalação

Após a instalação, verifique se o Kyverno foi instalado corretamente executando:

```sh
kubectl get pods -n kyverno
```

Você deve ver os pods do Kyverno em estado 'Running'.

## Comandos Makefile

O Makefile fornecido neste projeto possui o seguinte comando:

- `make install-kyverno`: Adiciona o repositório do Kyverno Helm, atualiza os repositórios, cria o namespace `kyverno` se não existir e instala o Kyverno usando o Helm.
