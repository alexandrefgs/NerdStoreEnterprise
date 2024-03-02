NerdStoreEnterprise
Visão Geral
Bem-vindo ao NerdStoreEnterprise, um projeto de E-Commerce inovador que utiliza microsserviços, gRPC, API Gateway, Docker, NGINX com Load Balancing e SSL para oferecer uma experiência de compra robusta e segura.

Arquitetura
API de Pedidos (DDD)
A API de Pedidos segue a arquitetura DDD, com camadas distintas para a API, domínio e infraestrutura. Utilizando CQRS, permite separar operações de leitura e gravação.

API de Clientes
A API de Clientes adota uma abordagem de camadas lógicas, com foco nas operações de aplicação, dados (Entity Framework), e domínio para agregações e entidades.

APIs de Pagamento, Carrinho e Catálogo
Desenvolvidas como microsserviços, essas APIs implementam comunicação assíncrona via RabbitMQ, garantindo a consistência e a escalabilidade necessárias.

Comunicação e Integração
API Gateway: Facilita a comunicação entre as APIs de Pagamento, Pedido, Catálogo e Carrinho, proporcionando uma entrada única e simplificada para os clientes.

gRPC e JSON: A comunicação entre a aplicação frontend e a API Gateway utiliza JSON, enquanto a interação específica entre a API de Carrinho e a API Gateway de Compras é realizada através do eficiente protocolo gRPC com ProtoBuf.

Identidade e Segurança: Implementação de tokens JWT, refresh tokens e chave assimétrica para garantir autenticação segura e autorização.

Deploy em Containers Docker
O projeto é completamente contido em contêineres Docker para facilitar a implantação e escalabilidade. O NGINX realiza Load Balancing entre quatro instâncias do frontend, conectando-se às APIs de Compras, que por sua vez interagem com as APIs necessárias para processar transações. Tanto o RabbitMQ quanto os bancos de dados (SQL Server e Event Store) são isolados em contêineres individuais. A segurança é reforçada com a implementação de SSL.
