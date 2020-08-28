# Test-Driven Development: By Example

<img src="../img/livros/test-driven-development.jpg" alt="drawing" height="250"/>

## Preface

Código limpo é importante, mas como alcança-lo? Drive development com testes automatizados "Test-Driven Development" (TDD). Nele voce:

* Escreve código novo só se primeiramente tiver um teste automatizado que falhou.
* Elimina duplicação.

As implicações técnicas dessas duas regras simples:

* Projetar organicamente
* Escrever seus próprios testes
* Fornecer resposta rápida a pequenas mudanças
* Projetar componentes altamente coesos e fracamente acoplados, apenas para facilitar o teste.

Essas duas regras implicam em uma ordem a tarefa de programar

* Vermelho - escrever um pequeno teste que não funciona e talvez nem compile
* Verde - fazer o teste funcionar rapidamente, cometendo todos os pecados no caminho
* Refatorar - eliminar toda a duplicação criada justamente pra fazer o teste funcionar

### Courage

TDD é uma forma de gerenciar o medo durante a programação

TDD é uma consciência da lacuna entre a decisão e o feedback durante a programação e as técnicas para controlar essa lacuna.

Certamente há tarefas de programação que não podem ser conduzidas apenas por testes, como software de segurança e concorrência.

## Section I: Money Example

Ritmo do TDD

1. Rapidamente adicione um teste
2. Rode todos os testes e veja o novo falhar
3. Faça uma pequena mudança
4. Rode todos os testes e veja todos passarem
5. Refatorar para remover duplicação

### Money Example

Não começamos com objetos, começamos com testes

Quando escrevemos um teste, imaginamos a interface perfeita para nossa operação. Estamos dizendo a nós mesmos como a operação será vista de fora. Nossa história nem sempre se tornará realidade, mas é melhor começar com a melhor API possível e trabalhar de tráz pra frente do que tornar as coisas complicadas, feias e "realistas" desde o início.

Pode-se acabar com vários erros de compilação em um único teste. Podemos precisar de um construtor, mas ele não precisa fazer nada. Podemos precisar de uma implementação vazia para métodos.

**Faremos o mínimo de trabalho possível apenas para que o teste seja compilado.**

Depois de solucionar os erros de compilação, executamos o teste e observamos sua falha. O fracasso é progresso. Transformamos um problema muito mais amplo para "fazer esse teste funcionar e fazer o resto dos testes funcionarem", que é, na verdade, um escopo muito mais simples e menor para o medo.

**Fazer passar**

O objetivo agora não é obter a resposta perfeita, o objetivo é passar no teste.

**Fazer certo**

Dependência é o problema chave no desenvolvimento de software em todas as escalas. Se a dependência é o problema, a duplicação é o sintoma.

Os objetos são excelentes para abstrair a duplicação da lógica. A eliminação da duplicação de programas elimina a dependência. Ao eliminar a duplicação antes de ir para o próximo teste, maximizamos nossa chance de conseguir executar o próximo teste com uma e apenas uma alteração.

TDD não é sobre darmos passos pequeninos; é sobre sermos capazes de dar passos pequeninos.

### Degenerate Objects
