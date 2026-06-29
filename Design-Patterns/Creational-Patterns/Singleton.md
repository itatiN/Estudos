É um padrão de Projeto que basicamente garante que aquela mesma instancia do objeto rode no ciclo de vida inteiro da aplicação.

Exemplo: Um arquivo de configuração para hashing de senhas é utilizado em diferentes partes do código, com a implementação desse algoritmo dentro de um padrão singleton, usaremos a mesma instancia desse objeto em todo código que precisar.