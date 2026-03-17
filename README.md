# 🏥 Voll.med - API

API REST desenvolvida para o gerenciamento de uma clínica médica. O sistema permite o cadastro e controle de médicos e pacientes, além de possuir regras de negócio complexas para o agendamento seguro de consultas.

## Tecnologias Utilizadas

* **Linguagem:** Java 17
* **Framework:** Spring Boot 3
* **Banco de Dados:** MySQL
* **Persistência & Migrações:** Spring Data JPA e Flyway
* **Segurança:** Spring Security e JWT (Auth0)
* **Testes:** JUnit 5, MockMvc, DataJpaTest e JacksonTester
* **Documentação:** SpringDoc OpenAPI (Swagger UI)
* **Facilitadores:** Lombok

## Funcionalidades (Endpoints Principais)

* **Autenticação (`/login`):** Validação de credenciais e geração de token JWT.
* **Médicos (`/medicos`):** CRUD completo com exclusão lógica (inativação) e validações de especialidade.
* **Pacientes (`/pacientes`):** CRUD completo com exclusão lógica.
* **Consultas (`/consultas`):** Agendamento de consultas com validações de regras de negócio (verificação de disponibilidade do médico, integridade do paciente, antecedência mínima, etc).

##  Como Executar

Configure as variáveis de ambiente necessárias no arquivo `application.properties` (na sua IDE ou sistema operacional):

```env
DB_HOST=localhost:3306
DB_NAME=vollmed_api
DB_USER=seu_usuario_mysql
DB_PASSWORD=sua_senha_mysql
JWT_SECRET=sua_chave_secreta_para_jwt
DB_TEST=vollmed_api_test  # Banco de dados exclusivo para rodar os testes
```

## Documentação da API
A documentação interativa dos endpoints pode ser acessada com a aplicação rodando através do navegador:

* **Swagger UI:** `http://localhost:8080/swagger-ui.html`
