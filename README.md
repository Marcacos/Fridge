# 🧊 Fridge

Sistema de gerenciamento de alimentos em geladeira, permitindo cadastro, listagem e exclusão de itens de forma simples e rápida via API REST.

![Java](https://img.shields.io/badge/Java-17%2B-orange?style=flat-square&logo=openjdk)
![Spring Boot](https://img.shields.io/badge/Spring%20Boot-3.x-brightgreen?style=flat-square&logo=springboot)
![H2 Database](https://img.shields.io/badge/H2-Database-blue?style=flat-square&logo=h2)
![Maven](https://img.shields.io/badge/Maven-Build-C71A36?style=flat-square&logo=apachemaven)
![License](https://img.shields.io/badge/license-MIT-lightgrey?style=flat-square)
![Status](https://img.shields.io/badge/status-em%20desenvolvimento-yellow?style=flat-square)

---

## 📋 Sobre o projeto

**Fridge** é uma API desenvolvida em **Java com Spring Boot** que permite o controle de alimentos armazenados na geladeira. Com ela é possível cadastrar novos itens, listar os alimentos existentes e excluir aqueles que não são mais necessários.

---

## 🚀 Tecnologias

Este projeto foi desenvolvido utilizando as seguintes tecnologias:

- **[Java](https://www.oracle.com/java/)** — linguagem de programação principal
- **[Spring Boot](https://spring.io/projects/spring-boot)** — framework para construção da API REST
- **[H2 Database](https://www.h2database.com/)** — banco de dados em memória para desenvolvimento e testes
- **[Maven](https://maven.apache.org/)** — gerenciador de dependências e build

---

## 🔧 Instalação

### Pré-requisitos

Antes de começar, você vai precisar ter instalado em sua máquina:

- [JDK 17+](https://www.oracle.com/java/technologies/downloads/)
- Uma IDE de sua preferência (recomendado: [IntelliJ IDEA](https://www.jetbrains.com/idea/))
- [Postman](https://www.postman.com/) ou ferramenta similar para testar as requisições

### Passo a passo

1. Clone o repositório:
   ```bash
   git clone https://github.com/seu-usuario/fridge.git
   ```

2. Abra o projeto no **IntelliJ** (ou na IDE de sua preferência).

3. Execute a aplicação clicando em **Run** na classe principal.

4. Com a aplicação rodando, acesse o console do banco H2 no navegador:
   ```
   http://localhost:8080/h2-console
   ```

5. Na tela de login do H2 Console, configure os campos:

   | Campo         | Valor                  |
      |---------------|------------------------|
   | JDBC URL      | `jdbc:h2:mem:testdb`   |
   | User Name     | `sa`                   |
   | Password      | *(deixe em branco)*    |

6. Clique em **Connect** para acessar o banco de dados em memória.

---

## ▶️ Uso

Com o projeto em execução, as requisições podem ser enviadas para a seguinte URL base:

```
http://localhost:8080/food
```

Utilize o **Postman** ou outra ferramenta de sua preferência para consumir a API.

### Exemplos de requisições

**Cadastrar um alimento**
```http
POST http://localhost:8080/food
Content-Type: application/json

{
  "name": "Leite",
  "quantity": 2,
  "experationDate": "2027-10-21"
}
```

**Listar todos os alimentos**
```http
GET http://localhost:8080/food
```

**Excluir um alimento**
```http
DELETE http://localhost:8080/food/{id}
```

> ⚠️ Os campos do corpo da requisição podem variar conforme a estrutura da entidade `Food` implementada no projeto.

---

## 📄 Licença

Este projeto está sob a licença MIT. Veja o arquivo [LICENSE](LICENSE) para mais detalhes.

---

<p align="center">Desenvolvido com ☕ e Spring Boot</p>