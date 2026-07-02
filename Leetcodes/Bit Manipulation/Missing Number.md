A melhor maneira de resolver esse problema é primeiro iniciar uma variável contendo o tamanho(length ou apenas .len(nums)) da lista de números; depois iterar a lista e ir adicionando a variável inicial com o resultado da subtração do index - o numero atual da lista; na ultima iteração teremos o numero que esta faltando. 

Exemplo de código: 
`def missingNumber(self, nums: List[int]) -> int:`
        `res = len(nums)`
        `for i in range(len(nums)):`
            `res += i - nums[i]`
        `return res`

Complexidade:
Tempo: O(n)
Espaço: O(1)