# 📦 microservices-springboot-kafka

Arquitetura de microservices desenvolvida com **Spring Boot** e **Apache Kafka**, aplicando princípios de **Event-Driven Architecture**.

O sistema contempla os domínios de:

- Produtos  
- Clientes  
- Pedidos  
- Faturamento  
- Logística  

Utilizando Docker, bancos de dados independentes, Webhooks, MinIO e Jasper Reports em um cenário próximo ao mundo real.

---

# 🏗 Arquitetura

Abaixo está o diagrama geral da arquitetura do sistema:

![Arquitetura Microservices](docs/desenho+de+solucao.jpg)

> Certifique-se de salvar sua imagem como `desenho+de+solucao.jpg` dentro da pasta `docs`.

---

# 🚀 Tecnologias Utilizadas

- Java 17+
- Spring Boot
- Spring Data JPA
- Apache Kafka
- Docker & Docker Compose
- PostgreSQL
- MinIO (Cloud Storage compatível com S3)
- Jasper Reports
- Webhooks (integrações externas)
- REST APIs

---

# 🧠 Conceitos Aplicados

- Microservices Architecture  
- Event-Driven Architecture  
- Comunicação assíncrona com Kafka  
- Banco de dados por serviço  
- Isolamento de domínio  
- Publicação e consumo de eventos  
- Escalabilidade horizontal  
- Integração via Webhooks  

---

# 🔄 Fluxo Geral do Sistema

1. Usuário cria pedido via Web ou Mobile  
2. Serviço de Pedidos publica evento de pagamento  
3. Faturamento consome evento e gera fatura  
4. Logística recebe notificação e inicia rastreamento  
5. Eventos são propagados via Kafka entre os serviços  

---

# 📂 Estrutura do Projeto
microservices-springboot-kafka/
│
├── product-service
├── customer-service
├── order-service
├── billing-service
├── logistics-service
├── docker-compose.yml
└── docs/

Cada microservice possui:
- Banco de dados próprio  
- Configuração independente  
- Comunicação via Kafka  

---

# 🐳 Executando o Projeto

## 1️⃣ Subir infraestrutura

```bash
docker-compose up -d
