# Boas Praticas

## Clean code: quais os impactos do spaghetti code e como melhorar?

##### Gabriela

Veja as principais consequências do spaghetti code e como o clean code  ajuda a evitá-las

Quem nunca se deparou com um código ruim, malfeito e, provavelmente, repleto de defeitos  na sua funcionalidade?

## Mas por que alguns softwares apresentam códigos com tantos erros?

Há algumas explicações para isso, como: “o cronograma ficou apertado”, “vou fazer o básico, depois melhoro”, “os requisitos mudaram no meio do desenvolvimento”, etc. O resultado disso é um código ruim, mal estruturado e difícil de entender, o chamado spaghetti code.  

A aplicação não nasce assim. Ela vai ficando desse jeito ao longo do tempo, depois de muitas alterações e remendos, bem como diferentes equipes a alterarem. Justamente por isso, a deterioração do código é pouco percebida e até negligenciada por gestores. Não por nós. 

Para combater esse problema tão comum surgiu o clean code, uma abordagem de desenvolvimento de software que tem como principal objetivo aplicar técnicas simples para facilitar a escrita e a leitura de um código.

De acordo com Robert C. Martin, em seu livro Clean Code: A Handbook of Agile Software Craftsmanship, que se tornou um clássico, quanto mais o programador utiliza as práticas do clean code, mais ele cria sensibilidade ao código, isto é, amplia sua habilidade de visualizar um código mal escrito e pensar em diferentes formas de limpá-lo ou refatorá-lo. 

Neste artigo, iremos abordar quais os impactos negativos do spaghetti code, quais as práticas adotadas por desenvolvedores para não cair no caos e como melhorar o código de aplicações para se chegar em um código limpo.

Saiba mais: Low-code: o que você precisa saber sobre desenvolvimento com pouco código

## 10 impactos negativos do spaghetti code 

Se você é programador e já trabalhou com um código spaghetti feito por outro profissional, sabe que negligenciar os princípios básicos do clean code pode ser muito ruim, principalmente na hora de reescrever esse código. 

O spaghetti code gera impactos negativos porque é difícil saber o fluxo do código e, como não há documentação que explique como ele foi programado, até porque ao ser escrito sem regras, ele provavelmente foi apenas codificado de uma maneira para funcionar, sem muitos cuidados, torna-se muito complicado refatorar.

Além da dificuldade de ler e manter, o spaghetti code apresenta outros impactos negativos. Relacionamos a seguir os 10 que mais se destacam:

### 1. Dificulta o planejamento

Esse é um dos principais problemas do spaghetti code: product managers e product owners não conseguem fazer boas estimativas para correção de bugs e para atualizações do software. Isso acaba prejudicando SLAs de sustentação e, no limite, o planejamento de releases. 

### 2. Desmotiva a equipe de desenvolvimento

O time de desenvolvimento quer criar e produzir. Porém, ao manter código ruim, ele vai perder muito tempo interpretando o código-fonte antes de dar qualquer passo novo. Com isso, o trabalho se torna maçante e pouco criativo. Logo, logo você terá uma equipe desmotivada, pois está gastando toda sua energia decifrando uma semântica ruim.

### 3. Diminui a produtividade 

Esse impacto é outra consequência de ficar muito tempo em cima da interpretação do código. Trabalhar com um código mal estruturado demanda muito tempo e, consequentemente, o resultado de todo o esforço empenhado. Com isso, o trabalho fica inexpressivo.

### 4. Afeta o ambiente de trabalho 

Outra consequência do spaghetti code é que normalmente esse emaranhado vai se refletir na própria equipe. Programadores vão começar a transferir responsabilidades por problemas não resolvidos e, no limite, você terá uma equipe desconectada e um aumento do turn-over, que já é alto nas áreas relacionadas ao desenvolvimento.

### 5. Implica defeitos maiores

Um código ruim, justamente por ser difícil de compreender, sempre esconde mais defeitos do que os que saltam à vista. Isso resulta na perda de controle da aplicação, aumentando consideravelmente o risco de falhas e de problemas com a segurança da aplicação.

### 6. Soluções improvisadas para resolver problemas 

Uma tralha a mais numa sala que já está completamente bagunçada não vai fazer muita diferença. É assim que os desenvolvedores vão pensar ao adicionar código numa aplicação caótica. Com isso, a sexta consequência do spaghetti code é que os desenvolvedores acabam pegando atalhos, inserindo novos problemas e gerando mais código ruim.

### 7. Perda de performance e de estabilidade da aplicação

O código ruim tem performance ruim também. E esse problema se agrava com o tempo. Correções de uma parte do código que levam a novas necessidades de mudança de outra parte e o excesso de soluções improvisadas afetam o desempenho.

### 8. Aumenta a dívida técnica 

Códigos malfeitos têm uma forte tendência a estarem relacionados com o aumento da dívida técnica, provavelmente, por conta da escolha de um design mais rápido e de baixa qualidade. 

### 9. Dificuldade em otimizar o código

Quando se trata de um spaghetti code é difícil adicionar mais recursos ao programa ou integrá-lo a outros sistemas. A aplicação fica mais engessada, sem contar que os desenvolvedores começam a ficar com medo de mexer para não causar instabilidades.

### 10. Menos atualizações do produto

Com um código spaghetti, fica cada vez mais difícil lançar novas features, fazer melhorias e evoluções no produto, o que o torna obsoleto mais rápido.

## Clean code: a solução para reduzir spaghetti code

Como uma das soluções realmente efetivas para evitar o spaghetti code, as técnicas do clean code foram citadas pela primeira vez no livro Clean Code: A Handbook of Agile Software Craftsmanship, lançado em 2008, por Robert Cecil Martin ou, para os íntimos, Uncle Bob. Ele atua na área de desenvolvimento desde 1970 e também participou da elaboração do Manifesto Ágil, lançado em 2001. 

Martin percebeu que a manutenção era um dos maiores problemas no desenvolvimento de softwares. Devido à criação de código ruim, os desenvolvedores passavam mais tempo tentando entender o código existente do que escrevendo código fresco. 

Assim, Martin chegou à conclusão de que a escrita do código-fonte precisava seguir certos princípios e práticas para ser compreensível e suficientemente flexível. Por meio da sua obra, ele as disseminou pelo mundo.

Hoje, a filosofia do clean code é amplamente usada, tida como boa prática básica do desenvolvimento de softwares.

“O código limpo não é escrito seguindo um conjunto de regras. Você não se torna um artesão de software aprendendo uma lista de práticas. Profissionalismo e habilidade vêm de valores que impulsionam as disciplinas [...] O código limpo sempre parece ter sido escrito por alguém que se importa.” 

- Robert C. Martin, Clean Code: A Handbook of Agile Software Craftsmanship.

## Como melhorar o código de aplicações: as 7 regras do clean code 

Criar um código limpo implica algumas práticas e cuidados na hora do desenvolvimento. O primeiro deles é ter em mente que o clean code tem foco na facilidade de escrever, ler e manter o código.

Para isso, indicamos, abaixo, as 7 principais regras do clean code, citadas no livro de Uncle Bob:

###  1. Use nome, evite abreviações

Abreviações dificultam o entendimento de novos membros do time e podem simplificar contextos que não devem ser simplificados.

###  2. Entenda a ideia central

Entender o contexto em que foi produzida a aplicação e pensar a respeito das suas responsabilidades é um exercício que deve ser feito ao criar um código.

### 3. Seja um bom autor

Para criar um código limpo é necessário criar funções simples, claras e pequenas. O nome pode ser grande, mas a função precisa ser a menor possível.

### 4. Não repita a si mesmo

Não pode existir duas partes do programa que desempenhem a mesma função. Ele deve ser totalmente livre de ambiguidades.

### 5. Refatore o código constantemente

Refatorar deve ser uma constante na produção de um clean code, ou seja, mexer na sua estrutura para torná-la mais clara e fácil de ser modificada, sem alterar nada. Isso faz com que sejam aproveitadas todas as oportunidades, como novas funcionalidades, correções de bugs etc.

### 6. Trate os erros

Os programadores devem ser os responsáveis por garantir que o código faça o que ele precisa. Se algo der errado, saiba tratar as exceções de forma correta.

### 7. Faça testes limpos

A fase de testes é essencial. Afinal, um código só é considerado realmente limpo após ser validado através de um teste. 

## Clean code: evolução nas práticas de desenvolvimento

O clean code é uma filosofia que está se estabelecendo cada vez mais entre os programadores. Seus princípios e boas práticas solucionam problemas que muitos projetos de software enfrentam: a manutenção do código fonte.E é uma busca, acima de tudo, necessária. Afinal,  se há uma máxima entre os programadores é que um bom software nunca estará completamente finalizado.

Evitar o spaghetti code e todos os impactos negativos que ele implica para o projeto deve ser uma prioridade na hora de programar.

Assim como contar com um parceiro em tecnologia que oferece soluções sustentáveis para seus projetos é ter garantia de um desenvolvimento saudável.

Na Supero Tecnologia, nossos projetos adotam práticas do clean code para entregar aplicações com código mais enxuto e semanticamente compreensível. 

[Artigo Original](https://www.supero.com.br/blog/clean-code-quais-os-impactos-do-spaghetti-code-e-como-melhorar/)