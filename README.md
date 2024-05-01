# Auth API 

A Auth API é uma solução robusta e eficiente, desenvolvida para fornecer serviços seguros de autenticação e registro de usuários. Utilizando as tecnologias Spring Framework, Spring Security e H2 Database, projetado para oferecer uma base sólida para a implementação de sistemas de autenticação em aplicativos web.

## Tecnologias Utilizadas - Extensões

- spring data-jpa
- spring security
- spring web
- spring devtools
- lombok
- h2 database

## Rotas
Nota: Esta API utiliza JSON (JavaScript Object Notation) para troca de dados. Ao interagir com as rotas, certifique-se de que suas respostas estejam no formato JSON. Siga o tópico 'Entidades' para garantir que as solicitações funcionem corretamente.

| Action                     | Endpoint                                                                   | Description                                           |
|----------------------------|----------------------------------------------------------------------------|-------------------------------------------------------|
| Login                      | [http://localhost:8080/auth/login](http://localhost:8080/auth/login)       | Endpoint para realizar login de usuarios              |
| Register                   | [http://localhost:8080/auth/register](http://localhost:8080/auth/register) | Endpoint para realizar o cadastro de usuarios         |
| Auth info                  | [http://localhost:8080/user](http://localhost:8080/user)                   | Endpoint para validar usuarios                        |

## Entidades 
  ```json
[
    {
        "name": "John Doe",
        "email": "johndoe@gmail.com",
        "password": "123456789"
    }
]
```

## Teste com Postman
Para realizar os testes dos endpoint foi usado [Postamn](https://www.postman.com/), caso não o tenha instalado clique em seu nome para ser direcionado a pagina de download.

## Instalação e Uso
Para que o projeto rode, é preciso que você tenha o Java instalado em sua maquina. Siga esses passos: 

1. clone o repositorio.
2. Navegue até o arquivo LoginAuthApiAplication.
3. Execute 'java -jar nome-do-arquivo-jar.jar' ou execute pelo 'run'.
4. Abra o Postman e inclua as rotas passadas seguindo fielmente sua url.
5. Digite suas entidades. 

 ## Arquitetura
```bash
├── src/main/java/com.example.loginauthapi
│ ├── Controllers
│ │ ├── AuthController.java
│ │ └── UserController.java
│ ├── Domain
│ │ └── user
│ │ └── User.java
│ ├── DTO
│ │ ├── LoginRequestDTO.java
│ │ ├── RegisterRequestDTO.java
│ │ └── ResponseDTO.java
│ ├── Infra
│ │ ├── Cors
│ │ │ └── CorsConfig.java
│ │ └── Security
│ │ ├── CustomUserDetailsService.java
│ │ ├── SecurityConfig.java
│ │ ├── SecurityFilter.java
│ │ └── TokenService.java
│ └── Repositories
│ └── LoginAuthApiApplication.java
```

## License

This project is licensed under the MIT License.
