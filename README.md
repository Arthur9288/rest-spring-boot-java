# RESTful API — Spring Boot & Java

<div align="center">

[![Continuous Integration and Delivery with Github Actions](https://github.com/Arthur9288/rest-spring-boot-java/actions/workflows/continuous-deployment.yml/badge.svg)](https://github.com/Arthur9288/rest-spring-boot-java/actions/workflows/continuous-deployment.yml)
![Java](https://img.shields.io/badge/Java-21-orange?logo=openjdk&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring%20Boot-3.4.1-brightgreen?logo=springboot&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-9.1.0-blue?logo=mysql&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-Containerized-2496ED?logo=docker&logoColor=white)

**API RESTful de nível profissional, construída com as melhores práticas de engenharia de software moderna.**

</div>

---

## 📌 Sobre o Projeto

Este projeto é uma **API RESTful completa e production-ready**, desenvolvida em **Java 21** com **Spring Boot 3.4.1**. Vai muito além de um simples CRUD — demonstra na prática as competências esperadas de um desenvolvedor backend sênior, cobrindo desde a arquitetura da aplicação até a entrega contínua em produção.

O projeto foi construído com foco em **qualidade, confiabilidade e manutenibilidade**, sendo respaldado por uma suíte abrangente de testes unitários e de integração, e operando através de um pipeline de CI/CD totalmente automatizado.

---

## ✨ Destaques do Projeto

| Categoria | Tecnologias e Práticas |
|---|---|
| 🔐 **Segurança** | Spring Security + JWT (Auth0) |
| 🧪 **Qualidade & Testes** | JUnit 5, Mockito, REST Assured, Testcontainers |
| 📦 **Serialização** | JSON, XML e YAML nativos via Jackson |
| 🚀 **DevOps** | Docker, Docker Compose, GitHub Actions (CI/CD) |
| 📄 **Documentação** | Swagger / OpenAPI 3 integrado |
| 🗃️ **Banco de Dados** | MySQL + Flyway (migrações versionadas) |
| 🔗 **Hypermedia** | HATEOAS (Spring HATEOAS) |
| 📊 **Exportação** | PDF (JasperReports), XLSX (Apache POI), CSV |
| 📁 **Upload/Download** | Serviço completo de gerenciamento de arquivos |
| 📧 **E-mail** | Envio de e-mails via Spring Mail |
| 📱 **QR Code** | Geração de QR Codes com ZXing |
| 🔍 **Monitoramento** | Portainer para gerenciamento de containers |

---

## 🧪 Estratégia de Testes — A Alma do Projeto

Uma das partes que mais me orgulho neste projeto é a **cobertura de testes robusta e profissional**, implementada em múltiplas camadas seguindo as melhores práticas da indústria.

### 🔬 Testes Unitários (Unit Tests)

Validam a lógica de negócio isoladamente, com dependências mockadas via **Mockito**, garantindo que cada componente funcione corretamente de forma independente:

- **`PersonServicesTest`** — Cobre todos os cenários da camada de serviço de pessoas: criação, leitura, atualização, deleção e tratamento de exceções
- **`BookServicesTest`** — Valida toda a lógica de negócio da entidade Book, incluindo edge cases
- **`ObjectMapperTests`** — Garante a correta conversão entre entidades e DTOs (Value Objects)
- **`MockPerson` / `MockBook`** — Fábricas de objetos de teste reutilizáveis para manter os testes limpos e organizados

### 🔗 Testes de Integração (Integration Tests)

Os testes de integração são o grande diferencial deste projeto. Utilizando **Testcontainers**, cada teste sobe um **banco de dados MySQL real em um container Docker efêmero**, garantindo que os testes rodem em um ambiente idêntico ao de produção — sem mocks de banco de dados, sem surpresas em produção.

Os testes cobrem os endpoints REST em **três formatos de serialização diferentes**:

#### 👤 Endpoints de Pessoa
| Classe de Teste | Formato | Cobertura |
|---|---|---|
| `PersonControllerJsonTest` | JSON | CRUD completo + paginação + desabilitar pessoa |
| `PersonControllerXmlTest` | XML | CRUD completo + paginação + desabilitar pessoa |
| `PersonControllerYamlTest` | YAML | CRUD completo + paginação + desabilitar pessoa |

#### 📚 Endpoints de Livro
| Classe de Teste | Formato | Cobertura |
|---|---|---|
| `BookControllerJsonTest` | JSON | CRUD completo + paginação |
| `BookControllerXmlTest` | XML | CRUD completo + paginação |
| `BookControllerYamlTest` | YAML | CRUD completo + paginação |

#### 🔑 Autenticação & Outros
| Classe de Teste | Descrição |
|---|---|
| `AuthControllerJsonTest` | Fluxo completo de autenticação via JWT em JSON |
| `AuthControllerXmlTest` | Fluxo completo de autenticação via JWT em XML |
| `AuthControllerYamlTest` | Fluxo completo de autenticação via JWT em YAML |
| `SwaggerIntegrationTest` | Garante que a documentação Swagger está disponível e operacional |
| `PersonRepositoryTest` | Valida queries customizadas e acesso ao banco de dados |

> **29 classes de teste** cobrindo **unitários, integração, repositório e contrato de API**, rodando contra um banco de dados real via Testcontainers.

---

## 🛠 Stack Tecnológica

### Backend
- **Java 21** + **Spring Boot 3.4.1**
- **Spring Security** com autenticação stateless via **JWT (Auth0)**
- **Spring HATEOAS** para APIs hypermedia-driven (nível 3 de maturidade REST)
- **Spring Data JPA** + **Hibernate**
- **Flyway** para migrações de banco de dados versionadas

### Serialização & Conteúdo
- **Jackson** — JSON, XML e YAML nativamente
- Suporte a `application/json`, `application/xml` e `application/x-yaml`

### Relatórios & Exportação
- **JasperReports** — Geração de PDFs
- **Apache POI** — Criação de planilhas XLSX
- **Apache Commons CSV** — Exportação e importação CSV
- **ZXing** — Geração de QR Codes

### Banco de Dados
- **MySQL 9.1.0** (produção)
- **Flyway** — Controle de versão do schema

### Testes
- **JUnit 5** — Framework de testes
- **Mockito** — Mock de dependências nos unit tests
- **REST Assured** — Testes de API REST de forma fluente
- **Testcontainers** — Banco de dados real em containers durante os testes

### Infra & DevOps
- **Docker** + **Docker Compose** — Containerização e orquestração local
- **GitHub Actions** — Pipeline CI/CD (build → test → push → deploy)
- **Docker Hub** — Repositório de imagens Docker
- **Portainer** — Interface web para gerenciamento de containers

### Documentação
- **SpringDoc OpenAPI 3 / Swagger UI** — Documentação interativa e automática

---

## 🏗 Arquitetura

```
src/
├── main/java/
│   ├── controllers/        # Camada REST (PersonController, BookController, AuthController...)
│   ├── services/           # Regras de negócio (PersonService, BookService, AuthService...)
│   ├── repositories/       # Acesso a dados (PersonRepository, BookRepository...)
│   ├── model/              # Entidades JPA (Person, Book, User, Permission)
│   ├── data/vo/            # DTOs / Value Objects
│   ├── security/           # JWT Filter, Token Provider, Security Config
│   ├── file/               # Upload, Download, Exporters (PDF, XLSX, CSV)
│   ├── config/             # Configurações (OpenAPI, Security, CORS, Mail...)
│   └── exceptions/         # Hierarquia de exceções customizadas
│
└── test/java/
    ├── integrationtests/   # Testes de integração por recurso e formato
    │   ├── controller/json/
    │   ├── controller/xml/
    │   ├── controller/yaml/
    │   └── repository/
    └── unittests/          # Testes unitários de services e mappers
```

---

## 🚀 Como Executar

### Pré-requisito: apenas Docker instalado

Para rodar a aplicação completa (API + MySQL + Portainer) com um único comando:

```bash
# 1. Clone o repositório
git clone https://github.com/Arthur9288/rest-spring-boot-java.git
cd rest-spring-boot-java

# 2. Suba toda a stack
docker-compose up -d
```

O Docker Compose irá automaticamente:
1. ✅ Baixar e iniciar o **MySQL 9.1.0**
2. ✅ Buildar e iniciar a **API Spring Boot**
3. ✅ Iniciar o **Portainer** para gerenciamento visual dos containers
4. ✅ Executar todas as **migrações do Flyway**

---

## 🌐 Acesso

Após os containers iniciarem:

| Serviço | URL |
|---|---|
| 🌍 API Root | [http://localhost:8080](http://localhost:8080) |
| 📋 Swagger UI | [http://localhost:8080/swagger-ui.html](http://localhost:8080/swagger-ui.html) |
| 🐳 Portainer | [http://localhost:9000](http://localhost:9000) |

---

## 🔐 Autenticação

A API utiliza **JWT (JSON Web Token)** para autenticação stateless. O fluxo é:

1. **Login** — `POST /auth/signin` com credenciais → retorna `accessToken` + `refreshToken`
2. **Usar Token** — Adicione o header `Authorization: Bearer <accessToken>` em todas as requisições
3. **Refresh** — `PUT /auth/refresh/{username}` para renovar o token sem novo login

---

## 📡 Principais Endpoints

### 👤 Pessoas
```
GET    /api/person/v1              → Lista paginada de pessoas
GET    /api/person/v1/{id}         → Busca pessoa por ID
GET    /api/person/v1/findByName/{name} → Busca por nome
POST   /api/person/v1              → Cria nova pessoa
PUT    /api/person/v1              → Atualiza pessoa
PATCH  /api/person/v1/disablePerson/{id} → Desabilita pessoa
DELETE /api/person/v1/{id}         → Remove pessoa
GET    /api/person/v1/exportPage   → Exporta lista em PDF/XLSX/CSV
```

### 📚 Livros
```
GET    /api/book/v1                → Lista paginada de livros
GET    /api/book/v1/{id}           → Busca livro por ID
POST   /api/book/v1                → Cria novo livro
PUT    /api/book/v1                → Atualiza livro
DELETE /api/book/v1/{id}           → Remove livro
```

### 📁 Arquivos
```
POST   /api/file/v1/uploadFile     → Upload de arquivo único
POST   /api/file/v1/uploadMultipleFiles → Upload múltiplo
GET    /api/file/v1/downloadFile/{filename} → Download de arquivo
```

> 💡 Todos os endpoints aceitam `application/json`, `application/xml` e `application/x-yaml` via header `Accept`.

---

## ⚙️ Pipeline CI/CD (GitHub Actions)

O projeto possui um pipeline de **Integração e Entrega Contínua** totalmente automatizado:

```
Push para main
     │
     ▼
┌─────────────┐    ┌─────────────┐    ┌─────────────────┐    ┌──────────────┐
│   Checkout  │───▶│   Build &   │───▶│  Push Docker    │───▶│   Deploy     │
│    Code     │    │  Run Tests  │    │  Image to Hub   │    │ (Produção)   │
└─────────────┘    └─────────────┘    └─────────────────┘    └──────────────┘
```

- **Build automático** a cada push
- **Todos os testes executados** (unitários + integração com Testcontainers) antes de qualquer deploy
- **Imagem Docker publicada** no Docker Hub apenas se todos os testes passarem



---
