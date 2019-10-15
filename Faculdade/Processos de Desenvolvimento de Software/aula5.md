# Aula 5 - As atividades de teste no processo de desenvolvimento de software

A fase de teste tem como objetivo detectar possíveis defeitos ou erros que possam surgir na fase de implementação. Nessa fase, de testes, deve-se coletar os resultados e analisá-los e consertá-los antes de sua implantação.
Essa fase é essencial para aumentar a qualidade do produto ou sistema em que será implantado.

## Conceito de teste para o processo de desenvolvimento de software

**Principal objetivo dos testes de software:** revelar falhas para que sejam corrigidas até que o produto final atinja a qualidade desejada ou acordada.

- Testes funcionais da aplicação
- Avaliação da especificação de requisitos
- Avaliação de projeto técnico
- Verificações em outros documentos
- Testes de performance e capacidade
- Avaliação de interface
- Dentre outros

“Quanto mais cedo, defeitos forem encontrados antes da implementação do sistema, o custo de correção é menor em relação ao encontrado na fase de produção”  
**(Regra de Myers)**

**Defeito** – passo, processo ou definição de dados incorreto, por exemplo, uma instrução ou comando incorreto.  
**Engano** – ação humana, por exemplo, tomada pelo programador, que produz um resultado incorreto.  
**Erro** – diferença entre o valor obtido e o valor esperado. Qualquer resultado incorreto ou inesperado na execução do programa.  
**Falha** – produção de uma saída incorreta com relação à especificação.

**CAUSA:** Engano; Defeito; Erro.  
**CONSEQUÊNCIA:** Falha

1.  **Teste:** Processo definido com intenção de encontrar um erro.
1.  **Objetivo:** Encontrar um erro que ainda não foi descoberto. Um teste bem sucedido corresponde à descoberta de um erro não previsto.
1.  **Critério:** Definição de uma métrica que, após análise do comportamento do sistema, atenda o critério.
1.  **Procedimento:** Conjunto de instruções para a realização de testes.
1.  **“Script” de teste:** É uma representação definida de um procedimento teste.

## Processo de Teste de Software

- **Planejamento dos testes:** “Garantir que os testes sejam preparados antes do fim da implementação do produto”.
- **Execução dos Testes:** “Executar os casos e procedimentos de teste especificados e comparar os resultados esperados e obtidos, registrando esses resultados”.
- **Controle dos testes:** “Garantir que os testes planejados sejam executados corretamente e seus resultados possam ser registrados através da sua monitoração constante”.

**Teste caixa preta (teste funcional):** Neste teste <u>o objetivo é testar todas as entradas e saídas desejadas</u>, mediante uma determinada entrada definida de dados. Aqui não se está preocupado com o código, **cada saída indesejada é vista como um erro**. Os mecanismos internos do sistema não são levados em conta.

**Teste caixa branca (teste estrutural):** Neste caso o <u>objetivo principal é testar o código dos componentes do sistema, quanto a sua estrutura e construção</u>. Os mecanismos internos do sistema serão analisados e suas representações lógicas também. Este teste não exclui a necessidade do Teste Caixa Preta, uma vez que o funcionamento interno do sistema ou produto pode corresponder logicamente, podendo produzir uma saída diferente da esperada. É comum se encontrar partes do código que nunca foram testadas.

## Classificação dos testes

### Quanto à utilização do código:

**Testes estáticos:** São testes realizados pela **análise estática e visual do código fonte**. Os componentes do software são verificados **sem que o produto seja executado**. <u>O principal objetivo dessa técnica é identificar erros de programação</u>, tais como: Prática ruins de programação; Práticas ruins; Erros de sintaxe; Falhas de segurança. Todos os caminhos de execução, processamento e exibição de valores são examinados. Como consequência, erros mais comuns são descobertos mais rapidamente.

**Testes dinâmicos:** São testes baseados na **execução do código do programa**. Informações que são inseridas nas **rotinas de entrada e saída de dados**. Além disso, são verificados itens como: O tempo de resposta; A performance da aplicação; A capacidade do software se adaptar a diferentes ambientes; O comportamento funcional. <u>Permite que problemas mais sutis sejam identificados</u>. As chances de um “bug” passar por uma análise estática e uma análise dinâmica, sem ser rastreado é consideravelmente baixa. <u>O teste dinâmico consegue dar mais segurança e confiabilidade ao produto final</u>.

### Classificação quanto ao nível dos testes:

**Testes de unidade (teste unitário):** Teste em nível de módulo, componente ou classe. É o teste cujo **objetivo é um “pedaço do código”**, ou em alguns módulos definidos que representam uma única unidade. A documentação do projeto define a quantidade de módulos a serem testados. Em geral, realizado pelo próprio programador, ou pelo seu par (em caso de ser usada nas metodologias ágeis).  
**Testes de integração:** Teste utilizado para **garantir que um ou mais componentes combinados, ou unidades, não contenham erros**. Podemos dizer que um teste de integração é composto por diversos testes de unidade. A cada teste de unidade encerrado, a unidade é integrada ao sistema já pronto, formando um nova versão, que deve ser testado em conjunto. Testa-se, em geral, as interfaces entre os componentes.  
**Teste de sistemas:** Teste do sistema **como um todo ou de uma entrega parcial**, contendo todos os elementos.  
**Testes de validação:** Teste realizado **após a integração de todos os módulos ou unidades** do sistema.

![Ferramentas automação teste](/media/processos_dev_software/ferramentas_automacao_testes.png)

**Partes fundamentais de um processo de desenvolvimento de software:** Planejamento, execução e controle.

**Visão interna:** É a visão que representa os componentes do sistema, a relação entre os componentes, o funcionamento dos componentes e a interconexão com outros sistemas.

São problemas encontrados na implementação do processo de desenvolvimento de software:
**resistência a mudanças**, erro no uso de metodologias a serem adotadas, adoção de ferramentas inadequadas, **desconhecimento do escopo do projeto** e inadequação da equipe.
