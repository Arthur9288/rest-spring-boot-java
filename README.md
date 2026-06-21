# RESTful API - Spring Boot & Java

[![Continuous Integration and Delivery with Github Actions](https://github.com/Arthur9288/rest-spring-boot-java/actions/workflows/continuous-deployment.yml/badge.svg)](https://github.com/Arthur9288/rest-spring-boot-java/actions/workflows/continuous-deployment.yml)

API RESTful desenvolvida em Java e Spring Boot. O projeto demonstra boas práticas de engenharia de software, integração contínua (CI/CD) e conteinerização, unindo o desenvolvimento backend a práticas modernas de infraestrutura.

## 🛠 Tecnologias

* **Backend:** Java 17+, Spring Boot
* **Infra & DevOps:** Docker, GitHub Actions (CI/CD)
* **Documentação:** Swagger / OpenAPI

## 🚀 Como executar (Padrão de Mercado)

Para rodar a aplicação e o banco de dados juntos de forma totalmente automatizada, você só precisa do Docker instalado.

```bash
# 1. Clone o repositório e entre na pasta
git clone [https://github.com/Arthur9288/rest-spring-boot-java.git](https://github.com/Arthur9288/rest-spring-boot-java.git)
cd rest-spring-boot-java```

# 2. Suba a API e o Banco de Dados com um único comando
docker-compose up -d

## 🌐 Acesso

Após o container iniciar, clique nos links abaixo para acessar:
* **API Root:** [http://localhost:8080](http://localhost:8080)
* **Swagger (Documentação):** [http://localhost:8080/swagger-ui.html](http://localhost:8080/swagger-ui.html)
