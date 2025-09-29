# Workshop Spring Boot 3 + JPA / Hibernate 🚀

Projeto desenvolvido no curso de Java ministrado pelo professor **Nélio Alves** na plataforma da Udemy.
O objetivo é criar uma aplicação web com **API REST** utilizando **Spring Boot, JPA/Hibernate e banco de dados relacional**, praticando mapeamento objeto-relacional, serviços, repositórios e tratamento de exceções.

---

## 📌 Objetivos do Projeto

* Criar um projeto Spring Boot Java
* Implementar um modelo de domínio
* Estruturar camadas lógicas: `resource`, `service`, `repository`
* Configurar banco de dados de teste (H2)
* Povoar o banco de dados com dados iniciais
* Implementar operações CRUD (Create, Read, Update, Delete)
* Tratar exceções de forma personalizada

---

## 🛠 Tecnologias Utilizadas

* **Java 17+**
* **Spring Boot 3**
* **Spring Data JPA / Hibernate**
* **Spring Web**
* **H2 Database**
* **Postman**
* **PostgreSQL**
* **Maven**

---

## 📐 Modelo de Domínio

O sistema modela um fluxo simples de pedidos, com as seguintes entidades:

* **User**: cliente do sistema
* **Order**: pedido realizado por um cliente
* **OrderStatus**: enum para status do pedido
* **Category**: categorias de produtos
* **Product**: produtos disponíveis
* **OrderItem**: itens de pedido (relação muitos-para-muitos com atributos extras)
* **Payment**: pagamento associado ao pedido (relação um-para-um)

---

## 🚀 Como Executar o Projeto

1. Clone o repositório:

   ```bash
   git clone https://github.com/heitorhidalgo/workshop-springboot3-jpa.git
   cd workshop-springboot3-jpa
   ```

2. Certifique-se de ter instalado:

   * Java 17+
   * Maven

3. Rode o projeto em perfil de teste (H2):

   ```bash
   mvn spring-boot:run
   ```

4. Acesse a aplicação em:

   ```
   http://localhost:8080
   ```

5. Console H2 disponível em:

   ```
   http://localhost:8080/h2-console
   ```

---

## 📡 Exemplos de Endpoints (API REST)

### Usuários

* `GET /users` → lista todos os usuários
* `GET /users/{id}` → busca usuário por ID
* `POST /users` → cria novo usuário
* `PUT /users/{id}` → atualiza usuário existente
* `DELETE /users/{id}` → remove usuário

Exemplo de JSON para `POST /users`:

```json
{
  "name": "Maria Brown",
  "email": "maria@gmail.com",
  "phone": "988888888",
  "password": "123456"
}
```

### Pedidos

* `GET /orders` → lista todos os pedidos
* `GET /orders/{id}` → busca pedido por ID

---

## ⚠️ Tratamento de Exceções

* **ResourceNotFoundException** → retorna `404 NOT FOUND`
* **DatabaseException** → retorna `400 BAD REQUEST`
* **EntityNotFoundException** → usado em atualizações inválidas

As respostas seguem padrão JSON:

```json
{
  "timestamp": "2025-09-28T15:21:22Z",
  "status": 404,
  "error": "Resource not found",
  "message": "Id not found 10",
  "path": "/users/10"
}
```

---

## 👤 Autor

**Heitor Hidalgo**
* **GitHub:** [heitorhidalgo](https://github.com/heitorhidalgo)
* **LinkedIn:** [Heitor Hidalgo](https://www.linkedin.com/in/heitorhidalgo)
---

## 🙏 Agradecimentos

* Gostaria de agradecer ao professor **Nélio Alves** pela excelente didática no curso.
* **Link do curso na Udemy:** [Curso Nélio](https://www.udemy.com/course/java-curso-completo)

## 📄 Licença

Este projeto está licenciado sob a [MIT License](LICENSE).
