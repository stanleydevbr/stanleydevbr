# AWS Developer Associate

## AWS API Gateway: Integrando e protegendo serviços
* Introdução
* Overview da arquitetura
* AWS API Gateway
* Politica e role de acesso ao bucket
    - Criação de bucket
    - IAM:
        - Create Policy: 
            - Serviço: S3
            - Actions: All permission
            - Resources: 
                - Add ARN (nome do bucket) marcar [x] any
                - Review (nome: nomeapp_s3_acesso_bucket)
        - Roles:
            - Criar nova role
                - Serviço que usa a role: Api Gateway
                - role name: NameApp-ROLE-S3_Acesso_ao_Bucket
                - Abrir a role >> Anexar a policy

* Controlando o acesso
    >> Policy >> Roles
* Importando a API

* Criando APIs no API Gateway
* Consolidando o conhecimento
* O que apreendi:

## Deploy da API
* O Método DELTE
* Métodos HTTP para o S3
* Deploy da API
* URL da API
* Testando a API
* Consolidando o seus conhecimento
    Chegou a hora de você seguir todos os passos realizados por mim durante esta aula. Caso já tenha feito, excelente. Se ainda não, seguem brevemente os passos principais:
        Na sua API adicione um novo método DELETE abaixo do /{item}
        Use a integração AWS Service e configure o seu bucket no S3
        Sobrescreve o PATH e coloque nome_do_seu_bucket/{item} (repare que definimos um URL Path Paramenter)
        Não esqueça de colar o ARN do seu role
        Adicione um URL PATH Paramenter com o name item e Mapped from method.request.path.item:
        Adicione uma resposta JSON no Integration Response, por exemplo: {"message":"Arquivo removido"}
        Crie um novo Deploy (na API -> Action - Deploy API)
        No Stage Name pode colocar dev
        Copie a URL do POST
        Teste com ferramenta HTTP, por exemplo Postman
        Algumas fotos estão nesse download
        Altere a URL para conter o nome da foto (no lugar de {item})
        Escolha o método POST
        Não esquece de definir o cabeçalho Content-type
        Na aba Body escolhe binary e selecione a foto para enviar
        Teste também o método DELETE
* O que aprendemos?


