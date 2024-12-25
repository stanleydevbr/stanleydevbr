## Abstract Factory
O principal objetivo do padrão Abstract Factory é fornecer uma interface para criar famílias de objetos relacionados sem especificar a class concreta.

Enquanto o Factory Method adia a criação da instância para as subclasses, o objetivo do Abstract Factory é criar famílias de objetos relacionados.

## Comparando Factory Method x Abstract Method
| Factory Method | Abstract Method |
|---|--|
| Expõe um método ao cliente para criar os objetos | Contém um ou mais métodos de fábrica para criar uma família de objetos relacionados.
| Usa herança e subclasses para definir o objeto a ser criado| Usa composição para deletar a responsabilidade de criar objetos de outra classe.
| É usado para criar um produto | É usado para criar famílias de produtos relacionados|

## Façade
Introdução aos padrões estruturais
* os padrões estruturais descrevem como objetos e classes podem ser combinados para compor estruturas maiores;
* Os padrões estruturais facilitam o design de software por meio da identificação de maneiras mais simples de perceber ou demonstrar relacionamentos entre os objetos ou classes;

Exemplos de padrões estruturais:
* Padrão Adapter (adaptador) - adapta uma interface a outr para que as expectativas do cliente sejam atendidas; procura combinar interfaces de classes diferentes conforme as necessidades do cliente;

* Padrão Bridge (ponte) - desacopla a interface de um objeto de sua implementação para que ambos possam trabalhar de forma independente;

* Padrão Decorator (Decorador) - define responsabilidades adicionais para um objeto em tempo de execução ou dinamicamente; podemos adicionar determinados atributos aos objetos com uma interface;

* Padrão Façade (Fachada) - ocuta as complexidades da estrutura interna de um objeto oferecendo uma interface ao cliente para que ele possa acessar o sistema de forma simplificada;

O padrão façade faz o seguinte: 
* Oferece uma interface unificada para um conjunto de interfaces em um subsistema e define uma interface de alto nível que ajuda o cliente a usar o subsistema de forma fácil;
* O Façade procura fazer a representação de um subsistema compexo com um único objeto de interface. Ele não encapsula o subsistema, mas, na verdade, combina os subsistemas subjacentes;
* Promove o desacoplamento da implementação com vários clientes;

### Princípio do conhecimento mínimo
O princípio do conhecimento mínimo nos orienta no sentido de reduzir as interações entre os objetos a apenas alguns amigos que sejam próximos a você.

Isso sgnifica que:
* Quando fizermos o design de um sistema, para todo objeto criado, devemos observar o número de classes com que essa classe interage e o modo como a interação ocorre;
* Seguindo este princípio, certifique-se de evitar situação em que haja muitas classes criadas que estejam altamente acopladas umas às outras;
* Se houver muitas dependências entre as classes, o sistema será difícil de manter. Qualquer mudança em uma parte do sistema poderá resultar em alterações não intencionais em outras partes, o que significa que o sistema estrá exposto a regressões, e isso deve ser evitado;


## Padrão Proxy
De forma gera, o Proxy é um sistema que serve de intermediário entre o solicitante, chamado de seeker, e o provedor, chamado de provider.

O solicitante é que faz a requisição, e o provedor entrega os recursos em resposta à requisição.

No mundo da internet, podemos relacionar o conceito de Proxy com Servidor Proxy. 

Quando os clientes fazem uma requisição ao site, inicialmente se conectam com um servidor proxy solicitando recursos, por exemplo uma página web.

O servidor proxy internamente avalia esta requisição, envia para um servidor apropriado e recebe a resposta, que é então entregue ao cliente.

No contexto de padrões de projetos, Proxy é uma classe que atua como uma interface para objetos reais.
Os objetos podem ser de vários tipos, como conexões de rede, objetos grandes em memória e arquivos, dentre outros.

Em resumo, Proxy é um agente que encapsula o objeto que está realmente servindo, podendo inclusive oferecer funcionalidades adicionais ao objeto que ele encapsula sem alterar o código do objeto.

Tipos de proxy: 
* Proxy Virtual
* Proxy Remoto
* Proxy de Proteção
* Proxy Inteligente

### Proxy Virtual
O proxy virtual funciona como um "placeholder" para objetos que são muito pesados para instanciar.
Por exemplo, se você quiser carregar uma imagem grande em seu site, esta requisição exigirá bastante tempo de carregamento.
Geralmente criamos um ícone de placeholder (valor inicial estático) na página web sugerindo quei ali existe uma imagem, no entanto a imagem só será carregada quando o usuário realmente clicar no ícone, evitando assim o custo de carregar uma imagem pesada na memória.
Desta forma, nos proxies virtuais, o objeto real é criado apenas quando o cliente faz sua primeira requisição ou seu primeiro acesso ao objeto.

### Proxy Remoto
O proxy remoto oferece uma representação local de um objeto real que está em um servidor remoto ou em um espaço de endereçamento diferente.
Por exemplo, imagine que você quer implementar um sistema de monitoração para a sua aplicação que tem vários servidores de banco de dados, servidores de tarefas Celery e servidores de caching, entre outros.
Se quisermos monitorar a utilização de CPU e de disco nestes servidores, precisaremos de um objeto que esteja disponível no contexto em que a aplicação de monitoramento é executada, mas que possa executar comandos remotos para obter os valores dos parâmetros.
Em casos assim, ter um objeto proxy remoto que seja uma representação local do objeto remoto ajudaria.

### Proxy de proteção
Este proxy controla o acesso às partes sensíveis de um objeto real.
Por exemplo, em sistemas distríbuidos, as aplicações web têm vários serviços que operam em conjunto para oferecer funcionalidades.
Em sistemas como esses, um serviço de autenticação atua como um servidor de proxy de proteção, responsável pela autenticação e pela autorização.
Neste caso, o proxy internamente ajuda na proteção das funcionalidades essenciais do site verificando agentes não reconhecidos ou não autorizadas.
Desta forma, o objeto substituto verifica se quem faz a chamada tem as permissões de acesso necessárias para encaminhar a requisição.

### Proxy Inteligente
Os proxies inteligientes interpõe ações adicionais quando um objeto é acessado.
Por exemplo, considere que haja um componente com ponto central único em um sistema que armazene dados em um local centralizado.
Geralmente, um componente como este é chamado por vários serviços diferentes para que eles possam concluir suas tarefas, e pode resultar em problemas com recuros compartilhados.
Em vez de os serviços chamarem diretamente o componente, um proxy inteligente é encarregado por verificar se o objeto real esta travado (sendo executado) antes de ser acessado a fim de garantir que nenhum outro objeto possa alterá-lo.


### Vantagens do padrão proxy
* Os proxies podem ajudar a melhorar o desempenho da aplicação ao fazer caching de objetos pesados ou, geralmente, de objetos acessados com frequência;

* Os proxies também autorizam o acesso a um objeto real; portanto este padrão auxilia na delegação somente se as permissões estiverem corretas;

* Os proxies remotos também facilitam a interação com servidores remotos, que podem funcionar como conexões de rede e de bancos de dados, além de poderem ser usados para monitorar sistemas

## Comparando o padrão proxy com padrão façade
Tanto o padrão Façade quanto o padrão proxy são padrões de projeto estruturais. 
Eles são semelhantes no sentido que ambos têm um objeto proxy/fachada na ferente de objetos reais.
As diferenças, na verdade, estão na intenção ou no propósito dos padrões.

| Padrão Proxy | Padrão Façade |
|--|--|
|Oferece um substituto (placeholder) para outro objeto a fim de controlar o acesso a ele| Oferece uma interface para subsistemas grandes de classes|
|Um objeto proxy tem a mesma interface do objeto alvo e armazena referências a esses objetos| Minimiza a comunicação e as dependências entre subsistemas|
|Atua como um intermediário entre o cliente e o objeto encapsulado| Um objeto Façade oferece uma interface única e simplificada.|


## Padrões de projetos comportamentais

Em seções passadas aprendemos que os Padrões de Criação funcionam com base no modo como os objetos podem ser criados.
Vimos também que os Padrões estruturais determinam o design da estrutura de objetos e classes para que estes possam trabalhar em conjunto a fim de alcançar resultados mais amplos, tendo como foco principal a simplificação da estrutura das aplicações.

Os padrões comportamentais, como o próprio nome sugere, têm como foco as responsabilidades de um objeto.
Eles lidam com a interação entre objetos para alcançar funcionalidades mais complexas.
Este padrão sugere ainda que, embora os objetos devam ser capazes de interagir uns com os outros eles devem manter um baixo acoplamento.

O padrão Observer é um dos padrões comportamentais mais simples que existem.

## Padrão observer
No padrão de projeto Observer um objeto mantém uma lista de dependentes de modo que este objeto possa notificar todos os dependentes acerca de mudanças pelas quais ele passa usando qualquer um dos métodos definidos pelo objeto.

No mundo das aplicações distribuídas, vários serviços interagem uns com os outros para exectuar uma operação mais complexa que o usuário queira fazer.

Os serviços podem realizar várias operações, mas a operação que eles executam é diretamente ou altamente dependente do estado dos objetos do serviço com o qual a interação ocorre.

## Contexto do padrão observer
Imagine um blog onde diversas pessoas postam diariamente diversos textos em tópicos diversos.

Pessoas, como eu ou você, podem se cadastrar no blog e se inscrever em determinados tópicos.

Quando um novo post for realizado sobre o tópico na qual você está inscrito você receberá uma notificação informando a nova postagem.

Por baixo dos panos, temos neste sistema o padrão observer sendo utilizado.

Neste nosso exemplo, o blog será o Objeto que mantém uma lista de dependentes (inscritos) e a qualquer mudança serão notificados pois os inscritos estão "observando" as mudanças no objeto observado.

## Objetivos do padrão observer.
* Define uma dependência de um-para-muitos (one-to-many entre os objetos, de modo que qualquer mudança em um objeto será notificada aos demais objetos dependentes automanticamente.
* Encapsula o componente "objeto"

## Caso de uso do padrão observer
* Na implementação de um serviço de eventos em sistemas distríbuidos;
* Na implementação de um sistema de notícias;
* No mercado de ações;

### Tipos de notificação do padrão observer
Existem duas maneiras diferentes de notificar os "observadores" das mudanças que ocorreram no objeto obsrvado. Elas podem ser classificadas como modelo push e pull.

Modelo pull: No modelo pull, o padrão observer desempenha um papel ativo da seguinte forma:
* O assunto/tópico faz um broadcast (espalhamento) para todos os inscritos registrados quando há uma mudança;
* O obsrvador é responsável por obter as mudanças, ou seja, o assinante deve buscar os dados quando houver uma alteração;
* O modelo pull não é eficiente, pois envolve dois passos, sendo o primeiro passo para o assunto/tópico notificar o observador e o segundo passo para o observador obter os dados necessários do assunto/tópico;

Modelo push: no modelo push, o assunto/tópico é quem desempenha um papel dominante, conforme:
* De modo diferente do modelo pull, as mudanças são envidas pelo assunto/tópico ao observador;
* Neste modelo, o assunto/tópico pode enviar informações detalhadas ao observador (mesmo que não seja necessário). Isso pode resultar em tempos de resposta mais lentos quando uma grande quantidade de dados é enviada pelo assunto/tópico, mas não é realmente usada pelo observador.
* Somente os dados necessários devem ser enviados pelo assunto/tópico para que o desempenho seja melhor.

### Baixo acoplamento do padrão observer
Em programação orientada a objetos, o baixo acoplamento é um princípio de design de software importate e que deve ser usado em aplicaçães.

O propósito principal deste princípio é esforçar-se para ter designs com baixo acomplamento, ou seja, baixa dependência, entre objetos que interagem uns com os outros.

O acomplamento refere-se ao grau de conhecimento que um objeto tem sobre outro com o qual interage.

Designs com baixo acoplamento nos permitem construir sistemas orientados a objetos flexíveis, capazes de lidar com mudanças, pois reduzem a dependência entre vários objetos.

A arquitetura com baixo acomplamento garante as seguintes características:
* Reduz o risco de que uma mudança em um elemento possa gerar impacto imprevisto em outros elementos;
* Simplifica os testes, a manuntenção e a resolução de problemas;
* O sistema pode ser facilmente separado em elementos definidos;


O padrão observer possibilita um design de objetos em que o Assunto/Tópico e o Observador têm baixo acomplamento pois: 
* A única informação que o Assunto/Tópico deve ter sobre o Observador é que ele implementa uma determinada interface. Ele não precisa conhecer as classes dos observadores;
* Qualquer novo observador poderá ser adicionado a qualquer momento;
* O Assunto/Tópico não precisa ser nem um pouco modificado para adicionar qualquer novo observador;
* O Assunto/Tòpico ou observadores não estão "amarrados" e podem ser usados de modo independente. Desta forma, o obsrvador poderá ser reutilizado em qualquer outro lugar caso necessário;
* Alterações no Assunto/Tópico ou no observador não afetarão um ao outro. Como ambos são independentes, isto é, têm baixo acoplamento, eles são livres para fazer suas próprias alterações.

### Vantagens do padrão observer:
* Oferece suporte para o princípo do baixo acoplamento entre objetos que interajam uns com os outros;
* Permite enviar dados a outro objetos de modo eficiente, sem qualquer mudança nas classes Assunto/Tópico ou Observer;
* Os Observers podem ser adicionados/removidos a qualquer momento;

### Desvantagens do padrão observer
* A interface Observer deve ser implementada pelos Observers, o que envolve herança. Não há opção para usar composição, pois a interface Observer não pode ser instanciada;
* Se não for implementado corretamente, o Observer pode acrescentar complexidade e levar a problemas imprevistos de desempenho;
* Em uma aplicação de software, às veses, as notificações podem não ser confiáveis e resultar em condições de concorrência (race conditions) ou inconsistências;

## Padrão Command
Já aprendemos que os padrões de projetos comportamentais têm como foco as responsabilidades de um objeto, pois eles lidam com a interação entre objetos para alcançar funcionalidades mais complexas.
O padrão Command é um padrão de projeto comportamental, em que um objeto é usado para encapuslar todas as informações necessárias para executar uma ação ou disparar um evento posteriormente. Estas informações incluem:
* O nome do método
* Um objeto que seja dono do método
* Valores para os parâmetros do método

### Compreendendo o padrão Command
O padrão command trabalha com os seguintes termos:
* Command > Um objeto command conhece os objetos Receiver e invoca um método deste objeto;
* Receiver > Os valores dos parâmetros do método receptor (receiver) são armazenados no objeto Command;
* Invoke > O chamado ou invocador (invoker) sabe como executar um comando;
* Client > O cliente cria o objeto Command e define o seu receptor

### Principais objetivos do padrão command
* Encapsular uma requisição com um objeto;
* Possibilitar a parametrização dos clientes com diferentes requisições;
* Permitir salvar as rquisições em uma fila;
* Oferecer uma callback orientada a objeto.

### O padrão command pode ser usado em diversos casos incluindo:
* Parametrizar objetos de acordo com a ação a ser executada;
* Adicionar ações em uma fila e executar as requisições em pontos diferentes;
* Criar uma estrutura para operações de alto nível baseada em operações menores;

### Vantagens do padrão command
* Desacopla as classes que invocam a operação do objeto;
* Permite criar uma sequência de comandos oferecendo um sistema de fila;
* Podemos facilmente adicionar um novo comando sem alterar o código existente;

### Desvantagens do padrão command
* Há um número elevado de classes e objetos trabalhando em conjunto para alcançar um objetivo. Como desenvolvedor de aplicações, você deve tomar cuidado para desenvolver essas classes corretamente;

* Todo comando individual é uma classe ComandoConcreto que aumenta o volume de classes para implementação e manutenção;


## Padrão de projeto Template Method
Aprendemos em aulas anteriores que os padrões de projetos comportamentais têm como foco as responsabilidades de um objeto, pois eles lidam com a interação entre objetos para alcançar funcionalidades mais complexas.

O padrão Template Method é um padrão de projeto comportamental que define o esqueleto do programa ou um altoritmo em um método chamado Método template.

Você pode, por exemplo, definir os passos para preparar uma bebida como um algorimo em um Método Template.
O padrão Template Method também ajuda a redefinir ou personalizar os passos do algoritimo adiando a implementação de alguns desses passos para as subclasses. Ou seja, as subclasses podem redefinir o seu próprio comportamento.

Desta forma uma subclasse poderia fazer uso do Método Template para preparar uma bebida e preparar chá enquanto outra subclasse poderia usar o mesmo Método Template para preparar café já que ambas são bebidas.

Vale destacar que a alteração dos passos nas subclasses não exerce impacto na estrutura do algoritmo original.

Desta forma, o recurso das subclasses pode sobrescrever no padrão Tempalte Method permite a ciração de diferentes comportamentos ou algoritmos.

No contexto de desenvolvimento de software, uma classe abstrata é usada para definir os passos do algoritmo. Esses passos são conhecidos como operações primitivas no contexto do padrão Template Method.

Estas operações são definidas como métodos abstratos e o Método Template define o algoritmo.

Uma classes concreta que for subclasse desta classe abstrata implemtna os passos do algoritmo específico para a subclasse

O padrão template method é usado nos seguintes casos:
* Quando vários algoritmos ou classes implementam uma lógica semelhante ou idêntica;
* Quando a implementação dos algoritmos em subclasses ajuda a reduzir a duplicidade de código;
* Quando vários algoritmos podem ser definidos ao deixar que as subclasses implementem o comportamento usando o recurso de subrescrita.

### Exemplo da preparação da bebida:
|Café|Chá|
|---|---|
|Ferva a água|Ferva a água|
|Passe a água fervente pelo pó de café| Coloque o saquinho de chá|
|Coloque o café em uma xícara| Coloque o chá em uma xícara |
|Adicione açúcar ou leite na xícara| Adicione limão ao chá |
|Misture, e o café estará pronto| Misture, e o chá estará pronto|

### Principais objetivos do padrão template method são: 
* Definir o esqueleto de um algoritmo com operações primitivas;
* Redefinir determinadas operações na subclasse sem alterar a estrutura do algoritmo;
* Reutilizar o código e evitar esforço duplicados;
* Tirar proveito de interfaces ou implementações comuns;


## Hooks
No padrão Template Method, um hook (gancho) é um método declarado na classe abstrata, que em geral, recebe uma implementação default.

A ideia por traz dos hooks é dar a uma subclasse a capacidade de fazer um uso padrão do algoritmo sempre que for necessário.

Um exemplo de utilização de hooks seria, no caso da nossa implementação Bedbida, acidionar açucar ou alguma outra especiária, conforme o desejo do cliente.

No caso da agência de viagens, pense que poderiamos ter turistas mais idosos que talvez não queiram sair em todos os três dias da viagem, pois poderão se cansar facilmente.

Neste caso podemos desenvolver um hook que garantirá que o segundo dia seja mais leve, o que significa que o turista poderá ir a lugares próximos e retornar ao plano normal no segundo dia.

### Principio Hollywood e o Template Method

O princípio de Hollywood é um principio de desgn de software que diz:

Não ligue para nós; nós ligaremos para você.

Isto é proveniente da filosofia de Hollywood, segundo a qual as produtoras de filmes e séries ligam para os atores caso haja algum papel para eles.

No mundo da Orientação a Objetos, permitimos que componentes de baixo nível se associem aos sistema usando o princípio de Hollywood.

No entanto, os componentes de alto nível determinam como e quando o sistemas de baixo nível são necessários.

Ou seja, os componentes de alto nível tratam os componentes de baixo nível assim:

não ligue para nós; nós ligaremos pra você.

Isso se relaciona ao padrão Template Method no sentido de que é a class abstrata de alto nível que organiza os passos para definir o algoritmo.

Com base no algoritmo, as classes de baixo nível são solicitadas e definidas a implementação concreta dos passos.


### Vantagens do padrão Template Method
* Uma das principais vantagens é que não há duplicação de código;
* A reutilização de código ocorre normalmente já que o padrão Template Method utiliza herança e não composição. Somente alguns métodos precisam ser sobrescritos.
* A flexibilidade permite que as subclasses decidam como implementar os passos do algoritmo.

### Desvantatens do padrão Template Method
* Debugar a aplicação e compreender a sequência do fluxo do padrão Template Method às vezes pode ser confuso. Você pode acabar implementando um método que não deveria ser implementado ou deixando de implementar um método abstrato. Vale a pena documentar bem o código e realizar tratamento de erros para evitar problemas;

* A manutenção dos componentes de alto ou baixo nível pode causar problemas na implementação;


## Padrões de projetos compostos
Confoem definido pela GoF, um padrão composto combina dois ou mais padrões em uma solução que resolve um problema recorrente ou genérico.

Ou seja, uma padrão composto não é um conjunto de padrões que trabalha em conjunto, mas sim uma solução geral para um problema.

### MVC
O padrão de projeto Model-View-Controller, ou MVC, é um padrão de softwsare para implementar interfaces de usuário com uma arquitetura que pode ser facilmente modificada e mantida.

Basicamente, o padrão MVC diz respeito á separação de aplicação em três partes básicas:
* Model (modelo)
* View (visão);
* Controller (Controlador).

Estas três partes são interconectadas e ajudam a separar os modelos como a informação é representada de forma como ela é apresentada.

### Como funciona o padrão MVC
O model (modelo) representa os dados e a lógica de negócio (como a informação é armazenada e consultada).
A view (visão) nada mais é que a representação (como ela é apresentada) dos dados.
O controller (controlador) é a "cola" que une ambos, ou seja, é a parte que direciona o modelo e a visão para que se comportem de determinada maneira de acordo com as necessiades de um usuário.

É importante observar que a visão e o controlador são independetes do modelo, mas não o contrário.
Isso ocorre porque um usuário esta preocupado com os dados, Desta forma podemos trabalhar com o model de forma independente, este é o aspecto principal do padrão MVC.

As aplicações web são exemplos clássicos para o padrão MVC. Você clica em um botão, algumas operações ocorrem e você passa a ver o que desejva na página.

Como isso ocorre?
* Voc~e e o usuário e interage com a visão. A visão e a página web apresentada. Você clica nos botões e ela informa ao controlador o que deve ser feito.
* O controlador obtém a entrada da visão e a envia ao modelo. O modelo é manipulado com base nas ações do usuário.
* O controlador também pode pedir à visão para mudar conforme a ação recebida do usuário, por exemplo, alterar os botões, apresentar elementos adicionais na interface, etc.
* O modelo notifica a alteração de estado à visão. Isso pode ser feito com base em alterações internas ou por acionamento externos, como cliques em um botão.
* A visão então exibe o estado que ela obtém diretamente o modelo.

## Padrão de projeto State
Os padrões de projeto comportamentais têm como foco as responsabilidades de um objeto, pois eles lidam com a interação entre objetos para alcançar funcionalidades mais complexas.

O padrão de projeto State (estado) é um padrão comportamental que, às vezes, também é chamado de padrão de objetos para estados.

Neste padrão, um objeto pode encapsular vários comportamentos de acordo com o seu estado interno.

O padrão State também é considerado como uma maneira de um objeto alterar seu comportamento em tempo de execução.

Compreendendo o padrão de projeto State
* State: É considerada uma interface que encapsula o comportamento do objeto. Esse comportamento está associado ao estado do objeto.
* StateConcreto: É uma subclasse que implementa a interface State. Esta subclasse implementa o comportamento propriamente dito associado ao estado particular do objeto.
* Context: Define a interface de interesse dos clientes. COntext também mantém uma instância da subclasse StateConcreto que, internamente, define a implementação do estado particular do objeto.

## Vantagens do padrão State:
* No padrão State, o comportamento de um objeto é resultado da função de seu estado, e o comportamento muda em tempo de execução de acordo com este estado. Isso elimina a dependência lógica condicional de if/else ou de switch/case (para linguagens que possui).

* Com o padrão State, as vantagens de implementar um comportamento polifórmico são evidentes, além de ser mais fácil adicionar estados para dar suporte a novos comportamentos.

* O padrão de projeto State também melhora a coesão, pois comportamentos específicos de estado são agregados nas classes StateConcreta, que são colocados em um só lugar no código.

* Com o padrão State é muito fácil acrescentar um comportamento simplesmente adicionando mais uma classe StateConcreta. Desta forma aumenta a flexibilidade, permitindo estender o comportamento da aplicação e facilitando a manutenção do código em geral.


## Desvantagens do padrão State:
* Grande aumento do número de classes. Como todo estado deve ser definido com a ajuda de StateConcreta, há uma chance de acabarmos escrevendo muito mais classes com uma pequena funcionalidade.

* Com a introdução de cada novo comportamento, a classe Context deve ser atualizada para lidar com o novo comportamento. Isso deixa o comportamento de Context mais frágil a cada novo comportamento adicionado.


## Antipadrões
Os princípios de design de software representam um conjunto de regras ou diretrizes que ajudam os desenvolvedores a tomar decisões no nível de design.

Existem quatro características em um design de software ruim:
* Imóvel: Uma aplicação é desenvolvida de modo que se torne muito difícil de ser reutilizada;
* Rígido: Uma aplicação é desenvolvida de modo que qualquer alteração pequena possa resultar na mudança de muitas partes do software;
* Frágil: Qualquer mudança na aplicação atual resulta em falhas no sistema existente com muita facilidade;
* Viscoso: Mudanças são feitas pelo desenvolvedor no código ou no próprio ambiente para evitar mudanças difíceis no nível da arquitetura;

Estas características, se forem aplicadas, resultam em soluções que não deveriam ser implementadas na arquitetura ou no desenvolvimento de software.

Um antipadrão é o resultado de uma solução ineficiente e contraproducente para problemas recorrentes.

Imagine que você está desenvolvendo um software e se depare com um problema de design. 
Você decide então solucionar este problema.

Porém o que acontece se a solução tiver um impacto negativo no design e causar qualquer problema de desempenho na aplicação?

Os antipadrões são processos e implementações defeituosos e comuns em aplicações de software.

Os antipadrões podem ser resultado de:
* Um desenvolvedor que desconhece boas práticas de desenvolvimento de software;
* Um desenvolvedor não aplica os padrões de projeto de forma correta;

Os antipadrões, apesar de tudo, podem se mostrar vantajosos pois:
* Nos ajudam a reconhecer problemas recorrentes no mercado de software e buscar soluções detalhadas para a maioria destes problemas, fazendo bom uso dos padrões de projeto;
* Nos ajudam a pensar em ferramentas para reconhecer os problemas e determinar suas causas;
* Nos ajudam a descrever as medidas que podem ser tomadas em vários níveis para melhorar a aplicação e a arquitetura;

Os antipadrões podem ser classificados em duas categorias principais:
* Antipadrões no desenvolvimento de software;
* Antipadrões na arquitetura de software;

