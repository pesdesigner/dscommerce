# DSCommerce - Projeto de Estudo com Spring Boot

Este projeto é uma aplicação de estudo desenvolvida utilizando **Spring Boot**. O objetivo do projeto é explorar e praticar conceitos fundamentais do framework, como APIs RESTful, validação de dados, tratamento de exceções e segurança.

## Descrição

A aplicação simula um sistema de e-commerce, onde usuários podem gerenciar produtos, categorias e pedidos. Inclui funcionalidades como autenticação de usuários, controle de acesso baseado em papéis (roles) e validação de dados. O projeto também demonstra como tratar exceções e retornar códigos de status HTTP apropriados.

## Endpoints

### Categorias
- **GET /categories**: Retorna todas as categorias.

### Produtos
- **POST /products**: Insere um novo produto (com validação de campos como nome, descrição e preço).
- **PUT /products/{id}**: Atualiza um produto existente.
- **GET /products/{id}**: Retorna um produto pelo seu ID.
- **DELETE /products/{id}**: Exclui um produto pelo seu ID.

### Pedidos
- **GET /orders/{id}**: Retorna um pedido pelo seu ID (acessível apenas pelo dono ou administrador).
- **POST /orders**: Cria um novo pedido.

### Autenticação
- **POST /login**: Autentica um usuário e gera um token JWT.

## Funcionalidades Principais

1. **Validação de Dados**:
    - Campos como `name`, `description` e `price` em `ProductDTO` são validados com anotações como `@NotBlank`, `@Size` e `@Positive`.

2. **Tratamento de Exceções**:
    - Exceções personalizadas como `ResourceNotFoundException`, `DatabaseException` e `ForbiddenException` são tratadas globalmente com `@ControllerAdvice`.

3. **Segurança**:
    - Controle de acesso baseado em papéis (roles) garante que apenas usuários autorizados acessem determinados endpoints.
    - Implementação de autenticação JWT para proteger a aplicação.

4. **DTOs e Entidades**:
    - Uso de DTOs (Data Transfer Objects) para separar a camada de API da camada de banco de dados.

5. **Camada de Serviço**:
    - A lógica de negócios é encapsulada em classes de serviço, garantindo uma arquitetura limpa.

## O Que Foi Aprendido

- Como criar uma API RESTful com Spring Boot.
- Implementação de validação de dados com anotações do `javax.validation`.
- Tratamento global de exceções com `@ControllerAdvice`.
- Segurança de endpoints com Spring Security e JWT.
- Uso de DTOs para gerenciar a transferência de dados entre camadas.
- Escrita de código limpo e manutenível com uma arquitetura em camadas.

## Tecnologias Utilizadas

- **Java**
- **Spring Boot**
- **Spring Security**
- **Hibernate/JPA**
- **Maven**
- **Banco de Dados H2** (para desenvolvimento e testes)

## Como Executar

1. Clone o repositório.
2. Abra o projeto na sua IDE.
3. Execute a aplicação utilizando o método `main` na classe `DscommerceApplication`.
4. Acesse a API em `http://localhost:8080`.

## Conclusão

Este projeto proporcionou uma experiência prática com o Spring Boot e seu ecossistema. Abrangeu tópicos essenciais como desenvolvimento de APIs RESTful, segurança e tratamento de exceções, tornando-se uma experiência valiosa para a construção de aplicações web robustas e seguras.