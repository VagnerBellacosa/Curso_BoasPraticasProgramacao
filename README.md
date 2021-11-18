<!-- PROJECT SHIELDS -->

[![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]
[![MIT License][license-shield]][license-url]
[![LinkedIn][linkedin-shield]][linkedin-url]

<!-- PROJECT LOGO -->
![Boas praticas em Programacao](Image/capa.png "Bootcamps")




# Curso Boas Praticas Programaçao

Desenvolver bom código, limpo, de fácil entendimento e ver as boas praticas do mercado

- [Trabalho em Curso](TrabalhoEmCurso)

Criar um roteiro onde o jovem padawan, aprenda a desenvolver bom codigo, limpo, testavel e funcional.



------



## 1 – Identar o código

Considero a identação de código um dos itens mais básicos e ao mesmo tempo importante para um programador, sendo ele iniciante ou avançado. O fato de identificarmos o escopo de condições IF, WHILE e etc., facilita muito entendimento do código, além de deixar mais bonito.

Tenho um defeito muito grave, por mais simples que seja o código mas se o mesmo estiver sem identação eu não consigo ler e muito menos entender nada, parece até “tique nervoso” mas já começo a colocar uns espaçamentos no código quase que involuntariamente.



## 2 – Nomear variáveis de maneira intuitiva

Nomear variáveis pode parecer uma tarefa simples, basta seguir as restrições de cada linguagem e por causa disso os nomes acabam não possuindo sentido ao escopo do código.

É possível encontrar esse tipo de problema em loops usando laços de repetição “FOR” aninhados, onde é comum encontrarmos contadores com nome de x, y, z e etc., variáveis, até mesmo nome de estruturas como Arrays é possível encontrar nomes “bizarros”.

 

## 3 – Evite chamar funções para testes em loops

Aproveitando o exemplo das 2 Arrays acima, vamos usar um “FOR” para percorrer os elementos das Arrays, mas o laço “FOR” precisa saber qual é o limite do loop, é nesse momento que geralmente chamamos funções nativas para efetuar a contagem de elementos.

No exemplo abaixo chamo a função “count()” para saber a quantidade de elementos na minha Array, temos que levar em consideração que caso nossa Array tenha 500 elementos, iremos chamar a função “count()” 500 vezes.



 

## 4 – Evitar condição de negação no IF

Praticamente não existe programação sem o controle de fluxo usando condições “IF”, a ideia é sempre avaliar se uma condição é verdadeira dentro da condição para executar determinado código. 

Por esse motivo evite sempre que possível usar verificações de negação na condição, sempre que possível avalie primeiro a condição verdadeira e caso falso execute o código do  “ELSE”, isso também torna o código mais legível e menos confuso quando temos “IFs” aninhados.

 

## 5 – Nomear funções da maneira intuitiva

Nomear funções é outra tarefa que aparentemente é simples, mas se soubermos escolher nomes mais intuitivos e ligados ao objetivo da função, também podemos tornar nosso código mais legível.

Por exemplo, nos meus scripts orientado a objetos ou não, tenho o costume de nomear funções que retornam valores do tipo BOOLEAN sempre iniciando com “is”, essa prática deixa a chamada da função dentro de um “IF” mais intuitivo.

No código abaixo coloquei uma função básica para validar e-mails “isEmailValid()”, quando chamo a função para válidar um e-mail o entendimento da condição “IF” fica algo semelhante “SE é um e-mail válido ENTÃO”:



## 6 – Comentar o código

Existem algumas literaturas que criticam a prática de comentar o código, pois acaba aumentando a quantidade de linhas e enchendo o código com sujeira, no livro “Código Limpo” o autor defende que variáveis e métodos bem nomeados são as melhores documentações e tiram a necessidade dos comentários.

Pessoalmente discordo dessa opinião, acho que um comentário detalhando o objetivo do método ou função, seus parâmetros de entrada e de saída podem ajudar em manutenções futuras desse código, principalmente se a manutenção for de um profissional que não conhece o sistema.



## 7 – Padronizar nome das constantes

Constantes são valores que não podem ser alterados durante a execução de uma aplicação, por isso elas merecem um destaque em nossos sistemas.

Uma boa prática é definir um padrão para o nome das constantes sempre em caixa alta, isso ajuda a identifica-las no meio do código, claro que se o programador tiver o costume de nomear variáveis em caixa alta também aí não tem sentido essa prática das constantes.



## 8 – Utilizar blocos try..catch..

Trabalhar com códigos dentro de blocos try..catch é considerado até uma boa prática de segurança, por exemplo se ocorrer um erro no script PHP para conexão com o banco de dados onde não está sendo usando try..catch, existem situações que será impresso na página o nome do banco de dados.

Além disso controlando as EXCEPTIONS da sua aplicação você pode exibir mensagens mais intuitivas para o usuário, evitando aquelas mensagens em ‘inglês” que são padrão da maioria das linguagens de programação.

Em ambiente de desenvolvimento até poderíamos exibir a mensagem de erro gerada em PDOException e retornada por “$e->getMessage()”, mas em produção é necessário uma mensagem mais amigável como abaixo:



## 9 – Não usar valor padrão em argumentos de funções

Quando escrevemos uma função que necessita receber argumentos de entrada as vezes sentimos a necessidade de deixar um valor padrão nesse argumento, mas garanto que nem mesmo quem escreveu a função vai lembrar desse valor padrão quando precisar debugar em erro, imagine outro programador.

De preferência em tratar um valor de argumento inválido do que usar um valor padrão, 



## 10 – Percorrer loops somente o necessário

As vezes precisamos percorrer um loop procurando por apenas uma combinação e mesmo após encontrar essa combinação ainda deixamos o loop executando por uma infinidade de vezes.

No exemplo abaixo estou percorrendo a “$arrayNome” procurando pelo valor ‘William’, caso seja encontrado atribuo o valor TRUE para variável “$existe” e mesmo assim o loop contínua, uma boa prática seria encerrar a execução do loop usando “break”.




---

#### * DIO - Digital Inovation One *
######  [Inscreva-se na Dio](https://digitalinnovation.one/sign-up?ref=R5J3ZLTIFS)  

######  [Vagner Bellacosa perfil na Dio](https://web.digitalinnovation.one/users/vagnerbellacosa?tab=achievements)  

<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[contributors-shield]: https://img.shields.io/github/contributors/VagnerBellacosa/Curso_BoasPraticasProgramacao.svg?style=for-the-badge
[contributors-url]: https://github.com/VagnerBellacosa/Curso_BoasPraticasProgramacao/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/VagnerBellacosa/Curso_BoasPraticasProgramacao.svg?style=for-the-badge
[forks-url]: https://github.com/VagnerBellacosa/Curso_BoasPraticasProgramacao/network/members
[stars-shield]: https://img.shields.io/github/stars/VagnerBellacosa/Curso_BoasPraticasProgramacao.svg?style=for-the-badge
[stars-url]: https://github.com/VagnerBellacosa/Curso_BoasPraticasProgramacao/stargazers
[issues-shield]: https://img.shields.io/github/issues/VagnerBellacosa/Curso_BoasPraticasProgramacao.svg?style=for-the-badge
[issues-url]: https://github.com/VagnerBellacosa/Curso_BoasPraticasProgramacao/issues
[license-shield]: https://img.shields.io/github/license/VagnerBellacosa/Curso_BoasPraticasProgramacao.svg?style=for-the-badge
[license-url]: https://github.com/VagnerBellacosa/Curso_BoasPraticasProgramacao/blob/master/LICENSE.txt
[linkedin-shield]: https://img.shields.io/badge/-LinkedIn-black.svg?style=for-the-badge&logo=linkedin&colorB=555
[linkedin-url]: https://www.linkedin.com/in/VagnerBellacosa/
[product-screenshot]: Image/capa.png
