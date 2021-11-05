# Aula 9 - LINGUAGEM SQL – Transação

Continuaremos utilizando o Banco de Dados da Empresa para os exemplos.

## Transação

Uma transação é uma unidade de execução de programa que acessa e, possivelmente, atualiza vários itens de dados. Uma transação, geralmente, é o resultado da execução de um programa de usuário escrito em uma linguagem de manipulação de dados, e é delimitada da seguinte forma:

```
begin transaction
.........
end transacion
```

A transação consiste de todas as operações ali executadas, entre o começo e o final da transação. Durante a execução de uma transação, o banco de dados pode passar por estados de inconsistência por vários motivos, como: queda de energia, falha física etc.

## Propriedades das Transações

Após uma transação, o banco de dados deve continuar consistente. Para assegurar a integridade dos dados, um sistema de banco de dados deve ter as seguintes propriedades das transações: atomicidade, consistência, isolamento e durabilidade, que são as chamadas propriedades ACID das transações.

Atomicidade: Indivisibilidade - É a propriedade que garante que todas as operações de uma transação são refletidas corretamente no banco de dados ou nenhuma será. Uma transação é indivisível;

Consistência: A execução de uma transação isolada (ou seja, sem a execução de outra transação qualquer concorrentemente) preserva a consistência do banco de dados;

Isolamento: Embora diversas transações possam ser executadas concorrentemente, o SGBD deve garantir que, para todo par de transações Ti, Tj, Ti, o Tj tenha terminado suas operações antes de Ti começar com as suas. Assim, cada transação não toma conhecimento de outras transações concorrentes no sistema. O sistema pode executar um pedaço de Ti parar e executar um pedaço de Tj, mas para as transações elas são únicas no sistema;

Durabilidade: Depois de a transação completar-se com sucesso, as mudanças que ela faz no banco de dados persistem, até mesmo se houver falha no sistema.

## Estados da transação

Quando não ocorre falha alguma na transação, todas as suas operações completam-se com sucesso e ela é efetivada, seus efeitos não podem ser desfeitos ou abortados. De outro modo, se ocorrer algum problema (falha) durante a transação, neste caso a transação será abortada e as operações já realizadas serão desfeitas.

Para melhor entendermos o funcionamento desse sistema, descrevemos o modelo simples e abstrato de estados das transações.

Cinco são os estados possíveis de uma transação:

| Ativa (ou estado inicial)                                                   | Em efetivação parcial               | Em falha                                                                           | Abortada                                                                                                                        | Em efetivação                             |
| --------------------------------------------------------------------------- | ----------------------------------- | ---------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------- |
| A transação permanece neste estado enquanto está executando suas operações. | Após a execução da última operação. | Após a descoberta de que a execução normal da transação já não pode ser realizada. | Depois que a transação foi desfeita e o banco de dados foi restabelecido ao estado anterior do início da execução da transação. | Após a conclusão da transação com sucesso |

![Estados da transação](/media/Implementação-de-Banco-de-Dados/aula9/Image1.jpeg)

### Transações concorrentes

Os sistemas de processamento de transação de banco de dados normalmente permitem que diversas transações sejam executadas de modo concorrente. Permitir que essas transações concorram na atualização dos dados traz diversas complicações em relação à consistência dos bancos de dados.

|              |                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| ------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Vantagens    | Uma transação consiste de diversos passos. Alguns envolvem atividades de E/S; outros, atividade de UCP. Logo, atividades de E/S podem ser feitas em paralelo com o processamento de UCP; assim, o paralelismo entre atividades de E/S e de UCP pode ser explorado para executar diversas transações em paralelo, aumentando o throughput do sistema (um maior número de transações podem ser executadas num determinado tempo); |
|              | Reduz o tempo médio de resposta para uma transação se completar após ser submetida, pois as transações curtas não precisam esperar que as longas terminem para serem iniciadas.                                                                                                                                                                                                                                                 |
| Desvantagens | Assegurar a consistência de transações exige trabalho adicional. É mais fácil assegurar as propriedades ACID em transações com execução sequencial do que em execuções concorrentes.                                                                                                                                                                                                                                            |

O fato de a execução das transações gerar dados consistentes não significa que produza o mesmo resultado. A mudança da ordem das transações pode provocar resultados diferentes. A execução sequencial de duas transações sempre produz um resultado consistente.

Uma execução concorrente pode produzir ou não um resultado consistente.

### Controle de transações

O SGBD assegura a consistência dos dados baseado nas transações. As transações dão mais flexibilidade e controle quando da mudança do conteúdo das tabelas e asseguram a consistência dos dados em caso de falhas nos processos do usuário ou no sistema.

Uma transação consiste de comandos DML (insert, update, delete, commit, rollback) que fazem uma mudança consistente nos dados. Por exemplo: uma transferência de valores entre duas contas bancárias implica no débito em uma conta e no crédito em outra no mesmo montante. Ambas as ações são realizadas ou são anuladas. O crédito não pode ser concretizado sem o correspondente débito.

Na maioria dos SGBDs, uma transação começa com o comando begin transaction.

![Comando begin transaction no PostgreSQL e SQLServer](/media/Implementação-de-Banco-de-Dados/aula9/Image2.png)

Uma exceção é o Oracle, no qual, quando damos qualquer comando, uma transação é aberta automaticamente pelo SGBD.

![Transação aberta no Oracle](/media/Implementação-de-Banco-de-Dados/aula9/Image3.png)

Uma transação termina quando aparece um dos seguintes comandos:

| Commit                                                                                              | Rollback                                                                   |
| --------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------- |
| Encerra a transação corrente, fazendo que todas as modificações pendentes passem a ser definitivas. | Encerra a transação corrente, desprezando todas as modificações pendentes. |

Todas as modificações feitas durante a transação são temporárias, até que a transação seja commited, ou seja, concretizada.

Situação do dado antes do commit ou do rollback:

- As operações de manipulação de dados primeiramente afetam o buffer do banco de dados;

- O usuário corrente pode rever os resultados das operações de manipulação de dados usando o comando select;

- Outros usuários não podem ver os resultados das operações de manipulação de dados do usuário corrente.

- As linhas afetadas ficam bloqueadas; outros usuários não podem modificar os dados existentes nas linhas afetadas.

Situação do dado depois do rollback:

- As mudanças são desfeitas. O conteúdo anterior do dado é restabelecido;

- Os bloqueios nas linhas afetadas são desfeitos; as linhas ficam disponíveis para que outros usuários possam executar novas alterações.

- Além do commit e do rollback, alguns SGBDs têm o SAVEPOINT, que serve para criar um ponto intermediário para fazermos o rollback, de forma que não precisemos desfazer a transação toda.

### PostgreSQL

PASSO 1: Abrir a transação.

![Abrindo a transação](/media/Implementação-de-Banco-de-Dados/aula9/Image4.jpeg)

PASSO 2: Criar a tabela teste com duas colunas.

![Criando a tabela Teste com duas colunas](/media/Implementação-de-Banco-de-Dados/aula9/Image5.jpeg)

PASSO 3: Confirmar a criação da tabela.

![Confirmando a criação da tabela](/media/Implementação-de-Banco-de-Dados/aula9/Image6.jpeg)

PASSO 4: Inserir uma linha na tabela.

![Inserindo uma linha na tabela](/media/Implementação-de-Banco-de-Dados/aula9/Image7.jpeg)

PASSO 5: Confirmar a inclusão.

![Confirmando a inclusão](/media/Implementação-de-Banco-de-Dados/aula9/Image8.jpeg)

PASSO 6: Criar um savepoint.

![Criando um savepoint](/media/Implementação-de-Banco-de-Dados/aula9/Image9.jpeg)

PASSO 7: Inserir uma segunda linha.

![Inserindo uma segunda linha](/media/Implementação-de-Banco-de-Dados/aula9/Image10.jpeg)

PASSO 8: Criar outro savepoint

![Criando outro savepoint](/media/Implementação-de-Banco-de-Dados/aula9/Image11.jpeg)

PASSO 9: Inserir uma terceira linha.

![Inserindo uma terceira linha](/media/Implementação-de-Banco-de-Dados/aula9/Image12.jpeg)

PASSO 10: Ver o conteúdo da tabela.

![Vendo o conteúdo da tabela](/media/Implementação-de-Banco-de-Dados/aula9/Image13.jpeg)

PASSO 11: Fazer rollback para savepoint.

Foram criados dois pontos de salvamento:

SAVEPOINT A - Após a inclusão da linha 1

SAVEPOINT B - Após a inclusão da linha 2

Portanto, se comandar um rollback para o ponto de salvamento B, a inclusão da linha 3 será desfeita.

Comando:

![Comando de rollback para o ponto de salvamento B](/media/Implementação-de-Banco-de-Dados/aula9/Image14.jpeg)

Verificando o resultado:

![Consultando a tabela após o rollback para o ponto de salvamento B](/media/Implementação-de-Banco-de-Dados/aula9/Image15.jpeg)

Note que agora somente aparecem as linhas 1 e 2.

PASSO 12: fazer rollback para savepoint A.

Comando:

![Comando de rollback para o ponto de salvamento A](/media/Implementação-de-Banco-de-Dados/aula9/Image16.jpeg)

Verificando o resultado:

![Consultando a tabela após o rollback para o ponto de salvamento A](/media/Implementação-de-Banco-de-Dados/aula9/Image17.jpeg)

Como esperado, agora só existe a linha 1. Será que você consegue voltar ao savepoint B e desta forma ter novamente a linha 2?

![Comando de rollback para o ponto de salvamento B](/media/Implementação-de-Banco-de-Dados/aula9/Image18.jpeg)

Não consegue, pois, uma vez realizado o rollback até um savepoint, ele é desmarcado e não fica mais disponível para uso.

PASSO 13: terminar a transação.

Uma transação pode terminar com commit ou rollback. Se você der commit, ela será efetivada e depois não adianta dar rollback, pois já fechou, sendo que o contrário também é verdadeiro: se der rollback, não adianta tentar dar commit depois.

Comando:

![Comando de rollback para terminar a transação](/media/Implementação-de-Banco-de-Dados/aula9/Image19.jpeg)

Se você der select na tabela teste agora, dirá que ela não existe; o rollback inclusive cancelou a criação da tabela.

![Comando select na tabela teste retorna um erro](/media/Implementação-de-Banco-de-Dados/aula9/Image20.jpeg)
