# Azure Pipelines - CI/CD, Docker e Kubernetes no Azure DevOps
Intrutor: **Higor Barbosa** - Solution Architecture | Cloud Specialist | SRE | Developer
Sobre o Curso: Integração e Entrega Contínua com Azure DevOps usando Docker, Kubernetes, Infraestrutura como Código (IaC) e Database
## Seção 1: Introdução a DevOps e Azure DevOps
* Introdução ao Modulo
* DevOps Básico
* Azure DevOps no Ciclo de Desenvolvimento
* Azure DevOps - Serviços e Principais Recursos
* Precificação do Azure DevOps e Azure Pipeline
* [Hands-On] Explorando o Azure
* [Hands-On] Usuários, Dashboard e Wiki
* [Hands-On] Azure Boards
* [Hands-On] Azure Repos
* [Hands-On] Azure Test Plan
* [Hands-On] Azure Artifacts
* [Hands-On] Extensões do Market Place
* Azure DevOps Server
* Teste 1: Quiz do Módulo
* Resumo do Módulo

## Seção 2: Azure Pipelines com Classic Editor
* Introdução ao Módulo
* Build Pipelines
* Workflow do Pipelines e Integração Continua
* Conceitos do Pipelines usando Classic Editor
* Ativar Execução de Pipeline usando Microsoft Self-Hosted Agent
* [Hands-On] Pipeline Básico
* [Hands-On] Agent Jobs
* [Hands-On] Agentless Jobs
* [Hands-On] Pipelines no Dashboard
* Variáveis, Grupos de Variáveis e Grupo de Tarefas
* [Hands-On] Variáveis e Grupo de Variáveis
* [Hands-On] Grupo de Tarefas
* Azure Key Vault
* [Hands-On] Utilizando Segredos do Azure Key Vault no Pipeline
* Triggers
* [Hands-On] Integração Continua com Classic Editor
* [Hands-On] Triggers - Agendamento de Builds com Editor Clássico
* [Hands-On] Build iniciado a partir de outro build
* [Hands-On] Propriedades do Build
* Azure App Service
* [Hands-On] Deploy usando Build Pipelines
* Teste 2: Quiz do Módulo
* Resumo do Módulo
  
## Seção 3: Azure Pipelines com YAML
* Introdução ao Módulo
* YAML
* Conceitos do Pipelines usando YAML
* [Hands-On] YAML Básico - Triggers, Pool e Steps
* [Hands-On] Triggers - Agendamento de Builds
* [Hands-On] YAML - Jobs, Dependências e Condições
* [Hands-On] YAML Stages
* [Hands-On] Usando Tasks e Variaveis
* [Hands-On] Templates YAML
* [Hands-On] YAML Release Pipelines
* [Hands-On] YAML no Visual Studio Code
* Teste 3: Quiz do Módulo
* Resumo do Módulo
  
## Seção 4: Agent Jobs no Azure Pipelines
* Introdução ao Módulo
* Agents no Azure Pipelines
* [Hands-On] Instalando Agente no Windows Server
* [Hands-On] Build com Agente Windows Self-Hosted
* [Hands-On] Instalando e Build com Agente no MacOS
* [Hands-On] Agentes Self-Hosted com YAML
* Teste 4: Quiz do Módulo
* Resumo do Módulo
  
## Seção 5: Releases - Básico
* Introdução ao Módulo
* Releases
* Princípios do Continuous Delivery
  * Processo Confiável Repetível
  * Automatize Tudo
  * Repositório em Tudo
  * Mais Complicado, Primeiro!
  * Qualidade Interna
  * Concluído = Liberado
  * Todos são Responsáveis
  * Melhoria Contínua
* Etapas para Entrega do nosso Software no Azure Pipelines Releases
* [Hands-On] Deploy do Release Pipeline com Azure App Service
* [Hands-On] Continuous Deployment Trigger
* [Hands-On] Agendamento de Deploy
* [Hands-On] Deploy em Multiplos Stages
* Aprovações Pré e Post Deployment
* [Hands-On] Aprovações no Release Pipelines
* Gates no Release Pipelines
* [Hands-On] Gates
* Testes 5: Quiz do Módulo
* Resumo do Módulo
  
## Seção 6: Releases - Deployment Group
* Introdução ao Módulo
* Agentes em Deployment Groups
* [Hands-On] Criando VM Windows Server no Azure
* [Hands-On] Configurando Deployment Group e associando a VM
* [Hands-On] Deploy utilizando IIS
* Teste 6: Quiz do Módulo
* Resumo do Módulo
  
## Seção 7: Releases - Deployment Patterns
* Introdução ao Módulo
* Deployment Patterns
* Estratégia de Implantação - Big Bang
* [Hands-On] Big Bang - Implantação via FTP Server
* Estratégia de Implantação Ramped
* Azure Load Balancer
* [Hands-On] Ramped - Criando VNET, NSG, Avalabity Set Load...
* [Hands-On] Ramped - Criando Maquinas Virtuais para Load Balancer
* [Hands-On] Ramped - Criando VMs Load Balancers
* [Hands-On] Ramped - Configurando IIS nas VMs Load Balancers
* [Hands-On] Ramped - Deployment Groups nas VMs com Load Balancers
* [Hands-On] Ramped - Criando a API
* [Hands-On] Ramped - Build e Release da Aplicação
* Estratégia de Implantação - Blue/Green
* Deployment Slots
* [Hands-On] Blue/Green - Criando Slots no App Services
* [Hands-On] Blue/Green - Build e Release da Aplicação
* Estrategia de Deploy - Canary
* [Hands-On] Canary - Criando App Service Slots
* [Hands-On] Canary - Build e Release Aplicação
* Estrategia de Deploy - A/B Testing
* Azure Traffic Manager
* [Hands-On] A/B Testing - Criando Azure App Services
* [Hands-On] A/B Testing - Criando Azure Traffic Manager
* [Hands-On] A/B Testing - Build e Release da Aplicação
* Comparativo dos Deployment Patterns
* Teste 7: Quiz do Módulo
* Resumo do Módulo
   
## Seção 8: Qualidade no CI/CD - SonarQube e Testes Unitários
* Introdução ao Módulo
* Testes de Unidade
* [Hands-On] Criando Projeto com Teste de Unidade
* [Hands-On] Build Pipeline - Validando Teste de Unidade
* Testes de Integração e Testes E2E
* [Hands-On] Criando Projeto com Testes de Integração (xUnit)
* [Hands-On] Build Pipeline Validando Teste de Integração
* SonarQube e SonarCloud
* [Hands-On] Verificação da Qualidade com SonarCloud
* Teste 8: Quiz do Módulo
* Resumo do Módulo
  
## Seção 9: Container no Azure Pipeline
* Introdução ao Módulo
* Docker Básico
* Principais Comandos Docker
    ```bash
      > docker version
      > docker images
      > docker image list
      > docker serch (parametro)
      > doker image pull (imagem)
      > docker run (nome da image)
      > docker run -it -p 8080:80 ngnix
      > docker ps
      > docker ps -a
      > docker stats (id ou alias)
      > docker inspect (id ou alias)
      > docker rmi (imagem)
      > docker exec (id ou nome)
      > docker start (id)
      > docker stop (id)
    ```
  * Comandos utilizados no curso:
    ```powershell
    > az acr login --name mvcdocker
    > docker pull mvcdocker.azurecr.io/imageacr:latest
    > docker run -d -p 2861:80 --name acrpipelines -e PORT=80 mvcdocker.azurecr.io/imageacr:latest
    > docker image list
    > docker container list
    > docker container rm ID container
    > docker stop ID container
    ```

* Docker no Azure e Azure DevOps
* [Hands-On] Aplicativo .NET com Container Docker
* Azure Container Registry (ACR)
* [Hands-On] ACR - Hospedando Docker Image no Azure
* [Hands-On] ACR - Usando a Imagem localmente
* [Hands-On] ACR - Publicando Imagem no Azure App Service for Containers
* [Hands-On] - Release App Service for Containers
* Azure Container Instances (ACI)
* [Hands-On] Criando Instancias com ACI
* Kubernets Básico
* Kubernetes, onde deve usar?
* Componentes do Kubernetes
* Azure Kubernetes Services (AKS)
* [Hands-On] AKS - Projeto API
* [Hands-On] AKS - Criando Serviços
* [Hands-On] AKS - Build YAML
* [Hands-On] Docker Agent Job - Agentes em Container Windows
* Teste 9: Quiz do Módulo
* Resumo do Módulo
  
## Seção 10: Infraestrutura como Código no Azure Pipeline
* Introdução ao Módulo
* Infraestrutura as a Code (IaC)
* ARM - Azure Resource Manager
* [Hands-On] ARM - Template ARM pelo Portal
* [Hands-On] ARM - Gerando Template
* [Hands-On] ARM - Parâmetros no Release Pipeline
* Terraform
* [Hands-On] Terraform - Criando Storage Account
* [Hands-On] Terraform - Release Pipeline
* [Hands-On] Terraform - Release Pipeline com App Service Storage
* Teste 10: Quiz do Módulo
* Resumo do Módulo
  
## Seção 11: Entrega Contínua do Banco de Dados no Azure
* Introdução ao Módulo
* Importância do C.I/C.D para o banco de dados
* Flyway
* [Hands-On] Flyway - Criando Azure SQL Database e Instalando Locamente
* [Hands-On] Flyway - Migração do banco de dados Locamente
* [Hands-On] Flyway - Migração do Banco de dAdos no Azure Pipelines
* SQL Server DACPAC
* [Hands-On] DACPAC - Criando projeto MVC .NET Core
* [Hands-On] DACPAC - Criando projeto Database
* [Hands-On] DACPAC - Publicando no Azure
* [Hands-On] DACPAC - Build e Release
* Teste 11: Quiz do Módulo
* Resumo do Módulo
## Seção 12: Montando Ambiente de Laboratório
* Ambiente de Laboratório
* [Tutorial] Instalando GIT
* [Tutorial] Instalando Visual Studio 2019
* [Tutorial] Instalando Visual Studio Code
* [Tutorial] Instalando DOcker no Windows
* [Tutorial] Instalação do Azure CLI