---
layout:         post
title:          "Francisco Souza sobre Go"
subject:        "Go"
date:           2014-02-04 08:00:00
categories:     go
comments:       true
description:    Um Papo com Francisco Souza sobre Go
interviewee_name:   Francisco Souza
interviewee_avatar: https://0.gravatar.com/avatar/a5e001826b5112a5c02f706569b93a3c?d=https%3A%2F%2Fidenticons.github.com%2Fb2047f78905b996ea25a379c25d54312.png&r=x&s=440
interviewee_avatar_major: https://0.gravatar.com/avatar/a5e001826b5112a5c02f706569b93a3c?d=https%3A%2F%2Fidenticons.github.com%2Fb2047f78905b996ea25a379c25d54312.png&r=x&s=440
interviewee_bio:    Francisco Souza é desenvolvedor na globo.com, onde ajuda a construir a plataforma de cloud computing Tsuru. É apaixonado por desenvolvimento de softwares, entusiasta em Python, Django, Go e software livre, associado à Associação Python Brasil e membro do cobrateam.
interviewee_twitter: https://twitter.com/franciscosouza
interviewee_facebook: https://www.facebook.com/franciscossouza
interviewee_blog: http://f.souza.cc/
interviewee_googleplus: https://plus.google.com/+FranciscoSouza
interviewee_bitbucket: https://bitbucket.org/fsouza
interviewee_github: https://github.com/fsouza

---


## Francisco, fale do seu envolvimento e sua experiência com Go.

Quando a linguagem foi anunciada publicamente em 2009, eu dei uma olhada rápida e segui minha vida, pois achei que não tinha muito a ver comigo. Comecei a brincar com [Go][go] no fim de 2010, por conta própria e por causa de um crescente interesse em concorrência e paralelismo. Na época, fiz uma ou outra coisa, mas foi em 2011 que comecei a me aprofundar mais na linguagem.

Inicialmente, comecei os estudos usando o Project Euler, depois comecei a me aventurar com bibliotecas e comecei a contribuir com a linguagem no fim de 2011. Em 2012, entrei para o time do [Tsuru][tsuru], um PaaS open source desenvolvido na [Globo.com](http://globo.com). Todo o código do Tsuru é em Go, então venho trabalhando com Go diariamente há quase 2 anos.

## Quais as principais vantagens em utilizar a linguagem?

A linguagem é extremamente simples e focada na escalabilidade do processo de desenvolvimento. É desenvolvimento na escala do Google. A forma como o compilador aplica regras que em outras linguagens são apenas convenções facilita em muito o processo de desenvolvimento com grandes times.

A maturidade da linguagem é outro ponto inquestionável: apesar de ser uma linguagem nova, é extremamente madura. E isso é fácil de explicar: embora seja nova, Go foi construída por pessoas com uma vasta experiência em diversos ramos, especialmente compiladores, sistemas operacionais e concorrência.

A abordagem para concorrência, paralelismo, deployment e compilação faz com que a linguagem sirva para resolver problemas complexos de uma maneira simples. O próprio Tsuru seria bem mais complexo se não fosse a linguagem.

Brad Fitzpatrick, criador do memcached e core developer do Go, sempre quis criar um serviço de storage pessoal distribuído, e afirma que com Go ele pode simplesmente tirar essa ideia do papel e criar o camlistore.

## E suas limitações? A ausência de algumas funcionalidades consideradas importantes em outras linguagens, como por exemplo o tratamento de exceção e a herança, fazem falta?

Go é uma linguagem muito bem pensada. Desta forma, a ausência de algumas funcionalidades é sempre uma opção de design muito bem justificada. Entretanto, é comum ver pessoas cobrando por funcionalidades bastante comuns em outras linguagens, como tratamento de exceção e generics.

É possível encontrar no [FAQ da linguagem](http://golang.org/doc/faq) algumas respostas para "por que Go não tem a minha feature preferida da minha linguagem X?". Lá será possível encontrar as justificativas para a linguagem não ter exceções, herança ou generics.

Como em qualquer linguagem, as features fazem falta até que você se acostume com a ausência delas, e entenda o "jeito Go" de resolver os problemas. O jeito Go tende a ser mais simples, e se encaixa muito melhor com a linguagem, então o segredo é aprender qualquer linguagem com a guarda baixa.

## Em que tipo de aplicações o uso de Go é indicado?

Aplicações que se beneficiam de concorrência e paralelismo, que tenham um processo de desenvolvimento que envolva um grande número de pessoas e qualquer aplicação que não tenha o requisito de ser escrita em utilizando outra linguagem :P

Go foi anunciada como uma linguagem destinada a systems programming, mas logo a comunidade adotou a linguagem em distintas áreas, provando sua força para resolver diversos problemas.

Dada a natureza, Go é uma excelente linguagem para construção de daemons e aplicações servidoras. A linguagem também se mostrou forte na construção de APIs HTTP que precisam ser simples de desenvolver, escalar e implantar. Diferente de outras linguagens, é comum, seguro e performático colocar uma aplicação web em Go de cara para o mundo, sem um proxy reverso na frente. Há casos de pessoas utilizando Go mesmo para servir estáticos, mas isto não é algo que eu recomendaria.

Além disso, as dezenas de aplicações utilizada na famigerada cloud vêm adotando Go: Docker, Juju, Tsuru, Flynn, Skynet, Apcera, Railgun, etc.

## E onde devemos descartar a adoção de Go?

Não recomendo o desenvolvimento de "websites" utilizando Go. Aplicações web muito bem resolvidas por frameworks como Django e Rails, onde tudo que você tem é um banco de dados sendo gerenciado e consumido por um website. O motivo é muito simples: Django, Rails e afins são especialistas nesse tipo de problema, possuem um ecossistema de desenvolvedores e bibliotecas muito evoluídas na área.

Naturalmente, existem pessoas que se aventuram na área. O próprio site da linguagem usa somente Go no servidor, então eu não descartaria o uso da linguagem, mas certamente não é a opção mais adequada.

O desenvolvimento de aplicações desktop e mobile ainda estão engatinhando em Go. Uma recente solução, o go-qml, permite desenvolver aplicativos desktop e mobile integrando com o Qt. É uma forma simples de usar Go para aplicativos com interface gráfica no Ubuntu em seus diferentes ambientes (Desktop, smartphones, smart TVs, etc.).

Go também não é a melhor linguagem para lidar com matrizes e cálculos que envolvem muitos pontos flutuantes, continue utilizando Fortran :)

## Descreva sobre a comunidade em torno do ecossistema Go.

A comunidade vem crescendo e ganhando cada vez mais força. Em 2014, haverá a primeira conferência dedicada exclusivamente a Go nos Estados Unidos. No Brasil, existe um pequeno movimento de adoção da linguagem, e algumas iniciativas de evangelização, principalmente através de palestras nos diversos eventos pelo Brasil.

As listas de discussão são bastante movimentadas, e todos os dias novos aventureiros aparecem. Além disso, alguns encontros de usuários vêm acontecendo na Europa, Estados e Austrália, gerando cada vez mais [conteúdo em vídeo sobre a linguagem](http://golang.org/doc/#talks).

Eventos como a OSCON, FOSDEM e Google I/O costumam ser também pequenos encontros da comunidade Go.

## Como você avalia a curva de aprendizado em Go?

É extremamente fácil aprender a programar em Go. Você pode compilar a linguagem e toda sua biblioteca padrão e escrever seu primeiro "Hello world" em menos de 2 minutos. E sem muita dificuldade começar a explorar as features da linguagem e sua biblioteca padrão.

Para concluirmos, quais seriam os primeiros passos para um desenvolvedor começar a se envolver com Go?
Go tem uma excelente documentação, e bons recursos para iniciantes. É possível começar pelo [Tour da linguagem](http://tour.golang.org/), que ensina desde princípios básicos até recursos mais avançados, com exercícios. E tudo que você precisa é o seu navegador: todo código que você escrever poderá ser executado ali mesmo, no navegador. Posteriormente, será possível discutir as soluções para os exercícios na lista de discussão.

O artigo ["Effective Go"](http://golang.org/doc/effective_go.html) é imprescindível para pessoas que começaram a dar os seus primeiros passos com a linguagem.

Por útimo, mas não menos importante, pessoas interessadas em aprender Go encontrarão diversos projetos bacanas para contribuir, como o [Docker][docker], [Tsuru][tsuru] e [Juju][juju].

## Seu ambiente de desenvolvimento

  - **Hardware:** *Macbook Pro 8.1 Intel Core i5 2.4GHz, 16GB de memóra RAM*
  - **Sistema Operacional:** *Mac OS X*
  - **Editor/IDE:** *Vim*
  - **Linguagem preferida:** *Go, Python e C*
  - **Controle de versão:** *Git*
  - **Browser:** *Firefox*


[go]:    http://golang.org/
[tsuru]:    http://www.tsuru.io/
[docker]: http://docker.io
[juju]: http://juju.ubuntu.com
