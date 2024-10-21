# Santander Dev Week 2023 - Java API

Este é um projeto da Santander Dev Week 2023, onde desenvolvi uma RESTful API utilizando Java 17 e Spring Boot 3.

## Principais Tecnologias
- **Java 17**: Utilizei a versão LTS mais recente do Java, aproveitando as inovações que essa linguagem robusta e amplamente utilizada oferece.
- **Spring Boot 3**: Trabalhei com a versão mais recente do Spring Boot, que maximizou minha produtividade com sua poderosa autoconfiguração.
- **Spring Data JPA**: Explorei essa ferramenta para simplificar a camada de acesso aos dados, facilitando a integração com bancos de dados SQL.
- **OpenAPI (Swagger)**: Criei uma documentação de API eficaz e de fácil compreensão, utilizando OpenAPI (Swagger) para facilitar o uso da API.
- **Railway**: Utilize esta plataforma para facilitar o deploy e monitoramento da solução na nuvem, além de oferecer diversos bancos de dados como serviço e pipelines de CI/CD.

## [Link do Figma]
Utilizei o Figma para abstrair o domínio da API, sendo uma ferramenta útil para a análise e o projeto da solução.

## Diagrama de Classes (Domínio da API)

```mermaid
classDiagram
  class User {
    -String name
    -Account account
    -Feature[] features
    -Card card
    -News[] news
  }

  class Account {
    -String number
    -String agency
    -Number balance
    -Number limit
  }

  class Feature {
    -String icon
    -String description
  }

  class Card {
    -String number
    -Number limit
  }

  class News {
    -String icon
    -String description
  }

  User "1" *-- "1" Account
  User "1" *-- "N" Feature
  User "1" *-- "1" Card
  User "1" *-- "N" News


Documentação da API (Swagger)
https://sdw-2023-prd.up.railway.app/swagger-ui.html
Esta API ficará disponível no Railway por um período de tempo limitado, mas este é um código-fonte aberto. Sinta-se à vontade para cloná-lo, modificá-lo e executá-lo localmente ou onde achar mais interessante. Não esqueça de marcar a gente quando divulgar a sua solução! 🥰

IMPORTANTE
Para aqueles interessados em desenvolver a tela inicial do App do Santander (Figma) em Angular, Android, iOS ou Flutter, caso a URL produtiva não esteja mais disponível, deixamos um Backup no GitHub Pages, é só dar um GET lá 😘

URL de Produção: https://sdw-2023-prd.up.railway.app/users/1
Mock (Backup): https://digitalinnovationone.github.io/santander-dev-week-2023-api/mocks/find_one.json
