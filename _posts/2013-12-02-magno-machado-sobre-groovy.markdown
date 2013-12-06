---
layout:         post
title:          "Magno Machado sobre Groovy"
subject:        "Groovy"
date:           2013-12-02 08:00:00
categories:     groovy
comments:       true
description:    Um Papo com Magno Machado sobre Groovy
interviewee_name:   Magno Machado
interviewee_avatar: ../images/avatar/magno-machado.jpg
interviewee_avatar_major: ../images/avatar/magno-machado.jpg
interviewee_bio:    Magno Machado é programador por paixão e professor pardal nas horas vagas. Atualmente divide seu tempo entre desenvolvimento em Groovy/Grails e projetos de dominação global com Arduino.
interviewee_twitter: https://twitter.com/magnomp
interviewee_facebook: https://www.facebook.com/magno.m.paulo
interviewee_blog: http://blog.magnomachado.com.br/
interviewee_googleplus: https://plus.google.com/117728583691170432727/posts
interviewee_bitbucket: https://bitbucket.org/magnomp

---


## Magno, como está sendo sua experiência com Groovy? Existe algum caso específico que você gostaria de compartilhar?

Minha experiência com [Groovy][groovy] na verdade está intimamente relacionada à minha experiencia com [Grails][grails]. No momento trabalho ativamente em três projetos Groovy/Grails, sendo um comercial/fechado e dois abertos, um dos quais um [plugin de gráficos][plugin-graficos] que serve aos outros projetos. A experiência não poderia ser melhor, a dupla caiu como uma luva nas minhas necessidades, que eram de uma plataforma para desenvolvimento web que ao mesmo tempo me trouxesse agilidade e me permitisse aproveitar a familiaridade que já tinha com Java.


## Como você vê a relação entre Groovy e as outras linguagens para JVM?

Hoje é possível executar várias linguagens na JVM, mas Groovy para mim se diferencia pelo fato de não ser apenas mais uma linguagem na JVM, e sim algo como um Java desburocratizado. Isso não a torna nem melhor nem pior que outras linguagens, é apenas uma característica que em alguns casos pode ser interessante, e em outros casos pode não ter valor algum.

Com poucas exceções, Groovy suporta toda a sintaxe do Java, ao mesmo tempo em que suporta construções adicionais, menos verbosas, ou formas alternativas de atingir o mesmo resultado (ex: `def m = [foo: "Bar"]` ao invés de `Map m = new HashMap(); m.put("foo", "Bar");`)

Para quem vem de uma experiência em Java, isso coloca em suas mãos uma linguagem com mais recursos, menos burocracia, menos verbosidade, ou seja, tudo que se espera de uma linguagem moderna, ao mesmo tempo que permite uma transição extremamente suave. Em resumo, você pode usar Groovy apenas como um Java sem ponto-e-virgula, ou pode aproveitar algumas construções da linguagem para escrever um
código mais enxuto e legível, ou pode aproveitar o dinamismo que ela te oferece e explorar possibilidades únicas!

## Qual você considera o ponto positivo da linguagem?

A base em Java sem dúvida foi um ponto positivo para mim.

Um recurso que considero fenomenal, embora não seja de uso em larga escala são as transformações AST, que em termos bem simples seria como um plugin para o compilador. Basicamente você pode interferir na própria compilação em qualquer uma das várias fases que o compilador percorre, modificando o que quiser no código fonte antes de ser produzido o bytecode final. O Grails por exemplo utiliza isso para transformar uma classe de domínio declarada seguindo as convenções do Grails:

{% highlight java %}
class Foo {
    String name
    static hasMany = [
        bars: Bar
    ]
    static constraints = {
        name nullable: true
    }
}
{% endhighlight %}

em uma classe com id, versão, métodos de busca e persistencia, log, validação, relacionamentos e etc, sendo tudo isso ocorrendo em tempo de compilação, portanto sem qualquer overhead em tempo de execução.

## E o ponto negativo?

Todo o dinamismo do Groovy sendo executado numa plataforma como a JVM, que não foi projetada para isso, traz um impacto negativo que em alguns casos pode ser bem significativo. Com o InvokeDynamic do Java7 isso tende a melhorar, entretanto.


## Quais seriam os primeiros passos para um desenvolvedor começar a estudar Groovy?

Conciliar com Grails é uma opção, foi o caminho que segui. Pode-se também começar a utilizar a linguagem com pequenos scripts para automatizar tarefas em algum projeto, vai ajudar a assimilar "o jeito groovy de fazer as coisas", pois muitas tarefas podem ser feitas usando "o jeito java" sendo que há uma alternativa "groovyficada" que é muito mais enxuta e legível.

## Seu ambiente de desenvolvimento

  - **Hardware:** *Dell Vosto 3500 Intel Corei5 @2.26Ghz 4Gb ram*
  - **Sistema Operacional:** *Windows 7 (Podem tacar pedras!!)*
  - **Editor/IDE:** *Eclipse, Spring Groovy/Grails Tool Suite*
  - **Linguagem preferida:** *Groovy*
  - **Controle de versão:** *Mercurial*
  - **Browser:** *Internet Explorer... Pelo tempo necessário para baixar o Google Chrome*


[groovy]:    http://groovy.codehaus.org/
[grails]:    http://grails.org/    
[plugin-graficos]: https://bitbucket.org/magnomp/grailscharts/