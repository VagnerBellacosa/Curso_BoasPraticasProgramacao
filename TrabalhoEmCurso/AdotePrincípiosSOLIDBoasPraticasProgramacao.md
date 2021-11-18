[Início](https://www.dtidigital.com.br/) » [Artigos](https://www.dtidigital.com.br/blog/) » [Tecnologia na prática](https://www.dtidigital.com.br/categoria/tecnologia-na-pratica/) » **Adote os princípios SOLID: Boas práticas de programação**

![Boas práticas de programação](https://www.dtidigital.com.br/wp-content/uploads/2019/03/CAPAS-BLOGPOSTS-5.png)

![img](https://www.dtidigital.com.br/wp-content/uploads/2020/10/moon-1.png)

- TECNOLOGIA NA PRÁTICA

# Adote os princípios SOLID: Boas práticas de programação

[![Magno Santos](https://secure.gravatar.com/avatar/ba730ff66f808690b7bdc323352d2653?s=300&d=mm&r=g)](https://www.dtidigital.com.br/blog/author/magno-santos/)

[Magno Santos](https://www.dtidigital.com.br/blog/author/magno-santos/)

- publicado em: 01/03/2019

É extremamente importante **implementar softwares adotando boas práticas de programação, sobretudo com princípios SOLID**. Elas propiciam o desenvolvimento de um código limpo, legível e testável. Diante dessa perspectiva, os sistemas atualmente implementados pela[ dti digital crafters](https://www.dtidigital.com.br/) são embasados [nos princípios SOLID proposto por Robert C. Martin](https://medium.com/desenvolvendo-com-paixao/o-que-é-solid-o-guia-completo-para-você-entender-os-5-princípios-da-poo-2b937b3fc530), por volta do ano 2000.

![princípios SOLID ](https://dtidigital.com.br/wp-content/uploads/2019/03/1.png)

Propomos neste material abordar algumas violações x código adequado de acordo com os princípios instituídos pelo SOLID.

Sumário [[Ver menos](https://www.dtidigital.com.br/blog/adote-principios-solid-boas-praticas-de-programacao/#)]

- [1 Princípio SSRP – Single responsibility principle](https://www.dtidigital.com.br/blog/adote-principios-solid-boas-praticas-de-programacao/#Principio-SSRP-Single-responsibility-principle)
- [2 Precisamos falar sobre SGBD quando falamos de princípios SOLID](https://www.dtidigital.com.br/blog/adote-principios-solid-boas-praticas-de-programacao/#Precisamos-falar-sobre-SGBD-quando-falamos-de-principios-SOLID)
- [3 Princípio OOCP – Open/Close principle](https://www.dtidigital.com.br/blog/adote-principios-solid-boas-praticas-de-programacao/#Principio-OOCP-8211-OpenClose-principle)
- [4 Princípio LLSP – Liskov substitution principle](https://www.dtidigital.com.br/blog/adote-principios-solid-boas-praticas-de-programacao/#Principio-LLSP-Liskov-substitution-principle)
- [5 Princípio IISP – Interface segragation principle](https://www.dtidigital.com.br/blog/adote-principios-solid-boas-praticas-de-programacao/#Principio-IISP-Interface-segragation-principle)
- [6 Princípios de substituição](https://www.dtidigital.com.br/blog/adote-principios-solid-boas-praticas-de-programacao/#Principios-de-substituicao)
- [7 Princípios SOLID em DDIP – Dependency Invension Principle](https://www.dtidigital.com.br/blog/adote-principios-solid-boas-praticas-de-programacao/#Principios-SOLID-em-DDIP-Dependency-Invension-Principle)
- [8 Segregação de Interface](https://www.dtidigital.com.br/blog/adote-principios-solid-boas-praticas-de-programacao/#Segregacao-de-Interface)
- [9 Referências – Princípios SOLID](https://www.dtidigital.com.br/blog/adote-principios-solid-boas-praticas-de-programacao/#Referencias-8211-Principios-SOLID)

## Princípio SSRP – Single responsibility principle

Observe a seguinte classe:

![princípios SOLID ](https://dtidigital.com.br/wp-content/uploads/2019/03/2.jpg)

Acredita que o método dicionarUmaNovaPessoa() deveria ser responsável por realizar tantas coisas? Como definir o modelo dos dados persistentes da aplicação, instanciar conexão e realizar manipulação de dados no banco? A solução para esse problema pode ser apontado a seguir:

![princípios SOLID ](https://www.dtidigital.com.br/wp-content/uploads/2019/03/3.png)

Note que a organização dos arquivos foi alterada, agora as classes estão divididas de acordo com as suas responsabilidades.
As classes CPFServices.cs e EmailServices.cs são responsáveis por validar os dados de CPF e E-mail da pessoa que se pretende cadastrar.

![princípios SOLID ](https://dtidigital.com.br/wp-content/uploads/2019/03/4.png)
![princípios SOLID ](https://dtidigital.com.br/wp-content/uploads/2019/03/5.png)
O método EValida() destas classes garante a **validação dos dados**, perceba que estes métodos são chamados na classe Pessoa.cs que contém os dados persistentes da aplicação (como um espelho da estrutura do banco de dados).

![princípios SOLID ](https://www.dtidigital.com.br/wp-content/uploads/2019/03/6.png)

## Precisamos falar sobre SGBD quando falamos de princípios SOLID

A classe PessoasRepository.cs responsabiliza-se pelo gerenciamento dos dados, logo a instanciação de conexão e definição dos métodos de adição de dados no **Sistema Gerenciador de Banco de Dados** (SGBD) devem ser definidos nesta classe. (Obs.: Isso ainda irá ser melhorado, não levem como verdade absoluta)![princípios SOLID ](https://www.dtidigital.com.br/wp-content/uploads/2019/03/7.png)

Por fim, a classe PessoaService.cs valida os dados e realiza o cadastro da Pessoa, com base nos métodos e classes que agora estão separados de acordo com sua responsabilidade.

## Princípio OOCP – Open/Close principle

Neste exemplo, criou-se uma classe enum para armazenar os turnos.

![validação de dados ](https://www.dtidigital.com.br/wp-content/uploads/2019/03/8.png)

Uma classe RemuneraçãoPorTurnos também foi criada para implementar o salário que algum funcionário recebe por cada turno, dessa forma bastaria alterar esta classe de acordo que surgissem novas demandas de turnos e acrescentar um if com a lógica correspondente à mudança.

![princípios SOLID ](https://www.dtidigital.com.br/wp-content/uploads/2019/03/9.png)

Porém, alterar uma classe já em funcionamento não é legal. Pensando nisso, podemos adicionar uma classe RemuneracaoBase que possa ser implementada por **cada turno com sua lógica correspondente**. Tal classe pode ser extensível para suas classes derivadas e fechada apenas naquele escopo que pretende atender. Veja o exemplo:

![programação ](https://www.dtidigital.com.br/wp-content/uploads/2019/03/10.png)Quero agora a remuneração para o turno matutino, assim:

![Cálculo matutino ](https://www.dtidigital.com.br/wp-content/uploads/2019/03/11.png)

## Princípio LLSP – Liskov substitution principle

Princípio de substitução de Liskov , pode ser apresentado pela seguinte diagramação UML:

![princípios SOLID ](https://www.dtidigital.com.br/wp-content/uploads/2019/03/12.gif)
Salienta-se que a classe Quadrado é similar à classe Retangulo, porém com uma característica especial: a largura e a altura são iguais. Logo, à primeira vista tudo parece correto (principalmente de forma conceitual, pois um quadro é um caso especial de um retângulo). Na notação UML classe Quadrado se apresenta com uma classe derivada e a classe retângulo configura-se como a classe base

![princípios SOLID ](https://www.dtidigital.com.br/wp-content/uploads/2019/03/13.png)Note que na classe Retangulo, definiu-se a altura, largura e uma função para cálculo de área. E diante do nosso contexto, a classe Quadrado deve herdar de retângulo e sobreescrever seus métodos.

![programação em SOLID ](https://www.dtidigital.com.br/wp-content/uploads/2019/03/14.png)

[![Entre chaves banner2](https://www.dtidigital.com.br/wp-content/uploads/2021/05/Entre-chaves-banner2-1.png)](https://www.instagram.com/entre.chaves/)Entre chaves banner2

Porém , como a classe quadrado herda de retângulo, esta também herdará a altura e largura da classe base. Isso não faz sentido, pois a altura e largura do retângulo não são iguais, o que descaracteriza as propriedades de um quadrado.

A solução é simples:

![princípios SOLID ](https://www.dtidigital.com.br/wp-content/uploads/2019/03/15.png)Ao definir a classe paralelogramo, é possível atribuir os dados de altura e largura corretos para cada uma das figuras geométricas, com isso o cálculo da área será feito corretamente.

## Princípio IISP – Interface segragation principle

Um claro exemplo da utilização de interfaces generalistas demais pode ser apresentado a seguir:

![princípios SOLID ](https://www.dtidigital.com.br/wp-content/uploads/2019/03/16.png)Perceba que a interface ICadastroGeral possui métodos para validar as informações, salvá-las no banco de dados e enviar e-mail confirmando o cadastro. Mas[ esses métodos são aplicáveis a todas as classes](https://www.dtidigital.com.br/blog/produto-transicao-de-carreira/) que implementam a interface?

![SOLID ](https://www.dtidigital.com.br/wp-content/uploads/2019/03/17.png)![validação de dados ](https://www.dtidigital.com.br/wp-content/uploads/2019/03/18.png)

Perceba que para a classe de CadastroMercadoria a interface não seria aplicável, pois uma mercadoria não possui um e-mail. Pense em criar interfaces específicas, não importa quantas interfaces tem sua solução desde que sejam aplicáveis a todos os casos!

## Princípios de substituição

Este tópico trata, sobretudo, do princípio da substituição Liskov: Um conceito importante para quem deseja se aprofundar mais nos [princípios de S.O.L.I.D](https://mari-azevedo.medium.com/princípios-s-o-l-i-d-o-que-são-e-porque-projetos-devem-utilizá-los-bf496b82b299), como os já apresentados anteriormente. Embora seja mais subjetivo, o princípio em questão diz que em um aplicativo, o objeto determinado pode ser facilmente substituído por outro objeto de um tipo derivado: Isso tudo sem sofrer qualquer impacto. Estamos falando claramente sobre conceitos abstratos e definição de contratos por meio de interfaces. Para melhor demonstrar esse princípio, imaginemos um programa bancário que exibe um relatório completo sobre as taxas de juros do cliente. No relatório, temos o arquivo do cliente e informações sobre as taxas.

## Princípios SOLID em DDIP – Dependency Invension Principle

O princípio de inversão de dependências diz respeito à depender de uma abstração e não de uma implementação. Nesse caso, todos os demais princípios são aplicados, garantindo que os sistemas sejam o mais desacoplados e coesos possível. Para isso, recomenda-se trabalhar com a **injeção de dependências**. Em linhas gerais, **“Injetar” uma dependência, nada mais é que passar uma classe (habitualmente uma classe interface) que será utilizada, para outra que irá consumir seus recursos.**

Diante do que foi apresentado até aqui, a proposta do DDIP é prover um conjunto de interfaces específicas, classes que trabalhem com responsabilidade única e que sejam fechadas no seu escopo e abertas para extensão.

![pessoa services ](https://www.dtidigital.com.br/wp-content/uploads/2019/03/19.png)

A classe **PessoaServices.cs é neste caso, responsável por controlar as manipulações e verificações de dados da pessoa que for cadastrada no sistema.** Neste caso, o construtor desta classe, está assim definido:

![princípios SOLID](https://www.dtidigital.com.br/wp-content/uploads/2019/03/20.png)princípios SOLID

 

## Segregação de Interface

Uma forma de otimizar o trabalho de toda e qualquer pessoa que trabalha com desenvolvimento é a quebra de alguns paradigmas pré-estabelecidos na área. O princípio de segregação parte do ponto de condução para que os desenvolvedores não tentem reaproveitar suas interfaces, porque há uma citação que diz: [“muitas interfaces específicas são melhores do que uma interface única.”](https://medium.com/@engnogueirawgn/princípio-da-segregação-de-interfaces-isp-8344ce3c5b4e)

Existem formas de encontrar solução para a segregação de interface. Com uma aplicação otimizada, ele nos da a possibilidade de utilizar o próximo princípio da inversão de dependência, inversão de controle e que nos leva a injeção de dependência.

Perceba que para adicionar uma nova pessoa neste exemplo, será preciso **injetar duas classes para validação** e adição de dados. Dessa forma, para que seja possível construir uma classe PessoaServices é preciso passar a referência das interfaces IEmailServices e IPessoaRepository. Lembramos também que esse é um princípio indispensável para quem busca **se aperfeiçoar em princípios SOLID.**

![princípios SOLID](https://www.dtidigital.com.br/wp-content/uploads/2019/03/21.png)

Note que o método AdicionarPessoa(Pessoa pessoa), é **responsável apenas por adicionar uma nova pessoa**, delegando à _pessoaRepository adicionar os dados dessa pessoa em um repositório de informações (pode ser um banco de dados, em memória, dentre outros) e à _emailServices enviar um e-mail comunicando que a pessoa foi cadastrada com sucesso !
Esperamos que este artigo seja útil a todos para entendimento e adoção do SOLID em suas aplicações. Obrigado !

## Referências – Princípios SOLID

- https://www.devmedia.com.br/padrao-de-injecao-de-dependencia/18506
- https://medium.com/thiago-aragao/solid-princ%C3%ADpios-da-programa%C3%A7%C3%A3o-orientada-a-objetos-ba7e31d8fb25
- https://www.eduardopires.net.br/2013/04/orientacao-a-objeto-solid/