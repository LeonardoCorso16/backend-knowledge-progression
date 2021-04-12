# Backend knowledge progression

Estudando e compartilhando todo o conhecimento referente as etapas do **[back-end roadmap](https://roadmap.sh/backend)** que foi criado por [@kamranahmedse](https://github.com/kamranahmedse).

# Sumário
<details>
<summary>Mostrar capítulos</summary>

1.  [Internet](https://github.com/causticroot/backend-knowledge-progression#internet)
2. [Conhecimento Basico de Frontend](https://github.com/causticroot/backend-knowledge-progression#conhecimento-b%C3%A1sico-de-frontend)
3. [SO e Conhecimentos Gerais](https://github.com/causticroot/backend-knowledge-progression#so-e-conhecimentos-gerais) 
4. [Aprenda uma linguagem](https://github.com/causticroot/backend-knowledge-progression#aprenda-uma-linguagem-c-ruby)   
5. [Sistema de Controle de Versão](https://github.com/causticroot/backend-knowledge-progression#sistema-de-controle-de-vers%C3%A3o)  
6. [Bancos de Dados Relacionais](https://github.com/causticroot/backend-knowledge-progression#bancos-de-dados-relacionais-mysql-postgresql)       
7. [Bancos de Dados NoSQL](https://github.com/causticroot/backend-knowledge-progression#bancos-de-dados-nosql-mongodb) 
8. [Mais sobre Bancos de Dados](https://github.com/causticroot/backend-knowledge-progression#mais-sobre-bancos-de-dados) 
9. [Aprenda sobre APIs](https://github.com/causticroot/backend-knowledge-progression#mais-sobre-bancos-de-dados) 
10. [Caching](https://github.com/causticroot/backend-knowledge-progression#caching) 
11. [Conhecimentos de segurança web](https://github.com/causticroot/backend-knowledge-progression#conhecimento-de-seguran%C3%A7a-web) 
12. [Teste](https://github.com/causticroot/backend-knowledge-progression#teste) 
13. [CI/CD](https://github.com/causticroot/backend-knowledge-progression#cicd) 
14. [Principios de Design e Desenvolvimento](https://github.com/causticroot/backend-knowledge-progression#princ%C3%ADpios-de-design-e-desenvolvimento) 
15. [Padrões de Arquitetura](https://github.com/causticroot/backend-knowledge-progression#padr%C3%B5es-de-arquitetura) 
16. [Motores de Busca](https://github.com/causticroot/backend-knowledge-progression#motores-de-busca) 
17. [Message Brokers](https://github.com/causticroot/backend-knowledge-progression#message-brokers) 
18. [Conteinerização vs Virtualização](https://github.com/causticroot/backend-knowledge-progression#conteineriza%C3%A7%C3%A3o-vs-virtualiza%C3%A7%C3%A3o) 
19. [GraphQL](https://github.com/causticroot/backend-knowledge-progression#graphql) 
20. [Bancos de Dados orientados a grafos](https://github.com/causticroot/backend-knowledge-progression#bancos-de-dados-orientados-a-grafos) 
21. [WebSockets](https://github.com/causticroot/backend-knowledge-progression#websockets) 
22. [Servidores Web](https://github.com/causticroot/backend-knowledge-progression#servidores-web)
</details>


# Internet

### Como a internet funciona

​	A internet é uma rede global de computadores conectados entre si  que comunicam-se através de um conjunto de protocolos padronizados. Tudo começou na década de 1960 como um projeto pesquisa do exército Estadunidense, 20 anos depois o projeto evoluiu para uma infraestrutura pública  com o apoio de universidades públicas e empresas privadas. Ao longo do tempo surgiram novas tecnologia mas o modo como a internet funciona não mudou muito, continua sendo uma forma de conectar todos os computadores e garantir que eles encontrem sempre uma maneira de permanecerem conectados.

> Obs: A internet foi resultado de um outro projeto, conhecido como ARPANET.



#### Funcionamento de uma Rede Simples

​	Quando dois computadores precisam se comunicar, ambos precisam ser conectados fisicamente (cabo ethernet), ou sem fio (wifi, bluetooth). Essa rede não está limitada somente a dois computadores,  podem ser conectados quantos você desejar. Mas a partir  do momento em que a quantidade dos computadores vão aumentando o procedimento vai ficando mais complexo. Se por exemplo, você está tentando conectar dez computadores, você precisaria de  45 cabos com 9 plugues por computador. 

​	Para solucionar o problema da quantidade de cabos foram criados os **roteadores**, que  possuem a exclusiva função de garantir que uma mensagem enviado de um determinado computador chegue ao computador de destino.

​	Se nossa rede de 10 computadores recebesse um roteador,  precisaríamos apenas de 10 cabos, um plug para cada computador  e um roteador com 10 plugues.



#### Uma Rede de Redes

​	Um único roteador não consegue suportar uma centenas ou milhares computadores, mas como os roteadores tratam-se de computadores também, então,  dois roteadores podem conectar-se entre si. Essa é um possibilidade que pode escalar infinitamente.

 	A ideia de instalar cabos entre sua caso e o resto das casas ao redor do mundo não é algo possível, digamos assim.  Por isso a internet usa os cabos que existem dentro de sua casa, por exemplo a  conexão telefônica.  A infraestrutura de telefonia já faz o favor de conectar uma casa, com as outras casas do mundo, mas para que a nossa rede se conecte à  infraestrutura da telefonia, é necessário um equipamento  que é chamado de **modem**. O modem é responsável por transformar as informações da rede em informações administráveis pela  infraestrutura da telefonia e vice-versa. 

​	Só essa conexão entre o modem e a infraestrutura  da telefonia não é o suficiente, para que isso seja possível é necessário conectarmos a rede à um **Provedor de Serviço de Internet (ISP)**. Um ISP é um empresa que gerencia **roteadores** especiais que estão interligados e, que podem acessar outros ISPs.  A internet consiste em todas essa infraestrutura de redes.



### O que é HTTP

​	O _Protocolo de Transferência de Hipertexto_ (**HTTP**), é um protocolo de camada de aplicativo_¹_ para a transmissão de documentos de hipermídia, como o HTML.  Foi projetado para comunicação entre navegadores da web e servidores da web, mas também possuem outros fins. Esse protocolo sempre estará trabalhando em conjuntos com mais outros dois  protocolos, o **_Transmission Control Protocol_ (TCP)** que é responsável pela transferência das informações, e o **_Internet Protocol_ (IP)** que cuida dos encaminhamentos dos dados. 



####  Principais métodos HTTP

* **GET - ** Solicita a representação de um recurso. Passando o estado atual do objeto  naquele momento.
* **POST - ** Solicita a criação de um recurso.
* **DELETE - ** Solicita a exclusão de um recurso.
* **PUT - ** Solicita a atualização de um recurso.



> Obs¹: Um Camada de Aplicativo,  é uma camada de abstração que específica  os protocolos de comunicação compartilhados  e os métodos de interface usados pelos hosts  em uma rede de comunicação. A abstração da camada de aplicação  é usada em ambos os modelos padrão de rede de computadores, TCP/IP e o modelo OSI.

​	

​	O HTTP segue um modelo clássico de **cliente-servidor**, com um cliente abrindo  uma conexão para fazer uma solicitação  e aguardando até receber uma resposta. HTTP é um protocolo sem estado, ou seja, o servidor não mantém nenhum dado entre duas solicitações.  O protocolo HTTP trabalha em um modelo de **request** (pedido) e **response** (resposta),  exemplo, um navegador realiza um acesso à um site então ele faz um **pedido** para o servidor que devolve uma **resposta**  geralmente em HTML, após esse processo de pedido e resposta a conexão é encerrada, sendo necessário repetir  o ciclo cada vez fez que um pedido é realizado (conexão não persistente).

#### **Request**

* Está relacionado à o pedido feito ao servidor.

 * Formado pelas seguintes entidades:
    * Linha de pedido
       * **Identificador do método:** Tipo de ação que esperamos do servidor (ex: GET, POST).
       * **URI do Recurso:**  Endereço no qual será enviado o pedido (ex: /index).
       * **Versão do protocolo**
    * Cabeçalho (Local para passar informações adicionais sobre a requisição, ex: Transfer-Encoding, Cache control...)
      	* **Cabeçalho Geral**
      	* **Cabeçalho de Requisição**
      	* **Cabeçalho de Entidades**
      	* **Mensagem**

![Requisição http](https://documentation.help/DogeTool-HTTP-Requests-vt/http_requestmessageexample.png)





#### **Response**

 * Está relacionado à resposta retornada pelo servidor
 * Formado pelas seguintes entidades:
    * Linha de Status:
       * **Código Numérico do Status:** Número  em 3 dígitos que corresponde como  o pedido foi condicionado  no servidor. As respostas são agrupadas em 5 classes:
          1. Respostas de informação (`100`-`199`),
         2. Respostas de sucesso (`200`-`299`),
         3. Redirecionamentos (`300`-`399`)
         4. Erros do cliente (`400`-`499`)
         5. Erros do servidor (`500`-`599`).
       * **Texto Associado ao Status**
       * **Versão do protocolo**
    * Cabeçalho
    * Mensagem

![](https://documentation.help/DogeTool-HTTP-Requests-vt/http_responsemessageexample.png)



### Navegadores e como funcionam ?

​	A principal funcionalidade do navegador é apresentar um recurso da web que foi escolhido por um cliente por meio de uma request ao servidor, depois exibi-lo na janela do navegador. Esse "recurso" geralmente trata-se de um documento HTML, mas pode ser qualquer outro tipo de arquivo. O local desses recursos é especificado pelo usuário através de uma URI.

#### Estrutura de um navegador

​	Um navegador é composto pelo os seguintes componentes :

1. **User Interface** - Todas as áreas do display do navegador, exceto a janela principal responsável pela visualização da página requisitada.

2. **Browser Engine** - Faz a triagem das ações entre a interface do usuário e o mecanismo de  de renderização.

3. **Rendering Engine** - Exibe o conteúdo solicitado.

4. **Networking** -  Responsável pelas chamadas de rede, como solicitações HTTP. Poussi a interface independente da plataforma e sub-implementação para cada plataforma.

5. **Javascript Interpreter** - Analisa e executa o código javascript.

6. **UI Backend** - Exibe uma interface genérica que não é específica da plataforma. Sob a interface, utiliza os métodos da interface do usuário do sistema operacional.

7. **Data Persistence** - Refere-se à uma camada persistente, onde o navegador guarda diversos dados no disco rígido, como cookies. Definido como "banco de dados da web".

   

​	**Então, se digitarmos o endereço de uma página web no navegador o que é que acontece ?**



 1. O Navegador vai para o servidor de DNS e encontra o endereço verdadeiro que o site esta hospedado.

 2. O navegador manda uma mensagem de requisição HTTP para o servidor, pedindo que ele envie uma cópia do site ao cliente. Esta mensagem e todos os outros dados enviados entre o cliente e o servidor são enviados pela sua conexão à internet usando TCP/IP.

 3. Se o servidor aprovar a requisição do cliente, o servidor enviará ao cliente uma mensagem "200 OK", e então começa a enviar os arquivos do site para o navegador como uma série de pequenos pedaços chamados pacotes de dados.

 4. O navegador monta os pequenos pedaços em um site completo e o mostra a você.

    

### DNS e como ele funciona?

​	**Domain Name System (DNS)**, como o nome já diz, é um tipo de registro que contém nomes de sites e seus respectivos endereços IP  adepto. Os **verdadeiros** endereços web não são sequência de palavras fáceis de lembrar, e sim um endereço ip, parecido com isso: `54.240.200.15` . Então o  DNS baseia-se em uma abstração ao nível do usuário, que permite que páginas sejam encontradas na internet. Cada um deles é único para cada site.

​	Tratando-se de uma **Hospedagem**, o DNS atua em uma infraestrutura de subsistemas, composta por diferentes servidores que processam e transmitem informações uns para os outros.

> Obs: Um bom exemplo é comprar à um setor de Telemarketing, onde o atendente transfere o cliente para o setor especializado de acordo com cada requisição específica.

​	Como funciona...

1. **DNS Recursivo (recursor)** - Atua na primeira camada recebendo solicitações diretamente dos provedores de acesso, e então depois ele repassa essa informação para um subsistema mais específico.
2. **Root Nameserver** - Responsável pela organização e distribuição dos pedidos para o TLD.
3. **TLD Nameserver** - Responsável por unir os domínios de acordo com um termo específico que os padroniza, o sufixo: “.com” ou “.org”, por exemplo. Quando você digita “google.com”, essa requisição é direcionada para o TLD.com, que contém os nomes dessa categoria.
4. **SLD Nameserver** - Último registro que a requisição chega, que é o nome (exemplo "...google..."), o SLD é composto por uma lista com os nomes e IPs mais específicos.



> Obs: Os endereços existentes na internet possuem combinações extremamente numerosas, e esses servidores ajudam a catalogá-los.
>
> 

### O que é Hospedagem ?

​	Quando um provedor de hospedagem (HostGator) aloca espaço em um servidor da web para que um site armazene seus arquivos, isso significa que ele está hospedando um site. A hospedagem na Web disponibiliza os arquivos que compõem um site e que possibilita a visualização online. Todo site está hospedado em um servidor.



#### Servidor Web Estático

​	Consiste em um computador (hardware) com um servidor HTTP (software). É chamado "estático" porque o servidor envia seus arquivos **tal como foram criados e armazenados (hospedados)** ao navegador.



#### Servidor Web Dinâmico

​	Consiste em um servidor web estático com software adicional, mais comumente um servidor de aplicações e um banco de dados. É chamado "dinâmico" porque o servidor de aplicações **atualiza os arquivos hospedados antes de enviá-los** ao navegador através do servidor HTTP.

[Back to top](#)

## Conhecimento Básico de Frontend 



[Back to top](#)

## SO e Conhecimentos Gerais



[Back to top](#)

## Aprenda uma linguagem (C#, Ruby)

### Csharp

### Ruby



[Back to top](#)

## Sistema de Controle de Versão

### Uso básico do Git

### Serviço de hospedagem de repositório



[Back to top](#)

## Bancos de Dados Relacionais (MySQL, PostgreSQL)



[Back to top](#)

## Bancos de Dados NoSQL (MongoDB)



[Back to top](#)

## Mais sobre Bancos de Dados

### ORMs



### ACID



### Transactions



### N+1 Problem



### Database Normalization



### Indexes and how they work

#### O que é um índice

Índices nos bancos de dados são utilizados para facilitar a busca de informações em uma tabela com o menor número possível de operações de leituras, tornando assim a busca mais rápida e eficiente.



**Dicas a serem consideradas na hora de criar índices**

*Campos para serem indexados afim de ganhar desempenho*

* Chaves primárias;
* Chaves estrangerias;
* Colunas acessadas por ranges (between);
* Campos utilizados em groupBy ou orderBy;

*Campos que não devem ser indexados*

* Campos dos tipos: text, image, decimais;
* Campos calculados;
* Campos com alta cardinalidade (Masculino ou Feminino);

#### Mantendo a integridade dos índices

Tabelas que sofrem muitas alterações tais como *Insert, Update* e *Delete*, refletem essas modificações nos índices, pois isso provoca espaços em brancos nas páginas da tabela. Estes espaços não utilizados refletem maior espaço em disco o que acarreta um desperdício de tempo ao percorrer a estrutura do índice.

Para resolver esse problema é necessário manter a integridade dos índices. A opção `REORGANIZE` remove somente a fragmentação do nível folha e a opção  `REBUILD` reconstrói todos os níveis do índice.



```sql
ALTER INDEX {nome_indice | ALL } ON REBUILD
ALTER INDEX {nome_indice | ALL } ON REORGANIZE
```



#### Métodos de acesso aos índices e tables

Os acessos aos dados das tabelas e índices podem ser realizados de duas formas `SEEK`  ou `SCAN`.

* **SCAN** - busca em todos os elementos da estrutura(tabela ou índice). É utilizado quando não possui índices que não atendam a instrução de SELECT ou quando a quantidade de registros que a query retorna  é grande.
* **SEEK** - busca binária nos elementos de um índice. É utilizado quando existe um índice que é adequado e a quantidade de registros retornados é pequena.

**Sendo assim, é possível executar as seguintes operações para acesso nas tabelas/índices:**

* **TABLE SCAN** - Busca todos os elementos da tabela de forma sequencial.
* **INDEX SCAN** - Busca em todos os elementos de um índice nonclustered, de forma sequencial.
* **INDEX SEEK** - Busca binária num índice noclustered.
* **CLUSTERED INDEX SCAN** - Busca em todos os elementos de um índice clustered, de forma sequencial.
* **INDEX SEEK** - Busca binária em um índice clustered.



[Back to top](#)

## Aprenda sobre APIs

### O que é API 

Aplication Programming Interface, ou Interface de Programação de Aplicativo, são conjuntos de rotinas documentados e disponibilizados  por uma aplicação para que outras aplicações possam consumir suas funcionalidades.

Quando  uma aplicação web disponibiliza um conjunto de rotinas e padrões através de serviços web podemos chamar esse conjunto de API.



### Web Services

Serviços web ou web services, são soluções para aplicações se comunicarem independente de linguagem, softwares e hardwares utilizados. Inicialmente os serviços web foram criado para troca de mensagens utilizando a linguagem XML sobre o protocolo HTTP sendo identificado por URI(Uniform Resource Identifier). Praticamente deduz-se que web services são API's que se comunicam por meio de redes através do protocolo HTTP.

> Todos Web Service é uma API, mas nem toda API é um Web Service.





#### O que é SOAP 

Simple Object Access Protocol (SOAP), ou Protocolo de acesso à objetos simples, é um protocolo baseado em XML para acessar web services principalmente por HTTP,  mas possui um meio de transporte genérico, portanto suporta outros protocolos. Desenvolvido para para facilitar as integrações entre  aplicações, pode-se dizer que SOAP é uma definição de como os web services se comunicam.

> #### XML
>
> * XML - Extensible Markup Language.
> * Linguagem de marcação criada  na década de 90 pela W3C.
> * Objetivo de facilitar a separação de conteúdo.
> * Sem limitações de criação de tags.
> * Linguagem comum para integrações entre aplicações.



#### Estrutura SOAP Message

* **SOAP Envelope :**  É o primeiro elemento do  documento e é utiliMensagemzado para encapsular toda a menssagem SOAP.
* **SOAP Header :** É o elemento que possui informações de atributos e metadados da requisição.
* **SOAP Body :** É o elemento que possui os detalhes da mensagem.



#### WSDL e XSD

**Web Services Description Language (WSDL)**,  usado para descrever web services, funciona como um contrato do serviço. A descrição é feita em um documento XML, onde é descrito o serviço, especificações de acesso, operações e métodos.

**XML Schema Definition (XSD)**, é um schema no formato XML usado para definir a estrutura de dados que será validada no XML. Funciona como uma documentação de como deve ser montado o  SOAP Message que será enviado através de  Web Service



### Authentication

* **OAuth**
* **Basic Authentication**
* **Token Authentication**



### REST

#### O que é REST

Representational State Transfer, ou Transferência Representacional de Estado, é um estilo de arquitetura  de software que define a implearquitetura monolíticamentação  de um web service. Aceita formatos como  XML, JSON  ou outros. REST utiliza os métodos HTTP para representar a operação a ser realizada em um determinado recurso.

> REST não é um protocolo, e sim um design  de arquitetura para web services.



#### Vantagens em se utilizar REST

* Permite integrações entre aplicações e também cliente e servidor em  páginas web  e aplicações.

* Utilizar métodos HTTP para definir a operação que está sendo passada.

* Arquitetura de fácil compreensão.

  

### JSON

JavaScript Object Notation, é uma formatação leve utilizada para troca de mensagens entre sistemas, usa-se de uma estrutura de chave e valor e também de listas ordenadas.

<p align="center">
    <img src="https://img.mandic.com.br/blog/2019/09/JSON-formato.png" alt="estrutura json"/>
</p>


[Back to top](#)

## Caching

### CDN

### Server Side

* **Redis**
* **Memcached**

### Client Side



[Back to top](#)

## Conhecimento de Segurança Web

### **MD5 and why not to use it**

### SHA Family

### Scrypt

### Bcrypt

### HTTPS

### Content Security Policy

### CORS

### SSL/TLS

### OWASP Security Risks



[Back to top](#)

## Teste

### Integration Testing

### Unit Testing

### Functional Testing



[Back to top](#)

## CI/CD



[Back to top](#)

## Princípios de Design e Desenvolvimento

### **SOLID**

​	SOLID é um conjunto de princípios (princípios de Projeto de classes)  que propõe uma maneira para desenvolvimento sob uma perspectiva da orientação a objetos, visando à gestão de dependências  e combate aos sintomas do apodrecimento do código-fonte, permeando a construção de melhores códigos do ponto de vista do Projeto de construção de software. 

​	S.O.L.I.D é uma concatenação das inicias dos nomes dos cincos princípios abordados, sendo estes: 

* ***S* ingle esponsibility -** princípio da responsabilidade única.
* ***O* pen closed-** princípio Aberto/Fechado.
* ***L* iskov substitution -** princípio da substituição de Liskov.
* ***I* nterface segregation -** princípio de segregação de interfaces.
* ***D* ependency inversion -** princípio da inversão de dependência.

##### Single responsibility 

​	O princípio da responsabilidade única tem como base a coesão. Coesão mede a capacidade da classe em executar uma única função. Classes com alto índice de coesão são mais fáceis de se entender e, também , mais fáceis de manter. Se uma classe tiver mais de uma razão para mudar, isso significa que as responsabilidades que causam essas mudanças devem ser separadas em outras classes. Alterações em uma responsabilidade podem prejudicar ou inibir a habilidade da classe em lidar com outras responsabilidades. Esse tipo de acoplamento leva a projeto mais frágeis que "quebram" de maneiras inesperadas quando alterados.

**Exemplo:**

```csharp
public class Retangulo()
{
    //Aplicação gráfica (desenha um retângulo na tela)
    public void Desenhar()
    {
        //desenha
    }
}

public class RetanguloGeometrico()
{
    //Aplicação de computção gemétrica (calcula o valor da área do retângulo)
    public double CalcularArea()
    {
        return 0;
    }
}
```

O princípio da responsabilidade única é um dos princípios mais simples porém um dos mais difíceis de  pratica corretamente. Agrupar responsabilidades é algo natural do ser humano e, encontrar e separar essa responsabilidades umas das outras é a parte da essência do Projeto de software.

##### **Open closed**

​	O princípios do aberto/fechado é o mais importante entre todos os da categoria  de princípios de classes, já que todos os demais de certa forma, são derivados de  *Open closed*. Este princípios surgiu  no trabalho de *Bertran Meyer*, que é reconhecido como autoridade no paradigma de orientação a objetos.

​	Este princípio afirma que  quando uma mudança simples em um sistema acarreta um efeito cascata de mudanças para os módulos dependentes, o sistema exibe atributos indesejados que são ligados ao mau projeto. O sistema se torna frágil, rígido, imprevisível e não reutilizável. O open closed ataca esse estado de uma maneira muito direta, dizendo para o Projeto criar módulos que nunca mudem. Quando os requisitos mudam, o comportamento da classe afetada deve ser alterada pela adição de código, e não pela alteração de código já existente e que funcione.

### KISS

### YAGNI

### DRY



[Back to top](#)

## Padrões de Arquitetura

### Monolithic Apps

A **arquitetura monolítica**, descreve uma única aplicação de software em camadas no qual a interface de usuário e código de acesso  aos dados são combinado em um único programa  a partir de uma única plataforma.  Sendo assim uma aplicação autônoma e independente  de outras aplicações.

<p align="center">
    <img src="https://raw.githubusercontent.com/jeffhsta/fundamentos_arquitetura/master/monolito.png"\>
</p>



#### Pros e Contra

**Pros**

* Baixa complexidade
* Monitoramento simplificado

**Contra**

* Stack única
* Compartilhamento de recursos
* Acoplamento
* Escalabilidade complexa



### Microservices

A **arquitetura de micro serviços** é utilizada para desenvolver uma aplicação como um conjunto de pequenos **serviços**, cada um funcionando em seu próprio processo. Cada **serviço** é desenvolvido em torno de um conjunto de regras de negócio específico, e é implementado de forma independente.

##### Microservice #1

<p align="center">
    <img src="https://raw.githubusercontent.com/jeffhsta/fundamentos_arquitetura/master/microservicos1.png"\>
</p>



##### Microservice #2

<p align="center">
    <img src="https://raw.githubusercontent.com/jeffhsta/fundamentos_arquitetura/master/microservicos2.png"\>
</p>



##### Microservice #3

<p align="center">
    <img src="https://raw.githubusercontent.com/jeffhsta/fundamentos_arquitetura/master/microservicos3.png"\>
</p>



#### Pros e Contra

**Pros**

* Stack dinâmica
* Escalabilidade simples
* Desacoplamento (Message broker #2)
* Menor complexidade (gerenciador de pipeline #3)

**Contra**

* Stack única
* Compartilhamento de recursos
* Acoplamento
* Escalabilidade complexa
* Monitoramento complexo (Message broker #2)
* Provisionamento complexo (Message Broker #2)
* Dependência do gerenciador de pipeline (gerenciador de pipeline #3)



### SOA

### CQRS and Event Sourcing

### Serverless



[Back to top](#)

## Motores de Busca

### Elasticsearch

### Solr



[Back to top](#)

## Message Brokers

O message broker é um intermediário entre as conexões realizadas e os serviços, permite identificar o motivo de um determinado serviço ter sido incapaz de responder no momento de uma requisição, aumentando a segurança  e evitando o retorno de condições indevidas ao sistema.

### Kafka



[Back to top](#)

## Conteinerização vs Virtualização

### Docker 



[Back to top](#)

## GraphQL





[Back to top](#)

## Bancos de Dados orientados a grafos



[Back to top](#)

## WebSockets



[Back to top](#)

## Servidores Web



[Back to top](#)





