# Aula 8 - MEMÓRIA (PARTE 1)

## O que é memória?

Memória é o componente dentro da arquitetura e organização do computador com a função de armazenar os programas e os dados que serão manipulados pelo sistema operacional dentro dos ciclos de instrução.

A memória não pode ser considerada um componente único, mas sim um subsistema.

## Velocidade de processamento

Memória principal: Essa memória principal é a tão conhecida memória RAM, que leva aproximadamente 60 nanossegundos para processar um dado e transferir para a CPU.

Dentro da CPU, um dado é processado em aproximadamente 5 nanossegundos (isto significa 5 bilionésimos de segundo), ao contrário do processamento da memória principal

## Memória primária x secundária

Uma memória é volátil quando ela perde o conteúdo, quando não há alimentação de energia. Resumindo, **se o equipamento é desligado, seu conteúdo é perdido.**

**Memória primária:** São os componentes que fornecem dados e instruções para uso imediato, sendo voláteis. Basicamente, é formada pelos seguintes componentes: Registradores, Memória cache e Memória principal.

**Memória secundária:** São os componentes que provêm capacidade de armazenamento permanente (não voláteis). Exemplos de dispositivos de armazenamento secundário são: Discos Rígidos, Discos Óticos (CDs, DVDs, etc.) e Fitas.

![Memória primária x secundária]("/media/memoria_primaria_secundaria.png")

## Registradores

São dispositivos de armazenamento temporário, localizados na CPU, utilizados constantemente dentro do processo de execução das instruções. Por serem usados pela CPU, entende-se que são memórias muito rápidas. Na verdade, são consideradas as memórias mais rápidas existentes no sistema de computação. Porém, como seu objetivo é o armazenamento do conteúdo de memória a ser processado pela CPU, sua capacidade de armazenamento se limita à palavra daquele processador, normalmente variando de 8 a 64 Bits.

Mesmo sendo de baixa capacidade de armazenamento, os registradores são sempre construídos internamente no chip do processador.

## Memória cache

É uma memória criada justamente para diminuir os “estados de espera” entre CPU e memória principal, sendo muito mais rápida do que a memória RAM e com mais capacidade do que os registradores.

Ela tem a função de armazenar temporariamente conteúdos muito requisitados e fornecer as informações para a CPU de forma mais ágil, evitando que a memória principal tenha que ser consultada a todo momento, reduzindo a ociosidade da CPU.

O custo da memória cache é maior do que o da principal e menor do que o custo de registradores, o que justifica parte da solução encontrada.

**O custo de fabricação da memória cache é muito maior do que o da principal, não justificando a extinção da principal. Ou seja, não seria viável economicamente construir um computador somente com tecnologia de memória cache.**

## Princípio da localidade

Todo conteúdo consultado com mais frequência na memória principal é mantido de forma espelhada na memória cache, ou seja, este conteúdo não é apagado na memória principal, somente espelhado. Esse conteúdo consultado com frequência é verificado pelo princípio da localidade.

Princípio da localidade temporal: Baseia-se no fato de que um dado acessado recentemente tem mais chances de ser usado novamente do que um dado usado há mais tempo. Isso é uma realidade pois, quando um programa está em execução, uma variável pode ser consultada diversas vezes durante seu processamento, por exemplo, se houver uma rotina de loop ou sub-rotinas. **Sendo assim, o princípio da localidade temporal tende a manter os dados e instruções recentemente acessados.**

**Princípio da localidade espacial:** Baseia-se no fato de que há uma grande probabilidade de acesso para dados e instruções em endereços próximos àqueles acessados recentemente pela CPU (como no exemplo citado anteriormente). Durante a execução de um programa, normalmente as variáveis são criadas e armazenadas próximas umas às outras, dentro da memória principal.

**O conteúdo estará disponível na memória cache de imediato?**
Nem sempre. 
- Se a CPU busca um determinado dado e o encontra na cache, dá-se o que chamamos de cache hit, ou seja, conteúdo é localizado na cache;
- Se o caso for negativo, ou seja, se o dado não estiver presente na cache, sendo necessário requisitar o conteúdo para a memória principal, dá-se o que chamamos de cache miss.

Independente de cache miss ou cache hit, dentro do processo de fabricação da memória cache e suas metodologias de gravação de dados, o índice de cache hit é geralmente acima de 90%.

## Níveis de cache

**Cache L1 (nível 1):** Pequena memória inserida internamente no processador, ou seja, encapsulada dentro do núcleo de processamento. Também conhecida como cache on-die (no núcleo), exatamente por estar dentro do processador.
Alguns fabricantes identificam as memórias cache L1 como formada por dois elementos:
- Memória de instrução – acionada quando o processador está buscando uma instrução;
- Memória para dados – acionada se o processador estiver buscando um dado.

**Cache L2 (nível 2):** Localizada fora do núcleo, mas muito próxima do mesmo, sendo construída normalmente dentro do processador.

**Cache L3 (nível 3):** Em algumas arquiteturas, encontramos ainda o nível 3 na placa-mãe. Em outras, dentro do processador. Porém, usada como cache compartilhada entre os núcleos de um processador. Foi criada originalmente pelo fabricante AMD.

Caches são geralmente inclusivas. Isso significa que o conteúdo total de uma cache L1 está na cache L2, que também está na cache L3.

## Mapeamento de cache

**Caches totalmente associativas:** Neste método todas as linhas de cache da memória principal podem ser gravadas em qualquer localização na memória cache. É uma forma ineficiente porque a recuperação dos dados pode levar à varredura completa da cache para localizar o conteúdo.

**Caches de mapeamento direto:** O método de mapeamento direto limita a gravação das linhas de cache em locais específicos na cache. Porém, este índice pré-definido dos locais permite que a pesquisa do conteúdo na cache seja mais ágil.

![Caches de mapeamento direto]("/media/cache_mapeamento_direto.png")

**Caches associativas de conjunto:** Este tipo de mapeamento é um esquema híbrido entre o mapeamento totalmente associativo e o mapeamento direto. Ele permite que os problemas do mapeamento totalmente associativo (em que a cache inteira precisa ser varrida à procura de um endereço) e do mapeamento direto (em que ocorrem colisões) sejam minimizados. Nele, um mesmo endereço na memória principal pode ser armazenado em mais de um local (por vez) da cache, através da criação de vias de cache, ou seja, cada linha pode possuir n vias de cache, onde normalmente são de 2 a 4 vias.

![Caches associativas de conjunto]("/media/cache_associativa_conjunto.png")

## Métodos de substituição de dados

No que se refere à memória cache, é importante lembrar que existe um momento em que sua capacidade está lotada e os dados precisam ser substituídos, como, por exemplo, os das vias de cache.

![Métodos de substituição de dados]("/media/metodos_substituicao_dados.png")

## Políticas de escrita em cache na memória principal

Logicamente, é necessário que, em algum momento, os dados atualizados na memória cache também sejam atualizados na memória principal. Afinal, uma deve ser o espelho da outra.

**Write Through:** Consiste em atualizar o valor em cache e na MP simultaneamente.
**Write Back:** Consiste em atualizar a cache, porém ao enviar atualizações em blocos para a memória principal.
