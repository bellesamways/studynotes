# Aula 3 - Descrição textual de casos de uso

O diagrama de caso de uso é útil, na medida em que nos fornece uma visão geral das funcionalidades do sistema (conjunto de casos de uso) e dos atores que com elas se relacionam.
É pobre na medida em que não entendemos como a interação ocorre em cada caso de uso.

**O diagrama é um sumário gráfico do conjunto de casos de uso (funcionalidades) de um sistema.**

Se o tempo destinado ao modelo de casos de uso for pouco, concentre-se na especificação ou descrição dos casos de uso e esqueça o diagrama.

## Formatos para especificar casos de uso

- **Resumido:** resumo de um parágrafo, contendo o cenário principal do caso de uso e o cenário de sucesso. Deve utilizar na análise inicial de requisitos para obter uma ideia do assunto e o escopo do caso de uso.
- **Informal:** múltiplos parágrafos que cobrem vários cenários de uso. Deve usar na mesma condição do resumido.
- **Completo:** todos os cenários (principal e alternativos) são descritos em detalhes, com seções adicionais, complementando a especificação com elementos que definem os pré e pós-condições. Deve usar depois que muitos casos tiverem sido descritos em resumo ou informal, geralmente durante a fase de análise de requisitos e de sistemas. Para casos de uso relevantes, tende a ser o mais adequado.

**Dicas para especificações de casos de uso:**

1. Não use detalhes de implementação ou de determinada tecnologia em suas especificações.
2. Procure não associar casos de uso a telas de sistemas.
3. Utilize um formato de especificação que deixa o diálogo mais claro entre ator e caso de uso. O modelo tem duas colunas. Na primeira, descrevemos as ações do ator, e na segunda as ações do sistema.
4. Os casos de uso incluídos (chamados de include) ou estendidos (chamados por extends) também devem ter descrição textual, podendo estar no formato resumido ou informal.
5. Algumas perguntas podem ajudar no detalhamento dos cenários principal e alternativos. Exemplo: Quando tudo ocorre na normalidade (com sucesso), qual o comportamento do sistema?
6. Quando um passo for muito complicado, ele pode vir a ser um novo caso de uso, que se relacionará com o caso original pelo estereótipo include.
7. Faça casos de uso enxutos, pois casos longos podem não ser lidos em sua totalidade.

![tabela casos de uso](../../media/modelagem_de_sistemas/aula03/img/img007.png)