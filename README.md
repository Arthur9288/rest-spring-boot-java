# RESTful API - Spring Boot & Java

[![Continuous Integration and Delivery with Github Actions](https://github.com/Arthur9288/rest-spring-boot-java/actions/workflows/continuous-deployment.yml/badge.svg)](https://github.com/Arthur9288/rest-spring-boot-java/actions/workflows/continuous-deployment.yml)

API RESTful desenvolvida em Java e Spring Boot. O projeto demonstra boas práticas de engenharia de software, integração contínua (CI/CD) e conteinerização, unindo o desenvolvimento backend a práticas modernas de infraestrutura.

## 🛠 Tecnologias

* **Backend:** Java 17+, Spring Boot
* **Infra & DevOps:** Docker, GitHub Actions (CI/CD)
* **Documentação:** Swagger / OpenAPI

## 🚀 Como executar (Plug and Play)

A imagem Docker já sobe a aplicação e o banco de dados juntos. Para rodar, basta ter o [Docker](https://www.docker.com/) instalado no seu ambiente. Não é necessário configurar o Java ou o banco localmente.

Execute um único comando no terminal:

```bash
docker run -p 8080:8080 -d jesudocker496519/rest-with-spring-boot-erudio:latest
```

## 🌐 Acesso

Após o container iniciar, clique nos links abaixo para acessar:
* **API Root:** [http://localhost:8080](http://localhost:8080)
* **Swagger (Documentação):** [http://localhost:8080/swagger-ui.html](http://localhost:8080/swagger-ui.html)
