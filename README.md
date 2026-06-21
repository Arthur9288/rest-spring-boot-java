# RESTful API with Spring Boot and Java

[![Continuous Integration and Delivery with Github Actions](https://github.com/Arthur9288/rest-spring-boot-java/actions/workflows/continuous-deployment.yml/badge.svg)](https://github.com/Arthur9288/rest-spring-boot-java/actions/workflows/continuous-deployment.yml)

Uma API RESTful desenvolvida em Java e Spring Boot, com foco em boas práticas de engenharia de software, integração contínua (CI/CD) e conteinerização. O objetivo deste projeto é demonstrar uma arquitetura escalável e de fácil deploy, unindo o desenvolvimento backend com práticas modernas de infraestrutura.

## 🛠 Tecnologias Utilizadas

* **Linguagem & Framework:** Java 17+, Spring Boot
* **Infraestrutura & DevOps:** Docker, Docker Compose
* **Automação:** GitHub Actions (CI/CD Pipeline)
* **Documentação:** Swagger / OpenAPI

## 🚀 Como executar a aplicação

A aplicação foi conteinerizada para garantir uma filosofia *Plug and Play*. Para rodar este projeto localmente, você precisa ter apenas o [Docker](https://www.docker.com/) e o [Docker Compose](https://docs.docker.com/compose/) instalados na sua máquina. Não é necessário instalar o Java ou configurar um banco de dados localmente.

docker run -p 8080:8080 -d jesudocker496519/rest-with-spring-boot-erudio:latest
