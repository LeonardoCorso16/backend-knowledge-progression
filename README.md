# Backend knowledge progression
Estudando e compartilhando todo o conhecimento referente as etapas do **[back-end roadmap](https://roadmap.sh/backend)** que foi criado por [@kamranahmedse](https://github.com/kamranahmedse).

# Internet

### > Como a internet funciona ?

​	A internet é uma rede global de computadores conectados entre si  que comunicam-se através de um conjunto de protocolos padronizados. Tudo começou na década de 1960 como um projeto pesquisa do exército Estadunidense, 20 anos depois o projeto evoluiu para uma infraestrutura pública  com o apoio de universidades públicas e empresas privadas. Ao longo do tempo surgiram novas tecnologia mas o modo como a internet funciona não mudou muito, continua sendo uma forma de conectar todos os computadores e garantir que eles encontrem sempre uma maneira de permanecerem conectados.

> Obs: A internet foi resultado de um outro projeto, conhecido como ARPANET.



#### Funcionamento de uma Rede Simples

​	Quando dois computadores precisam se comunicar, ambos precisam ser conectados fisicamente (cabo ethernet), ou sem fio (wifi, bluetooth). Essa rede não está limitada somente a dois computadores,  podem ser conectados quantos você desejar. Mas a partir  do momento em que a quantidade dos computadores vão aumentando o procedimento vai ficando mais complexo. Se por exemplo, você está tentando conectar dez computadores, você precisaria de  45 cabos com 9 plugues por computador. 



![Rede simples](https://mdn.mozillademos.org/files/8443/internet-schema-2.png)



​	Para solucionar o problema da quantidade de cabos foram criados os **roteadores**, que  possuem a exclusiva função de garantir que uma mensagem enviado de um determinado computador chegue ao computador de destino.

​	Se nossa rede de 10 computadores recebesse um roteador,  precisaríamos apenas de 10 cabos, um plug para cada computador  e um roteador com 10 plugues.



![Conexão simples com roteador](https://mdn.mozillademos.org/files/8445/internet-schema-3.png)



#### Uma Rede de Redes

​	Um único roteador não consegue suportar uma centenas ou milhares computadores, mas como os roteadores tratam-se de computadores também, então,  dois roteadores podem conectar-se entre si. Essa é um possibilidade que pode escalar infinitamente.

![Conexão de redes com redes](https://mdn.mozillademos.org/files/8449/internet-schema-5.png) 



​	A ideia de instalar cabos entre sua caso e o resto das casas ao redor do mundo não é algo possível, digamos assim.  Por isso a internet usa os cabos que existem dentro de sua casa, por exemplo a  conexão telefônica.  A infraestrutura de telefonia já faz o favor de conectar uma casa, com as outras casas do mundo, mas para que a nossa rede se conecte à  infraestrutura da telefonia, é necessário um equipamento  que é chamado de **modem**. O modem é responsável por transformar as informações da rede em informações administráveis pela  infraestrutura da telefonia e vice-versa. 

​	Só essa conexão entre o modem e a infraestrutura  da telefonia não é o suficiente, para que isso seja possível é necessário conectarmos a rede à um **Provedor de Serviço de Internet (ISP)**. Um ISP é um empresa que gerencia **roteadores** especiais que estão interligados e, que podem acessar outros ISPs.  A internet consiste em todas essa infraestrutura de redes.



![Conexão entre redes de ISPs diferentes](https://mdn.mozillademos.org/files/8453/internet-schema-7.png)



### > O que é HTTP ?

​	O _Protocolo de Transferência de Hipertexto_ (**HTTP**), é um protocolo de camada de aplicativo_¹_ para a transmissão de documentos de hipermídia, como o HTML.  Foi projetado para comunicação entre navegadores da web e servidores da web, mas também possuem outros fins. Esse protocolo sempre estará trabalhando em conjuntos com mais outros dois  protocolos, o **_Transmission Control Protocol_ (TCP)** que é responsável pela transferência das informações, e o **_Internet Protocol_ (IP)** que cuida dos encaminhamentos dos dados. 



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
   	* Mensagem

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



### > Navegadores e como funcionam ?

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

![Estrutura de um navegador](https://miro.medium.com/max/1322/1*52xFpyJc1ZQ-AN1Kc_zkwA.png)

​	Então, se digitarmos o endereço de uma página web no navegador o que é que acontece ?

 1. O Navegador vai para o servidor de DNS e encontra o endereço verdadeiro que o site esta hospedado.

 2. O navegador manda uma mensagem de requisição HTTP para o servidor, pedindo que ele envie uma cópia do site ao cliente. Esta mensagem e todos os outros dados enviados entre o cliente e o servidor são enviados pela sua conexão à internet usando TCP/IP.

 3. Se o servidor aprovar a requisição do cliente, o servidor enviará ao cliente uma mensagem "200 OK", e então começa a enviar os arquivos do site para o navegador como uma série de pequenos pedaços chamados pacotes de dados.

 4. O navegador monta os pequenos pedaços em um site completo e o mostra a você.

    

### > DNS e como ele funciona?

​	**Domain Name System (DNS)**, como o nome já diz, é um tipo de registro que contém nomes de sites e seus respectivos endereços IP  adepto. Os **verdadeiros** endereços web não são sequência de palavras fáceis de lembrar, e sim um endereço ip, parecido com isso: `54.240.200.15` . Então o  DNS baseia-se em uma abstração ao nível do usuário, que permite que páginas sejam encontradas na internet. Cada um deles é único para cada site.

​	Tratando-se de uma **Hospedagem**, o DNS atua em uma infraestrutura de subsistemas, composta por diferentes servidores que processam e transmitem informações uns para os outros.

> Obs: Um bom exemplo é comprar à um setor de Telemarketing, onde o atendente transfere o cliente para o setor especializado de acordo com cada requisição específica.

​	Como funciona...

1. **DNS Recursivo (recursor)** - Atua na primeira camada recebendo solicitações diretamente dos provedores de acesso, e então depois ele repassa essa informação para um subsistema mais específico.
2. **Root Nameserver** - Responsável pela organização e distribuição dos pedidos para o TLD.
3. **TLD Nameserver** - Responsável por unir os domínios de acordo com um termo específico que os padroniza, o sufixo: “.com” ou “.org”, por exemplo. Quando você digita “google.com”, essa requisição é direcionada para o TLD.com, que contém os nomes dessa categoria.
4. **SLD Nameserver** - Último registro que a requisição chega, que é o nome (exemplo "...google..."), o SLD é composto por uma lista com os nomes e IPs mais específicos.



> Obs: Os endereços existentes na internet possuem combinações extremamente numerosas, e esses servidores ajudam a catalogá-los.

![DNS em uma hospedagem](https://narodev.com/wp-content/uploads/2019/04/DS.png)



### > O que é Hospedagem ?

​	Quando um provedor de hospedagem (HostGator) aloca espaço em um servidor da web para que um site armazene seus arquivos, isso significa que ele está hospedando um site. A hospedagem na Web disponibiliza os arquivos que compõem um site e que possibilita a visualização online. Todo site está hospedado em um servidor.



![Funcionamento de um webserver](https://mdn.mozillademos.org/files/8659/web-server.svg)



#### Servidor Web Estático

​	Consiste em um computador (hardware) com um servidor HTTP (software). É chamado "estático" porque o servidor envia seus arquivos **tal como foram criados e armazenados (hospedados)** ao navegador.



#### Servidor Web Dinâmico

​	Consiste em um servidor web estático com software adicional, mais comumente um servidor de aplicações e um banco de dados. É chamado "dinâmico" porque o servidor de aplicações **atualiza os arquivos hospedados antes de enviá-los** ao navegador através do servidor HTTP.





## Conhecimento Básico de Frontend 



## SO e Conhecimentos Gerais



## Aprenda uma linguagem (C#, Ruby)

### Csharp

### Ruby



## Sistema de Controle de Versão

### Uso básico do Git

### Serviço de hospedagem de repositório



## Bancos de Dados Relacionais (MySQL, PostgreSQL)



## Bancos de Dados NoSQL (MongoDB)



## Mais sobre Bancos de Dados

### ORMs

### ACID

### Transactions

### N+1 Problem

### Database Normalization

### Indexes and how they work



## Aprenda sobre APIs

### Authentication

* **OAuth**
* **Basic Authentication**
* **Token Authentication**

### REST

### JSON APIs



## Caching

### CDN

### Server Side

* **Redis**
* **Memcached**

### Client Side



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



## Teste

### Integration Testing

### Unit Testing

### Functional Testing



## CI/CD



## Princípios de Design e Desenvolvimento

### SOLID

### KISS

### YAGNI

### DRY



## Padrões de Arquitetura

### Monolithic Apps

### Microservices

### SOA

### CQRS and Event Sourcing

### Serverless



## Motores de Busca

### Elasticsearch

### Solr



## Message Brokers

### Kafka



## Conteinerização vs Virtualização

### Docker 



## GraphQL





## Bancos de Dados orientados a grafos



## WebSockets



## Servidores Web





