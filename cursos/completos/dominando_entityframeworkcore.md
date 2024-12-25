# Dominando Entity Framework Core
## Introdução
  - Apresentação
  - O que é o Entity Framework Core?
  - Teste os seus conhecimentos

## Setup do Ambiente
  - Instalação do .NET 5 e SQL Server
  - Criando um projeto via CLI
  - Criando classes de entidades 

## EF Database
  - Introdução
  - Para que serve o Ensure Deleted/Created?
  - Resolvendo GAP do EnsureCreated para múltiplos contextos
  - HealthCheck do banco de dados
  - Gerenciando o estado da Conexão
  - Conhecendo os comandos ExecuteSql
  - Como se proteger de ataques do tipo SQL Injection?
  - Detectando migrações Pendentes
  - Forçando uma migração
  - Recuperando todas as migrações existentes em sua aplicação
  - Recuperando migrações aplicadas em seu banco de dados
  - Gerando o script de criação SQL do modelo de dados
  - Teste os seus conhecimentos
Tipos de carregamento - DeepDive
  - Tipos de carregamentos
  - Consultando dados usando carregamento adiantando (Eager)
  - Consultando dados usando carregamento explícito (Explicitly)
  - Consultando dados usando carregamento lento (LazyLoad) 
  - Teste os seus conhecimentos
## Consultas
  - Introdução a consultas 
  - Configurando um filtro global 
  - Ignorando filtros globais 
  - Criando consultas projetadas 
  - Criando consultas parametrizadas 
  - Criando consultas interpoladas 
  - Usando o recuso TAG em suas consultas para auditar comandos 
  - Entendendo a diferença em consultas 1xN vs Nx1 
  - Divisão de consultas com SplitQuery 

## Stored Procedures
  - Introdução
  - Criando uma procedure de inserção
  - Executando inserção via procedure
  - Criando uma procedure de consulta
  - Executando uma consulta via procedure

## Infraestrutura
  - Introdução 
  - Configurando um log simplificado 
  - Filtrando eventos de seus logs 
  - Gravando seus logs em um arquivo 
  - Habilitando erros detalhados 
  - Habilitando visualização dos dados sensíveis 
  - Habilitando Batch Size 
  - Configurando o Timeout do comando global 
  - Configurando o Timeout do comando para um fluxo 
  - Habilitando resiliência para sua aplicação 
  - Criando uma estratégia de resiliência 

## Modelo de dados
  - Introdução
  - Collations
  - Sequencias
  - Índices 
  - Propagação de dados
  - Esquemas
  - Conversores de Valores 
  - Criando um conversor de valor customizado 
  - O que é Shadow Properties
  - Configurando uma propriedade de sombra
  - Inserindo e Consultando dados usando uma propriedade de sombra
  - Owned Types 
  - Configurando Relacionamento um-para-um 
  - Configurando Relacionamento um-para-muitos
  - Configurando Relacionamento muitos-para-muitos
  - Customização muitos-para-muitos
  - Campo de apoio
  - Configurando modelo de dados com TPH 
  - Configurando modelo de dados do TPT
  - Sacola de propriedades

## Atributos - DataAnnotations
  - Introdução 
  - Atributo Table 
  - Atributo Inverse Property 
  - Atributo NotMapped 
  - Atributo Database Generated 
  - Atributo Index 
  - Atributo Comment 
  - Atributo Backing Field 
  - Atributo Keyless 

## EF Functions
  - Introdução
  - Funções de datas 
  - Função Like
  - Função DataLength
  - Função Property
  - Função Collate

## Interceptação
  - Introdução 
  - O que são interceptadores de comandos? 
  - Criando e registrando um interceptador 
  - Sobrescrevendo métodos da classe base 
  - Aplicando hint NOLOCK nas consultas 
  - Interceptando abertura de conexão com o banco 
  - Interceptando alterações 

## Transações
  - Introdução 
  - O que é transação? 
  - Comportamento padrão do EF Core 
  - Gerenciando transação manualmente 
  - Revertendo uma transação 
  - Salvando ponto de uma transação 
  - Usando TransactionScope 

## UDFs (Funções definidas pelo usuário)
  - Introdução
  - O que é UDF?
  - Built-In Function
  - Registrando Funções
  - Registrando Funções Via Fluent API
  - Função defina pelo usuário
  - Customizando uma função complexa 
## Performance
  - Introdução
  - Tracking vs NoTracking
  - Resolução de Identidade 
  - Desabilitando rastreamento de consultas
  - Consulta projeta e rastreada
  - Consultas Projetas
## Migrations
  - Introdução
  - Migrações
  - Dependências necessárias para criar uma migração
  - Gerando uma migração
  - Analisando arquivos da migração
  - Gerando script SQL
  - Gerando script SQL idempotente
  - Aplicando migração no banco de dados
  - Desfazendo migrações
  - Migrações pendentes
  - Engenharia reversa 
## Acessando outros bancos de dados
  - Introdução
  - Provider PostgreSQL 
  - Provider SQLite
  - Provider InMemory
  - Provider Azure Cosmos DB
## Aplicação MultiTenant
  - Introdução
  - Arquitetura Multi-tenant
  - Single-tenant vs Multi-tenant
  - Estratégias Multi-tenant
  - Criando o projeto
  - Instalando dependências
  - Preparando o ambiente 
  - Estratégia 1 - Identificar na tabela 
  - Estratégia 2 - Schema 
  - Estratégia 3 - Banco de dados 
## Padrão Repository & UoW
  - Introdução
  - O que é Repository Pattern?
  - O que é Unit-Of-Work?
  - DbContext já é um padrão Repository & UoW
  - Preparando o Ambiente 
  - Implementando Repository Pattern 
  - Implementando Persistência na API
  - Implementando UoW - Estratégia I
  - Implementando UoW - Estratégia II
  - Criando um Repositório Genérico 
  - Consulta com Repositório Genérico
## Dicas e Truques
  - Introdução
  - Preparando o ambiente
  - Método ToQueryString
  - Análise com DebugView
  - Redefinindo o estado do contexto
  - Include com consultas filtradas
  - SingleOrDefault vs FirstOrDefault
  - Tabela sem chave primária
  - Usando Views de seu banco de dados
  - Forçando o uso do VARCHAR
  - Aplicando conversão de nomenclatura
  - Operadores de agregação
  - Operadores de agregação no agrupamento
  - Contadores de eventos
## Testes
  - Introdução
  - Preparando o ambiente
  - Criando entidade e contexto
  - Criando testes usando o provider InMemory 
  - Criando testes usando o provider SQLite 
## Sobrescrevendo comportamentos do EF Core
  - Introdução
  - Preparando o ambiente
  - Criando entidade e contexto
  - Gerador SQL customizado
  - Criando factory do gerador SQL
  - Usando o gerador SQL customizado
## Diagnostics
  - Introdução
  - O que é Diagnostic Source?
  - Criando um interceptador
  - Criando um listener
  - Assinando o listener e validando