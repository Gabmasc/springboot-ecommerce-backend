# 🛒 E-commerce Back-end | Java & Spring Boot

Back-end de um **e-commerce desenvolvido em Java com Spring Boot**, com foco em **boas práticas de arquitetura**, organização por domínio e padrões amplamente utilizados no mercado.

O projeto foi iniciado como um **monólito REST**, com estrutura preparada para **evolução, escalabilidade e futura modularização**, servindo como **projeto de portfólio** e base realista para um sistema de e-commerce.

---

## 🚀 Visão Geral

Este projeto tem como objetivo demonstrar a construção de um back-end **robusto, organizado e profissional**, priorizando:

- Arquitetura bem definida desde o início
- Separação clara de responsabilidades
- Versionamento de banco de dados
- Padronização de ambiente com Docker
- Código legível e fácil de manter

Mesmo em estágio inicial, o projeto segue práticas comuns em **ambientes corporativos**.

---

## 🧠 Decisões de Arquitetura

- Arquitetura **RESTful**
- Projeto **monolítico organizado por domínio**
- Controllers enxutos, regras de negócio concentradas na camada de Service
- Preparado para futuras evoluções como:
    - Autenticação e autorização
    - Mensageria
    - Cache
    - Microserviços

📌 A organização por domínio facilita manutenção, testes e futura extração de módulos.

---

## 🗂️ Estrutura do Projeto
```
com.seuprojeto.ecommerce
├── auth # Autenticação (em evolução)
├── user # Domínio de usuários
├── product # Domínio de produtos
├── order # Domínio de pedidos
├── cart # Carrinho de compras
├── config # Configurações globais
├── exception # Tratamento centralizado de erros
└── shared # Componentes reutilizáveis
```
---

## ⚙️ Tecnologias Utilizadas

- **Java 17**
- **Spring Boot**
- **Spring Web**
- **Spring Data JPA**
- **Hibernate**
- **PostgreSQL**
- **Flyway** (controle de migrações)
- **Docker & Docker Compose**
- **Maven**

> 🔐 **Spring Security e JWT** ainda não foram implementados nesta fase inicial e fazem parte do roadmap do projeto.

---

## 🗄️ Banco de Dados & Migrações

O controle do schema do banco de dados é feito exclusivamente com **Flyway**, garantindo:

- Versionamento do banco
- Histórico de alterações
- Ambiente previsível entre desenvolvedores

O Hibernate está configurado apenas para **validar o schema**, evitando alterações automáticas no banco:

```yaml
spring.jpa.hibernate.ddl-auto=validate
```
---

## 🐳 Ambiente de Desenvolvimento com Docker

O projeto possui um arquivo docker-compose.yaml versionado na raiz do repositório, responsável por subir:

- PostgreSQL

- PgAdmin

Subir o ambiente local:
```
docker-compose up -d
```
---

## 🚧 Status do Projeto

🟡 **Em desenvolvimento**

**Implementado até o momento:**

- Estrutura base do projeto

- Arquitetura organizada por domínio

- Integração Flyway + JPA

- Migração inicial da tabela de usuários

- Ambiente dockerizado para desenvolvimento

**Funcionalidades planejadas:**

- Cadastro e login de usuários

- Autenticação e autorização com JWT

- Controle de acesso por roles

- CRUD de produtos

- Carrinho de compras

- Fluxo de pedidos
---
## 👨‍💻 Autor

- Gabriel Mascarenhas
- Desenvolvedor Back-end Java
- Foco em APIs REST, arquitetura limpa e sistemas escaláveis