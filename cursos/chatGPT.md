# Como utilizar o ChatGPT como Compiloto de Programação
## Introdução
* Copiloto de código
* Regras do jogo

## Pair Programming with GPT
* Solicitando unidades com conjuntos de regras
```cmd
Crie uma função que retorne somente os números de um conteúdo alfanúmerico
{REGRAS}
> Linguagem: .NET CORE 
> Input: code: string
> Output: numberId: number
> Aplique boas praticas de Clean Code
> No final,Explique o que foi feito
```
* Crie funções explicitadas
```cmd
Implemente a lógica da função abaixo
//passa coordenadas de latitude e longitude e retorna código de cep do local
public function long GetZipCode(latitude: long, longitude: long){

}

{REGRAS}
> Linguagem: .NET CORE 
> Aplique boas praticas de Clean Code
> No final,Explique o que foi feito
```
* Criando testes unitários com GPT
```cmd
Implemente testes unitários para função abaixo e/ou selecionada
{REGRAS}
> Linguagem: .NET Core
> Utilize a biblioteca: XUNIT
> Crie pelo menos 3 unidades de teste
```

* Desacoplando códigos
```cmd
refatore o código abaixo e/ou selecionado aplicando os conceitos de clean code e Single Responsability

{REGRAS}
> Linguagem: .NET Core
> Crie um código que seja Testavel
> Implemente pelo menos 3 testes utilizando a XUnit
```
* Entendendo Racional de códigos
```cmd
Me explique o que essa função abaixo e/ou selecionada .NET Core esta fazendo e adicione comentários
```
* Convertendo código e tornando-os mais amigáveis
```cmd
Converta o código abaixo e/ou selecionado em [Linguagem X] para [Linguagem Y]
```

## Documentações profissionais e instântaneas
* Criando documentações generalistas automáticas
```chatGPT
faça uma documentação da função abaixo e/ou selecionada
```
* Criando documentações de modelos específicos
```chatGPT
Crie uma documentação para função abaixo e/ou selecionada, no mesmo modelo desta documentação:
{modelo doc}
{função}
```
* Comentários baseados em templates
```chatGPT
Adicione o modelo de documentação abaixo, na função abaixo e/ou selecionada
{MODELO}
{FUNÇÃO}
```
## Utilidades
* GPT as a MENTOR
```chatGPT
Me ajude a criar este projeto abaixo, me indicando como fazer e quais bibliotecaq utilizar para construir na nameira mais prática
{REGRAS}
> Linguagem: .NET Core
> Plataforma: Multplataforma
> Crie no padrão de Clean Code

{FEATURES}
> Realizar o upload de uma imagem
> Validar o número de cartão de credito de um usuário
```
```
Implemente uma camada de login utilizando JWT com .NET Core neste mesmo projeto.
```
* Criando uma cheat-sheet
```
crie uma cheat-sheet para os principais comandos PowerShell
crie uma cheat-sheet para os principais comandos GIT
crie uma cheat-sheet para os principais comandos CSS
crie uma cheat-sheet para os principais comandos .NET Core
```
## DIO - Geração de conteúdo
Checklist de para gerar artigos de qualidade: 
> Definir o assunto
> Titulo chamativo: headline
> Imagem de capa chamativa
> Blocos do artigo
> Postar o artigo com um call to action

Pergunta: 
Crie 10 headlines para nomes de artigos sobre o assunto Angular - Diretivas

Ferramentas: 
lexica.art

## Prompts ricos para gerar artigos: 
### Assunto
Angular - Diretivas
### Titulo
Diretivas estruturais versus diretivas de atributo: Qual usar no Angular?
## Capa: 
Feito com Lexica.Art e Power Point

## Blocos
- O que são diretivas no Angular
- O que são diretivas estruturais
    - Cite exemplos com código de diretivas estruturais
- O que são diretivas atributos
    - Cite exemplos com código de diretivas atributos
- Faça um call to action para as minhas redes sócias
- Coloque 3 hashtags que façam sentido        
Ilustrações de capa: gerada pela lexica.art
Conteúdo gerado por: ChatGPT e revisões humanas

{REGRAS}
> Comporte-se como um escritor de artigos tech front-end e escreva  o artigo atendendo as regras abiaxo:
> No máximo 5 linhas por blocos de explicação
> Me explique de maneira informal, como se eu fosse uma criança de 10 anos
> Os blocos que serão criados estão abaixo:
    - O que são diretivas no Angular
    - O que são diretivas estruturais
        - Cite exemplos com código de diretivas estruturais
    - O que são diretivas atributos
        - Cite exemplos com código de diretivas atributos
    - Faça um call to action para as minhas redes sócias
    - Coloque 3 hashtags que façam sentido        