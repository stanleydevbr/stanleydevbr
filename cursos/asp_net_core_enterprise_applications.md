## Introdução
  - Apresentação
  - Objetivos e pré-requisitos 

## Enterprise Applications
  - Pensando em aplicações corporativas
  - Microsserviços não são bala de prata
  - Decisões de arquitetura 
  - Tecnologias e ferramentas 
  
## API de Identidade
  - Fluxo de autenticação WebAPP - API 
  - Setup da arquitetura base 
  - Configuração do Identity 
  - Registro e login de usuário
  - Documentação da API e testes
  - Configurando o JWT na API 
  - Emitindo JWT pela controller
  - Response customizado 
  - Customizando as mensagens do Identity 
  - Refatoração e melhorias 

## Aplicação Web
  - Introdução
  - MVC ou Razor Pages?
  - Configurando a autenticação 
  - Models, Views e Controllers de login 
  - Consumindo uma API via HttpService 
  - Padronizando os objetos de retorno
  - Gerando o cookie através do JWT 
  - Obtendo dados de usuário do cookie
  - Tratamento de erros do response 
  - Exibindo os erros para o usuário
  - Tratamento de erros do servidor - pt I 
  - Tratamento de erros do servidor - pt II 
  - Boas práticas com HttpServices - pt I
  - Boas práticas com HttpServices - pt II 
  
## Comunicação com API's
  - Introdução
  - Layout do e-commerce
  - Arquitetura API Catalogo
  - Modelagem API Catalogo 
  - Acesso a dados API Catalogo 
  - Comportamentos básicos API Catalogo 
  - Validação de JWT na API Catalogo 
  - Validação de acesso baseado em claims 
  - Catalogo HttpService 
  - Entendendo os DelegatingHandlers 
  - Utilizando Refit para o consumo de API's 
  - Retry Pattern com Polly 
  - Circuit Breaker com Polly 
  - Melhorias na WebApp 

## Modelagem da API de Clientes
  - Introdução
  - O papel do cliente no negócio 
  - Definindo as entidades
  - Objetos de valor e validações 
  - Mapeamento das tabelas
  - Command e Command Handler 
  - MediatR e Command Handler 
  - Persistência via Command Handler
  - Validação de comandos
  - Trabalhando com eventos 
  - Execução do processo de cadastro 
  - Registro do cliente via WebApp 

## Comunicação entre API's com RabbitMQ
  - Introdução
  - Setup do RabbitMQ
  - O básico que você precisa saber sobre RabbitMQ 
  - Request Response Pattern 
  - Implementando o Request
  - Implementando o Response 
  - Executando a integração 
  - Customizacao do EventBus - pt I 
  - Customizacao do EventBus - pt II 
  - Customizacao do EventBus - pt III 
  - Validando cenários e recuperação de falhas 
  - Melhorando a resiliência da aplicação 

## API de Carrinho
  - Introdução
  - Decisões de arquitetura
  - Estrutura de dados da API
  - Reconhecimento do usuári
  - Comportamentos de negocio da API - pt I
  - Comportamentos de negocio da API - pt II
  - Comportamentos de negocio da API - pt III
  - Implementando o carrinho no front-end - pt I
  - Implementando o carrinho no front-end - pt II
  - Implementando o carrinho no front-end - pt III

## Processo de Pedidos
  - Introdução 
  - Implementando o BFF de Compras 
  - Consumindo serviços pelo BFF - pt I 
  - Consumindo serviços pelo BFF - pt II 
  - Conectando o BFF na WebApp 
  - Definindo a arquitetura da API de Pedidos 
  - Modelagem da entidade voucher e criação da tabela 
  - Application Query Stack e Specification Pattern 
  - Aplicando o voucher via BFF Compras 
  - Aplicando o voucher na API de Carrinho 
  - Aplicando o voucher na WebApp 
  - Modelagem do pedido no domínio 
  - Camada de infraestrutura de pedido 
  - Camada de application de pedido - pt I 
  - Camada de application de pedido - pt II 
  - Utilizando o Dapper na Query Stack - pt I 
  - Utilizando o Dapper na Query Stack - pt II
  - Manipulando o carrinho via RabbitMQ 
  - Finalizando a API de Pedido
  - Cadastro e consulta de endereço do cliente 
  - Configurações em validações no BFF de Compras 
  - Tratamento de erros na finalização do pedido 

## API de Pagamentos
  - Introdução
  - Como receber pagamentos online
  - Entendendo o Gateway de pagamento 
  - Solicitando processamento de pagamento
  - Modelagem das classes de pagamento
  - Facade com o gateway de pagamento
  - Background service de pagamento 
  - Testando a aplicação
  - Fluxo de captura e cancelamento
  - Rodando tarefas agendadas de forma nativa 
  - Obtendo pedidos autorizados via Dapper
  - Baixando o pedido do estoque 
  - Captura e cancelamento de pagamentos 
  - Explorando os cenários na aplicação 

## Melhorias e Novas Tecnologias
  - Introduçã
  - Paginação na API de Catálogo
  - Paginação no MVC
  - ViewComponent de paginação
  - Dica de pesquisa avançad
  - Identity Server - Você precisa dele
  - Criptografia simétrica é inseguro
  - JWK e JWKS na API de identidade
  - Implementando o JWK nas demais API's
  - Refresh Token na API de Identidade
  - Refresh Token na App MVC
  - gRPC - O futuro da comunicação?
  - Implementando um gRPC Server - pt I
  - Implementando um gRPC Server - pt II
  - Implementando um gRPC Client
  - Testando a chamada client/server com gRPC
  - Tratando erros do gRPC no clien

## Deploy e Docker
  - Introdução
  - Visão geral do Docker 
  - Docker Images 
  - Docker Containers 
  - Conhecimentos necessários 
  - Conhecendo o Dockerfile 
  - Limitações do Dockerfile 
  - Implementando o Docker-Compose 
  - Comunicação entre containers 
  - Acessando a base local via docker 
  - Rodando SQL Server via Docker 
  - Executando a aplicação completa em containers 
  - Implementando o NGINX - pt I 
  - Implementando o NGINX - pt II 
  - Implementando SSL no NGINX 
  - Comunicação interna via SSL 
  - Implementando Load Balancing no NGINX 
