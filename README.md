# Produtos API

API REST para gerenciamento de produtos desenvolvida com Spring Boot.

## Tecnologias

- Java 21
- Spring Boot 3.5.4
- Spring Data JPA
- H2 Database (in-memory)
- Maven

## Como executar

```bash
mvn spring-boot:run
```

A aplicação estará disponível em: `http://localhost:8080`

## Endpoints

### Criar produto
```http
POST /produtos
Content-Type: application/json

{
  "nome": "Produto Exemplo",
  "descricao": "Descrição do produto",
  "preco": 99.99
}
```

### Buscar produto por ID
```http
GET /produtos/{id}
```

### Buscar produtos por nome
```http
GET /produtos?nome=NomeDoProduto
```

### Atualizar produto
```http
PUT /produtos/{id}
Content-Type: application/json

{
  "nome": "Produto Atualizado",
  "descricao": "Nova descrição",
  "preco": 149.99
}
```

### Deletar produto
```http
DELETE /produtos/{id}
```

## Banco de dados

A aplicação utiliza H2 Database em memória. Para acessar o console:

- URL: `http://localhost:8080/h2-console`
- JDBC URL: `jdbc:h2:mem:produtos`
- Username: `sa`
- Password: `password`

## Estrutura do projeto

```
src/main/java/com/example/java_crud/
├── controller/ProdutoController.java
├── model/Produto.java
├── repository/ProdutoRepository.java
└── JavaCrudApplication.java
```