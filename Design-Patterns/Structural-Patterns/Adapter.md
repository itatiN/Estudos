Usado para fazer interfaces previamente não compatíveis funcionarem entre si.
Normalmente você usa esse padrão para refatoração do seu projeto.
Pode ser usado para fazer conexão com API de terceiros de modo com que a classe chame esse adaptador e esse adaptador faça a conexão certa e caso se precisar alterar ou adicionar um novo, você basicamente cria uma classe nova a partir do adapter mas não altere o adapter principal nem as classes que fazem o uso desse adapter. 
O uso funciona basicamente criando uma camada intermediária responsável por traduzir chamadas, dados ou comportamentos entre duas interfaces não compatíveis.

