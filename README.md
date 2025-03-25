# Cloudmart - Multicloud e Inteligência Artificial

## Visão Geral
Cloudmart é um projeto de e-commerce fictício desenvolvido durante o Bootcamp de Multicloud e IA da empresa The Cloud Bootcamp. O objetivo principal foi integrar tecnologias de nuvem de diferentes provedores (AWS, Google Cloud e Microsoft Azure) e soluções de inteligência artificial para construir uma arquitetura moderna e escalável.

O sistema foi implementado com as seguintes funcionalidades:
- Arquitetura Multicloud utilizando AWS, Google Cloud e Azure.
- Sistema de análise em tempo real com BigQuery do Google Cloud.
- Integração com OpenAI API para gestão de pedidos e suporte via chat.
- Suporte ao cliente com Claude 3 Sonnet, configurado via Amazon Bedrock.
- Pipeline de CI/CD para automação de deploy utilizando AWS CodePipeline e Terraform.

![Arquitetura Multicloud](https://github.com/user-attachments/assets/c20474d7-76dd-490e-91c5-3ce66381b49a)
*Figura 1: Arquitetura Multicloud do projeto Cloudmart.*

---

## Funcionalidades e Tecnologias Utilizadas

### 1. Frontend e Backend no Amazon EKS
A aplicação foi implantada em um cluster Kubernetes gerenciado pela AWS (Amazon EKS). A estrutura foi dividida em pods para o frontend e backend, permitindo alta disponibilidade e escalabilidade.

### 2. Análise em Tempo Real com BigQuery
Foi utilizado o Google BigQuery para analisar dados transacionais de pedidos em tempo real. O pipeline de dados foi configurado para enviar informações de pedidos diretamente para o BigQuery, onde eram processadas para obter insights rápidos e precisos.

![BigQuerry](https://github.com/user-attachments/assets/8cfb9a7f-320d-411d-82d2-25955667ec76)
*Figura 2: Painel de análise em tempo real no BigQuery.*

---

### 3. Integração com a API da OpenAI para Cancelamento de Pedidos
Implementamos uma funcionalidade de suporte ao cliente utilizando a API da OpenAI. Clientes podem interagir via chat para solicitar cancelamentos de pedidos, e a API realiza a chamada para o backend, que executa o cancelamento.

![Orders](https://github.com/user-attachments/assets/ab062212-4179-446b-b9df-a0954b626fc6)
![Cancelando pedido](https://github.com/user-attachments/assets/bbed7711-f6ad-4686-a94d-0d3d6352781e)
![Cancelando pedido 2](https://github.com/user-attachments/assets/ef7a0ce5-6f57-4be3-95ab-17f018cf970d)


*Figuras 3, 4 e 5: Exemplo de cancelamento de pedido no chat utilizando OpenAI API.*

---

### 4. Suporte ao Cliente com Claude 3 Sonnet via Amazon Bedrock
Além da OpenAI API, também foi configurado o modelo Claude 3 Sonnet, utilizando o Amazon Bedrock para fornecer suporte adicional ao cliente. Essa integração foi feita para explorar diferentes soluções de IA disponíveis no mercado.

![Teste Bedrock](https://github.com/user-attachments/assets/f73774ff-d2ef-493f-a654-2a2762008235)
*Figura 6: Chat de suporte ao cliente com Claude 3 Sonnet configurado via Amazon Bedrock.*

---

### 5. Pipeline de CI/CD Automatizado
O deploy da aplicação foi automatizado com o uso de AWS CodePipeline e AWS CodeBuild, orquestrados pelo Terraform. Esse pipeline permite que alterações no código sejam rapidamente integradas e implantadas no ambiente de produção.

![Pipeline CI-CD](https://github.com/user-attachments/assets/915768d1-0c65-4b24-9ff6-8efe68d349d0)
*Figura 7: Execução do pipeline de CI/CD no AWS CodePipeline.*

---

## Tecnologias Utilizadas
As seguintes tecnologias foram utilizadas no desenvolvimento do projeto:

<a href="https://skillicons.dev">
<img src="https://skillicons.dev/icons?i=linux,terraform,docker,kubernetes,aws,dynamodb,git,gcp,azure"/>
