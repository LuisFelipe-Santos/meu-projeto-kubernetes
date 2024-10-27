# Meu Projeto Kubernetes

![Kubernetes Logo](https://kubernetes.io/images/header/logo.svg) <!-- Exemplo de imagem, você pode usar outras -->

## Descrição

Este projeto demonstra como implantar uma aplicação usando Kubernetes com um serviço de NodePort. A aplicação foi configurada para ser acessível a partir de uma máquina local, utilizando Minikube.

## Tecnologias Utilizadas

- [Kubernetes](https://kubernetes.io) - Sistema de orquestração de contêineres
- [Minikube](https://minikube.sigs.k8s.io/docs/start/) - Ferramenta para rodar Kubernetes localmente
- [Docker](https://www.docker.com/) - Plataforma para desenvolvimento e execução de aplicativos em contêineres
- [Git](https://git-scm.com/) - Sistema de controle de versão

## Estrutura do Projeto

```plaintext
meu-projeto-k8s/
├── k8s/
│   ├── deployment.yaml
│   ├── service.yaml
├── README.md

```
## Pré-requisitos
Antes de começar, você precisará ter instalado em sua máquina:

- Minikube
- kubectl
- Docker

## Como Executar o Projeto

1. **Inicie o Minikube**:

   ```bash
   minikube start
2. Aplique os arquivos de configuração:

  ```bash
kubectl apply -f k8s/deployment.yaml
kubectl apply -f k8s/service.yaml
```
3.Verifique os pods e serviços:
  
  ```bash
  kubectl get pods
  kubectl get services
```
4. Acesse a aplicação:

Use o comando curl ou seu navegador:

```bash
curl http://<minikube-ip>:<nodeport>
```
Substitua <minikube-ip> pelo IP do Minikube e <nodeport> pela porta correspondente.

## Testando Localmente
Você pode testar a aplicação diretamente no terminal do Minikube usando o seguinte comando:

```bash
minikube ssh
curl http://localhost:<nodeport>
```


### Notas

- O uso de listas numeradas e formatação de código torna a seção mais legível.
- Certifique-se de substituir `<minikube-ip>` e `<nodeport>` com os valores corretos ao executar os comandos. 
