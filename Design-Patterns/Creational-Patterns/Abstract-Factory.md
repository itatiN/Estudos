Padrão mais verboso e que necessita o uso de mais classes e interfaces.
Normalmente utilizado por linhas de produtos que precisam ter compatibilidade, ou apenas para funções semelhantes que dependem de terceiros.
Basicamente você cria uma interface para cada método usado em um determinado produto; Depois disso você cria uma interface que subscreve os métodos da primeira interface para um método mais concreto; Depois você tem a Factory que vai retornar as interfaces que já estão mais concretas.

Exemplo: Um gateway de pagamentos pode ser dividido entre 3 interfaces ( Processamento de pagamentos, Validação da transação, e Checar se existe fraude);
A partir disso podemos fazer mais 3 "interfaces concretas" que vão realmente implementar o funcionamento esperado dos métodos da interface; Depois temos a Factory que monta essas 3 "interfaces concretas" e esta pronto para retornar para a aplicação.