# User Registration API – Primeiro projeto com Spring Boot e Persistência de Dados.

Vídeo: https://www.youtube.com/watch?v=yW7RrWfUeHE 

Canal: Javanauta

Descrição: Este projeto marca o início dos meus estudos com o framework Spring Boot. Trata-se de uma API REST para cadastro de usuários, onde apliquei conceitos de arquitetura em camadas e integração com banco de dados. O objetivo principal foi compreender a injeção de dependências do Spring, o funcionamento do Spring Data JPA e a exposição de endpoints para operações de CRUD (Create, Read, Update, Delete).

Tecnologias & Ferramentas:

    Linguagem: Java 25 (JDK 25).

    Framework: Spring Boot.

    Persistência: Spring Data JPA / Hibernate.

    Banco de Dados: H2 Database (Banco em memória para desenvolvimento ágil).

    Produtividade: Lombok (Para redução de código boilerplate como Getters e Setters).

    Gerenciador de Dependências: Maven.

    Testes de API: Postman.

Funcionalidades da API:

    POST /usuario: Realiza o cadastro de um novo usuário (E-mail e Nome).

    GET /usuario?email={email}: Busca as informações de um usuário específico via Query Param.

    PUT /usuario?id={id}: Atualiza os dados de um usuário existente, utilizando lógica de validação ternária para preservar campos não enviados.

    DELETE /usuario?email={email}: Remove um usuário do sistema de forma transacional.

Destaques Técnicos:

    Arquitetura de Camadas: Organização clara entre Controller (entrada de dados), Business/Service (regras de negócio) e Infrastructure (entidades e acesso a dados).

    Tratamento Transacional: Uso da anotação @Transactional em operações sensíveis como o delete por e-mail, garantindo a integridade dos dados.

    Consultas Customizadas: Implementação de Derived Queries no JPA Repository (ex: findByEmail) para buscas que não fazem parte do padrão nativo.

    Configuração de Ambiente: Uso do application.properties para gerenciar portas de execução e console do banco H2.

Instalação/Uso:

    Clone este repositório.

    Certifique-se de ter o Maven e o JDK 23 instalados.

    Execute a aplicação através da sua IDE ou via terminal: ./mvnw spring-boot:run.

    Acesse o console do banco H2 em: http://localhost:8081/h2-console (ou a porta configurada).

    Utilize o Postman para interagir com os endpoints citados acima.

Contribuição:
Este é um projeto de aprendizado inicial em Spring Boot. Sugestões sobre tratamento de exceções customizadas ou implementação de DTOs (Data Transfer Objects) são muito bem-vindas.

Licença:
MIT License
