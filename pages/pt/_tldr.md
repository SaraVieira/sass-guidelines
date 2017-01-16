
# Longo Demais; Não Li

Este guia é um pouco longo e por vozes é bom resumir numa versão mais curta. Aqui podes encontrar um sumário do que falamos neste guia:

## Princípios Chave

* Ter um styleguide é tudo sobre **consistência**. Se discordas com algumas regras deste guia está tudo bem desde que mantenhas a consistência. [↩](#why-a-styleguide)
* O Sass deve ser mantido o mais simples possível. Evita sempre criar sistemas complexos a não ser que seja absolutamente necessário. [↩](#key-principles)
* Não te esqueças que às vezes *KISS* (Keep It Simple, Stupid) é melhor que *DRY* (Don’t Repeat Yourself). [↩](#key-principles)

## Sintaxe e formatação

* Indentação de dois (2) espaços, nada de tabulações [↩](#syntax--formatting)
* Linhas deverão ser as mais curtas possíveis, menos de 80 carateres. Podes sempre dividir código em várias linhas se for necessário [↩](#syntax--formatting)
* O CSS deverá estar bem escrito, possivelmente seguindo as [CSS Guidelines](http://cssguidelin.es) do Harry Roberts. [↩](#syntax--formatting)
* O espaço é grátis, usa para separar itens, regras e declarações. Não hesites em deixar linhas em branco, nunca é mau.[↩](#syntax--formatting)

### Strings

* Declarar o `@charset` no topo da guia de estilo é muito recomendado. [↩](#encoding)
* A não ser que estejas a aplicar identificadores de CSS, strings deverão ser sempre ser envolvidos em plicas. Com os URL's a mesma regra deve ser seguida. [↩](#strings-as-css-values)

### Números

* O Sass consegue fazer a distinção entre números inteiros e números com casas decimais por isso não usar zeros (0) não significativos à direita da vírgula mas zeros depois da vírgula devem ser usados pois ajudam na legibilidade. [↩](#zeros)
* Um valor de 0 não deve ter uma unidade. [↩](#units)
* Manipulações de números devem ser pensadas como operações aritméticas, não operações de strings. [↩](#units)
* Para melhorar a legibilidade, cálculos de alto nível devem ser envolvidas em parênteses. Também quando tens operações de matemática complexas estas podem ser dividas em pedaços mais pequenos. [↩](#calculations)
* Números mágicos magoam dramaticamente a manutenção do código e devem ser evitados em todas as ocasiões. Quando em duvida, explica o valor questionável extensivamente. [↩](#magic-numbers)

### Cores

* As cores devem ser escritas em HSL quando possível, se não usar RGB e em terceiro caso usar código hexadecimal (em letras minúsculas e na versão curta). Nomes de cores devem ser evitados. [↩](#color-formats)
* Usar `mix(..)` em vex de `darken(..)` e `lighten(..)` quando for para escurecer ou aclarar uma cor. [↩](#lightening-and-darkening-colors)

### Listas

* A não ser que seja um mapa directo de valores de CSS separados por espaços, listas devem ser sempre separadas por virgulas. [↩](#lists)
* Envolver em parênteses também deve ser ponderado para melhor legibilidade. [↩](#lists)
* Listas de uma linha não necessitam de uma vírgula antes, mas listas com várias linhas sim. [↩](#lists)

### Maps

* Maps que contenham mais de que um par devem ser escritos em várias linhas. [↩](#maps)
* Para ajudar na manutenção, o ultimo par de cada map deve ter uma virgula no fim. [↩](#maps)
* Chaves de um map que são strings devem ter aspas ou plicas como qualquer outro string. [↩](#maps)

### Ordenação de declarações

* O sistema usados para ordenação de declarações (alfabético, por tipo, etc.) não interessa desde que se este seja consistente. [↩](#declaration-sorting)

### Nesting de seletores

* Evitar nesting de seletores quando não é necessário (o que representa a maior parte dos casos). [↩](#selector-nesting)
* Usar nesting de seletores para pseudo-classes e pseudo-elementos. [↩](#selector-nesting)
* Media queries também podem ser nested dentro do seu seletor. [↩](#selector-nesting)

## Convenções de nome

* É melhor ficar pelas convenções de nome do CSS que são (exceto alguns erros) letra minúscula e separados por hífen. [↩](#naming-conventions)

## Comentários

* CSS é uma linguagem complicada; não hesites em escrever comentários extensivos sobre coisas que parecem (ou são) duvidosas. [↩](#commenting)
* Para variáveis, funções, mixins e placeholders estabelece uma API publica, usar comentários estilo SassDoc. [↩](#documentation)


## Variáveis

* Não usar a flag `!default` para alguma variável que faça parte da API publica que possa ser mudada com segurança. [↩](#default-flag)
* Não usar a flag `!global` no nível root porque pode ser uma violação da sintaxe do Sass no futuro. [↩](#global-flag)

## Extend

* Fica só por estender (`@extend`) placeholders, não seletores de CSS já existentes. [↩](#extend)
* Tenta estender um placeholder o mínimo de vezes possíveis para minimizar efeitos secundários. [↩](#extend)
