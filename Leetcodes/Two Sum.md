A maneira mais fácil de resolver esse problema é iterando os números e salvando-os em um hashmap que contenha o valor do numero e sua posição, na iteração eu faço uma conta para descobrir qual valor o target - aquele numero eu preciso achar; confiro se já tenho ele no hashmap; se sim, retorno a posição desse numero e o numero em si; se não, repito o processo ate achar o resultado esperado.

Exemplo de código em python:
`def twoSum(self, nums: List[int], target: int) -> List[int]:`
        `prevMap = {}`
        `for i, n in enumerate(nums):`
            `diff = target - n`
            `if diff in prevMap:`
                `return [prevMap[diff], i]`
            `prevMap[n] = i`
        `return -1`
        
Complexidade:
Tempo: O(n)
Espaço: O(n)