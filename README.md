# Projeto-State
- Intenção:

State é um padrão de design comportamental que permite que um objeto altere seu comportamento quando seu estado interno muda. Parece que o objeto mudou sua classe.

- Implementação:

O padrão State é uma solução para o problema de como fazer o comportamento depender do estado.

-Defina uma classe de "contexto" para apresentar uma única interface para o mundo exterior.
-Defina uma classe base abstrata State.
-Representam os diferentes "estados" da máquina de estado como classes derivadas da classe base State.
-Defina o comportamento específico do estado nas classes derivadas de estado apropriadas.
-Manter um ponteiro para o "estado" atual na classe "contexto".
-Para alterar o estado da máquina de estado, altere o ponteiro de "estado" atual.

- Estrutura:

A interface da máquina de estado é encapsulada na classe "wrapper". A interface da hierarquia do wrapper espelha a interface do wrapper, com exceção de um parâmetro adicional. O parâmetro extra permite que classes derivadas de wrappee chamem de volta à classe de wrapper conforme necessário. A complexidade que, de outra forma, arrastaria para baixo a classe de invólucro é ordenadamente compartimentada e encapsulada em uma hierarquia polimórfica à qual o objeto de invólucro delega.

![alt text](https://sourcemaking.com/files/v2/content/patterns/State1.png)

- Exemplo

O padrão State permite que um objeto mude seu comportamento quando seu estado interno muda. Esse padrão pode ser observado em uma máquina de venda automática. As máquinas de venda automática têm estados com base no estoque, quantidade de moeda depositada, a capacidade de fazer alterações, o item selecionado, etc. Quando a moeda é depositada e uma seleção é feita, uma máquina de venda automática entrega um produto e, sem troco, entrega um produto e mudança, não entregue nenhum produto devido a moeda insuficiente no depósito, ou não entregue nenhum produto devido ao esgotamento do estoque.

![alt text](https://sourcemaking.com/files/v2/content/patterns/State_example1.png)
