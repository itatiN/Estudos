O enunciado desse problema é mais difícil que o problema em si, mas basicamente recebemos uma lista de string que pode ter dentro dela:
+ + = Fazer uma adição dos últimos dois números
+ D = Adicionar o dobro do ultimo elemento
+ C = Remover o ultimo elemento
+ Numero = Temos que transformar esse para int para podermos fazer as operações.

Tendo essas informações o algoritmo é bem simples, iniciamos uma stack(pilha); iteramos pelas operações; se for um +, adicionamos a soma dos últimos 2 números;
se for D, adicionamos o dobro do ultimo numero; se for C apenas fazemos um pop;
se for um numero, transformamos esse numero para int e adicionamos a stack;
no final retornamos a soma da stack.

Exemplo de código:
`def calPoints(self, operations: List[str]) -> int:`
        `stack = []`
        `for op in operations:`
            `if op == "+":`
                `stack.append(stack[-1] + stack[-2])`
            `elif op == "D":`
                `stack.append(2 * stack[-1])`
            `elif op == "C":`
                `stack.pop()`
            `else:`
                `stack.append(int(op))`
        `return sum(stack)`

Complexidade:
Tempo: O(n)
Espaço: O(n)
