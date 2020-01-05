# Padrões de projeto ou Design Patterns

Um `padrão` descreve um conjunto composto por um contexto, um problema e uma solução, isto é, um padrão descreve uma solução para um problema em um contexto. Contudo, um padrão descreve uma solução que ja tenha sido utilizada com sucesso em mais de um contexto.Portanto, um padrão descreve soluções consolidadas.

## Conceitos
### Composição
Apesar de não estar entre os quatro elementos principais de uma linguagem orientada a objetos, a composição é um conceito que vem implícito quando se fala em objetos. a composição combinada com o uso de abstrações pode ser eficaz na solução de diferentes
problemas.

### Hook Methods
`Hook Methods` são métodos que podem ser sobrescritos pelas subclasses como forma de estender e/ou especializar o comportamento da classe.

![Hook Method](/media/engenharia_software/hookMethod.png).

Quando um hook method é utilizado a escolha é feita no momento em que o objeto é instaciando. Isso ocorre pois ao criarmos um novo objeto devemos escolher qual a classe concreta que será utilizada.

### Hook Class
`Hook Classes` são classes que possuem o comportamento definido em uma outra classe que compõe a classe principal.

Na hook class a implementação pode ser trocada a qualquer momento, bastando trocar a instância que foi configurada.