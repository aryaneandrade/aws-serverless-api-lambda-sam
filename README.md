# 📡 Serverless API com AWS Lambda, SAM, API Gateway e RDS

Projeto prático desenvolvido como parte da Mentoria Desafio Labs - Formação AWS, com foco em arquitetura **serverless**, automação de infraestrutura e integração com serviços gerenciados da AWS.

---

## 📌 Objetivo

Migrar uma aplicação Node.js para um ambiente **100% serverless** utilizando:

- AWS Lambda como camada de execução
- Amazon API Gateway como camada de exposição HTTP
- AWS SAM como framework de infraestrutura como código (IaC)
- Amazon RDS (PostgreSQL) como banco de dados relacional

O projeto contempla **execução local, testes, validação, build, deploy automatizado**, e **integração de backend com banco de dados em ambiente gerenciado**.

---

## 🧰 Tecnologias e Serviços Utilizados

| Tecnologia / Serviço       | Função no Projeto                          |
|----------------------------|--------------------------------------------|
| **AWS Lambda**             | Execução da lógica da API (function-as-a-service) |
| **Amazon API Gateway**     | Exposição de endpoints HTTP (REST API)     |
| **AWS SAM CLI**            | Build, validação e deploy via IaC          |
| **Amazon RDS (PostgreSQL)**| Armazenamento persistente dos dados        |
| **Docker**                 | Execução local da Lambda com SAM           |
| **Node.js**                | Runtime da aplicação                       |
| **CloudFormation**         | Provisionamento automatizado da infraestrutura |

---

## 🧪 Etapas Realizadas

1. Criação inicial da função Lambda no console AWS
2. Instalação e configuração do ambiente SAM local
3. Desenvolvimento e teste local da função utilizando Docker + SAM
4. Build, validação e deploy com SAM CLI (`sam deploy`)
5. Criação e configuração da API REST no API Gateway
6. Integração da Lambda com o banco de dados RDS
7. Testes de conectividade e resposta via endpoint público

---

## 🖼️ Evidências Técnicas

> ⚠️ Substitua os caminhos `./screenshots/...` pelas imagens reais após upload no repositório.

### ✅ Função Lambda Criada via Console AWS  
*Demonstra a criação inicial com runtime configurado.*  
![lambda-console](./screenshots/lambda-console.png)

---

### ✅ Execução Local da Função com SAM CLI  
*Função testada localmente com Docker via `sam local invoke`.*  
![sam-local-invoke](./screenshots/sam-local-invoke.png)

---

### ✅ Deploy Automatizado com SAM CLI  
*Deploy da aplicação para a AWS utilizando `sam deploy --guided`.*  
![sam-deploy](./screenshots/sam-deploy.png)

---

### ✅ Integração da API Gateway com a Lambda  
*Configuração do método HTTP vinculado à função Lambda.*  
![api-gateway](./screenshots/api-gateway.png)

---

### ✅ Teste Funcional do Endpoint REST  
*Requisição realizada ao endpoint da API Gateway com resposta da função.*  
![api-test](./screenshots/api-test.png)

---

### ✅ Conexão da Lambda com Amazon RDS  
*Trecho da função demonstrando integração com banco relacional.*  
![lambda-rds](./screenshots/lambda-rds.png)

---

## 📂 Comandos Essenciais

```bash
# Compilar a aplicação
sam build

# Validar a estrutura do template SAM
sam validate

# Executar a função localmente com Docker
sam local invoke HelloWorldFunction --event events/event.json

# Realizar o deploy com assistente
sam deploy --guided


---

## 🛡️ Boas Práticas Aplicadas

- Deploy automatizado com SAM (infraestrutura como código)
- Conexão com RDS via variáveis de ambiente seguras (não expostas)
- Separação de ambientes (desenvolvimento/teste)
- Testes locais antes do deploy em nuvem
- Uso de serviços gerenciados, reduzindo overhead operacional

---

## 🧠 Aprendizados Técnicos

- Criação e execução de funções AWS Lambda via console e SAM
- Utilização completa do ciclo de vida do SAM (build, validate, invoke, deploy)
- Configuração de API Gateway com métodos e integração backend
- Gerenciamento de banco relacional com Amazon RDS
- Prática com Docker e execução local de ambiente AWS

---

## 👤 Autora

**Aryane Andrade**  
[LinkedIn](https://www.linkedin.com/in/aryane-andrade) 
