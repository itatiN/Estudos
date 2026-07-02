Outro problema que pode ser resolvido com sliding window, simplesmente podemos criar uma variável esquerda e outra direita; criar uma variável para conter o maior profit; iterar o conjunto de valores e se achar um valor menor fazer o inicio do sliding window mudar para a direita; se achar um possível candidato a profit, simplesmente checa se é melhor ou pior do que o profit atual. Sempre vamos adicionar um numero a mais na direita para continuar checando todos os números.

Exemplo de código:
`def maxProfit(self, prices: List[int]) -> int:`
        `l, r = 0, 1`
        `maxProfit = 0`
        `while r < len(prices):`
            `if prices[l] < prices[r]:`
                `profit = prices[r] - prices[l]`
                `maxProfit = max(maxProfit, profit)`
            `else:`
                `l = r`
            `r += 1`
        `return maxProfit`
        
Complexidade:
Tempo: O(n)
Espaço: O(1) - Pois não crio nenhuma lista nova