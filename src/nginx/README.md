# NGINX Ingress Controller Makefile

Este Makefile automatiza a implantação do controlador NGINX Ingress em um cluster Kubernetes.

## Conteúdo do Makefile

Este Makefile inclui as seguintes metas:

- `all`: Cria o namespace `ingress-nginx`, implanta o controlador NGINX Ingress e verifica se os pods estão prontos.
- `create-namespace`: Cria o namespace `ingress-nginx` (ignora o erro se o namespace já existir).
- `deploy-ingress`: Implanta o controlador NGINX Ingress.
- `verify-ingress`: Verifica se os pods do controlador NGINX Ingress estão prontos.
- `clean`: Remove o namespace `ingress-nginx` e todos os recursos nele contidos.
- `help`: Exibe uma mensagem de ajuda explicando as metas disponíveis.

## Como Usar

1. Salve o conteúdo do Makefile em um arquivo chamado `Makefile`.

2. Execute o seguinte comando para realizar todo o processo:

   ```sh
   make all
   ```

   Isso irá:
   - Criar o namespace para o controlador NGINX Ingress (ignorando qualquer erro se o namespace já existir).
   - Implantar o controlador NGINX Ingress.
   - Verificar se os pods do controlador NGINX Ingress estão em execução.

## Limpeza

Para limpar todos os recursos criados, execute:

   ```sh
   make clean
   ```

## Notas

- Certifique-se de que o contexto do seu cluster Kubernetes esteja configurado corretamente antes de executar o Makefile.
- Este Makefile fornece uma maneira simples de instalar o controlador NGINX Ingress no seu cluster Kubernetes.
