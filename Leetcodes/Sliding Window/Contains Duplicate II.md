Basicamente nesse problema temos que achar os índices de números iguais que a subtração seja igual a K.
Para isso usamos um algoritmo de sliding window que inicia um hashmap e uma variável esquerda; depois iteramos a lista de números criando uma variável direita; se o numero já estiver no hashmap retornamos true; se não adicionamos ele ao hashmap; se direita - esquerda for maior que K, removemos o numero da esquerda e adicionamos um ao seu contador, o que faz com que o sliding window se mova para frente. 

Exemplo de código:
`def containsNearbyDuplicate(self, nums: List[int], k: int) -> bool:`
        `window = set()`
        `left = 0`
        `for rigth in range(len(nums)):`
            `if rigth - left > k:`
                `window.remove(nums[left])`
                `left += 1`
            `if nums[rigth] in window:`
                `return True`
            `window.add(nums[rigth])`
        `return False`

Complexidade:
Tempo: O(n)
Espaço: O(n)