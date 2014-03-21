---
layout:         post
title:          "Alberto Souza sobre o Play Framework"
subject:        "Play Framework"
date:           2014-03-21 14:00:00
categories:     java scala play framework
comments:       true
description:    um papo com Alberto Souza sobre o Play Framework
interviewee_name:   Alberto Souza
interviewee_avatar: ../images/avatar/alberto-souza-120.jpeg
interviewee_avatar_major: ../images/avatar/alberto-souza-120.jpeg
interviewee_bio:    Alberto trabalha na Caelum como instrutor e desenvolvedor. Não é apaixonado por nenhuma linguagem, gosta apenas de tentar usar a melhor ferramenta para determinado problema. Atualmente mantém projetos usando Scala, Ruby e Java.
interviewee_twitter: https://twitter.com/alberto_souza
interviewee_facebook: https://www.facebook.com/alberto.souza.332
interviewee_blog: http://alots.wordpress.com/
interviewee_googleplus: https://plus.google.com/101139135933113985213
interviewee_github: https://github.com/asouza

---


## Alberto, poderia se apresentar e falar do seu envolvimento com o Play Framework?

Claro! Me chamo Alberto Souza e trabalho a 4 anos na [Caelum](http://www.caelum.com.br/). Lá eu sou um dos responsáveis por toda parte relacionada às aulas e também colaborador de alguns projetos. Participei do inicio do desenvolvimento do [Alura](http://www.alura.com.br/) e já há um bom tempo faço parte do time do [VRaptor](http://vraptor.caelum.com.br/pt/). Ainda na versão 3 eu comecei o plugin para possibilitar a integração com o CDI e na versão 4, junto com todo o time, participei da reconstrução do framework para uma total integração com o CDI e tudo relacionado ao JAVAEE 7.

Para finalizar, e talvez essa seja  a parte mais importante porque está relacionada a entrevista, eu comecei alguns projetos usando o [Play Framework](http://www.playframework.com/) e atualmente tem 2 que usamos bastante. Um serviço que nos possibilita gerar as apostilas sem precisar instalar nada na máquina do usuário e outro que nos ajuda nas marcações das aulas da Caelum.

## O que diferencia o Play dos outros frameworks existentes no mercado?

Faço parte do time que não gosta de perder tempo com nada que não seja relativo ao problema que estou resolvendo e isso me levou a apreciar bastante o Ruby on Rails, que para mim é referência em produtividade dentre os frameworks que existem no mercado para todas as linguagens. O Play tenta trazer justamente essa produtividade para o mundo Java e ele usa algumas táticas para atingir o objetivo. Uma primeira decisão importante foi a de ser um framework que contempla todas as camadas do nosso projeto, chamado de Full Stack. Não preciso me preocupar com qual tecnologia de view, persistencia, mensageria, agendamento, consumo de webservices, web sockets, server sent events, servidor web,  etc. Ele já tomou essa decisão e em 90% dos casos as aplicações vão viver bem com isso. Ainda em relação a essa primeira decisão, ele inclusive se preocupou com uma parte muito importante que é a de testes. Fazer testes de integração e aceitação ficou muito mais fácil, já que ele possui APIs prontas para isso.

A segunda decisão foi a de possibilitar alterações contínuas sem a necessidade de reload da aplicação. O programador pode alterar uma classe, arquivo de rotas, views, arquivos de mensagens e configurações sem a necessidade de ficar esperando o servidor recarregar a aplicação. Para os programadores do mundo Java e Scala, como eu, isso faz muita diferença.

A terceira decisão foi a de ter um console onde eu posso rodar tarefas comuns as aplicações como: testes, compilação, execução do servidor e geração do arquivo de deploy da aplicação.

A quarta e talvez mais importante para um nicho de aplicações, é que ele foi concebido com a idéia de ser totalmente assíncrono. E isso não fica apenas no core do framework, as APIs que são expostas para os programadores também foram implementadas pensando nisso. Com isso, utilizando apenas um servidor (sem necessidade de load balancers), a aplicação consegue responder a muito mais requests simultâneos. Fiz até um post sobre isso no [meu blog](http://alots.wordpress.com/2014/02/18/play-um-framework-pensado-para-voce-e-sua-empresa/).

## Onde você considera que o Play ainda precisa melhorar?

O principal trabalho não é no framework em si e sim na ferramenta utilizada para build, no caso o SBT. Ele é a responsável por realizar o trabalho de compilação contínua e ainda precisa melhorar. Eles conseguiram grandes avanços na versão 2.2.2 utilizada em conjunto com o sbt 0.13.2-M2. O anuncio foi feito no [grupo de usuários](https://groups.google.com/forum/#!topic/play-framework/S_-wYW5Tcvw). 

## Você publicou o livro Play Framework na Prática. Fale a respeito dele.

O [livro](https://leanpub.com/playframeworknapratica) foi a maneira que encontrei de tentar fazer com que mais pessoas conheçam e pensem em usar o Play. Acho que consegui abordar tudo que é necessário para a pessoa criar uma nova aplicação do zero. Ele vai desde o ínicio bem básico e necessário para o uso da ferramenta até tópicos como necessidade de balanceamento de carga e criação de plugins. Até agora o feedback das pessoas que leram foi positivo. Estou acabando os últimos dois capítulos e devo lança-los em breve. Daqui a uns meses deve sair a versão em Scala também, esse pela [Casa do Código](http://www.casadocodigo.com.br/). 

## Descreva a comunidade em torno do Play e fale como está a aceitação do framework.

Acho que está ficando bem forte. O forum no google groups é bem movimentado, tanto que respondo dúvidas diariamente. A [Typesafe](http://typesafe.com/) tem feito um ótimo trabalho em divulgação, colocando o Play em diversas conferências. Inclusive, neste ano, houve um evento exclusivo sobre o framework, a [PingConf](http://www.ping-conf.com/). Empresas importantes como [Linkedin](http://engineering.linkedin.com/play/play-framework-linkedin) e [Coursera](http://www.typesafe.com/blog/making-online-education-accessible-with-typesafe) já usam fortemente. Aqui no Brasil ainda está crescendo, mas acho que no médio prazo vai ser um concorrente forte.

## Algumas considerações finais?

Para quem quiser aprender mais sobre o framework, existem algumas fontes interessantes. Existe o meu [livro](https://leanpub.com/playframeworknapratica), escrito em português e disponível na [Leanpub](https://leanpub.com/playframeworknapratica), o [meu blog pessoal](http://alots.wordpress.com) onde tenho postado semanalmente sobre alguma característica do framework, o [grupo de usuários do framework](https://groups.google.com/forum/#!forum/play-framework). Para finalizar, [essa discussão](https://groups.google.com/forum/#!topic/play-framework/3N6PuGXW-bA) no forum traz o blog de vários dos desenvolvedores.

## Seu ambiente de desenvolvimento

  - **Hardware:** *Macbook Pro, 2.3 Ghz Intel Core 5, 8 GB de memória*
  - **Sistema Operacional:** *Mac OS X*
  - **Editor/IDE:** *Eclipse e Textmate*
  - **Linguagem preferida:** *Scala, Java e Ruby*
  - **Controle de versÃ£o:** *Git*
  - **Browser:** *Chrome*
