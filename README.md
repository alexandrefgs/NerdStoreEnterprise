# NerdShop - Uma aplicação de referência de comércio eletrônico com microservices construída com ASP.NET 3

Esta aplicação foi criada para fins educacionais e baseada em diversos cursos do site [desenvolvedor.io](https://desenvolvedor.io/).
Uma aplicação de referência do mundo real desenvolvida por [desenvolvedor.io](https://desenvolvedor.io/) ❤️ Brasil, implementando as tecnologias mais comuns e amplamente utilizadas para compartilhar com a comunidade técnica a melhor forma de desenvolver aplicativos completos e complexos com .NET.

---

<p align="center">
    <img alt="DevStore" src="https://user-images.githubusercontent.com/5068797/164293734-a72fbeeb-0965-4413-a624-29e1c56c25df.png" />
</p>

## Quer aprender tudo para construir um aplicativo como este?  :mortar_board:
Confira estes cursos online na [desenvolvedor.io](https://desenvolvedor.io/) (apenas em português)

- [ASP.NET Core Expert](https://desenvolvedor.io/formacao/asp-net-core-expert)
- [Software Architect](https://desenvolvedor.io/formacao/arquiteto-de-software)

## Tecnologias / Componentes Implementados

- .NET 3
    - ASP.NET MVC Core
    - ASP.NET WebApi
    - ASP.NET Minimal API
    - ASP.NET Identity Core
    - Refresh Token
    - JWT com chaves pública/privada rotativas    
    - GRPC
    - Background Services
    - Entity Framework Core 6

- Componentes / Serviços
    - RabbitMQ
    - EasyNetQ
    - Refit 
    - Polly
    - Bogus
    - Dapper
    - FluentValidator
    - MediatR
    - Swagger UI com suporte JWT
    - NetDevPack
    - NetDevPack.Identity
    - NetDevPack.Security.JWT

- Hospedagem
    - IIS
    - NGINX
    - Docker (com compose)

## Arquitetura:

### Arquitetura completa implementando as preocupações mais importantes e utilizadas como:

- Hexagonal Architecture
- Clean Code
- Clean Architecture
- DDD - Domain Driven Design (Camadas e Padrão de Modelo de Domínio)
- Domain Events
- Domain Notification
- Domain Validations
- CQRS (Consistência Imediata)
- Retry Pattern
- Circuit Breaker
- Unit of Work
- Repository
- Specification Pattern
- API Gateway / BFF

---

## Visão Geral da Arquitetura

### Toda a aplicação é baseada em uma única solução com 7 APIs e uma aplicação web (MVC)
<p align="center">
    <img alt="read before" src="https://user-images.githubusercontent.com/5068797/161202409-edcf2f38-0714-4de5-927d-1a02be4501ec.png" />
</p>

---

Esta é uma aplicação de referência, onde cada microserviço tem seu próprio banco de dados e representa um contexto delimitado (conceito DDD).
Existe um BFF / API Gateway para gerenciar as solicitações de Carrinho / Pedido / Pagamento e a estrutura de dados das respostas.

<p align="center">
    <img alt="read before" src="https://user-images.githubusercontent.com/5068797/161207732-e4f67ce4-624d-4067-a756-67ee1bb553de.png" />
</p>

---

## Como Começar
Você pode executar o projeto NerdShop em qualquer sistema operacional. **Certifique-se de ter o Docker instalado em seu ambiente.** ([Obtenha a Instalação do Docker](https://docs.docker.com/get-docker/))

Clone o repositório NerdShop e vá para a pasta **/Docker** e então:

### Se você só quer executar a aplicação NerdShop no seu ambiente Docker:

docker-compose -f nerdstore_production.yml up

### Se você quer construir as imagens locais e executar a aplicação NerdShop no seu ambiente Docker:

Este compose fornecerá um contêiner de banco de dados para cada serviço da API.

docker-compose -f nerdstore_production.yml up --build

---

### Se você quer executar localmente com o VS/VS Code:

Você precisará de:

- Docker
- Instância SQL (ou contêiner)

Então, você pode editar o Docker compose para apenas executar as dependências de banco de dados e fila e economizar seu tempo.

![image](https://user-images.githubusercontent.com/5068797/161358024-bd5754b6-61e3-47f2-bd17-bd3c32ec4bdd.png)

---

## Sobre
O DevStore foi orgulhosamente desenvolvido pela equipe [desenvolvedor.io](https://desenvolvedor.io/) ❤️<img alt="Brasil" src="https://user-images.githubusercontent.com/5068797/161345649-c7184fdc-2bc3-42a9-8fb6-6ffee9c8f9c2.png" width="20" height="14" /> sob a [licença MIT](LICENSE).

