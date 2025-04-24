# Lógica Proposicional

A lógica proposicional, cujas raízes remontam a Aristóteles, foi desenvolvida com o objetivo de modelar o raciocínio humano. Ela se baseia no uso de proposições, que são sentenças declarativas com valores de verdade bem definidos — podem ser verdadeiras ($\color{red}{V}$) ou falsas  ($\color{red}{F}$). A partir dessas proposições, novas expressões lógicas podem ser construídas utilizando conectivos lógicos fundamentais, tais como:

- **Negação** ($\neg$) — inverte o valor lógico de uma proposição; 
- **Conjunção** ($\wedge$) — representa a ideia de “e”; 
- **Disjunção** ($\vee$) — representa a ideia de “ou”; 
- **Condicional** ($\rightarrow$) — estabelece uma relação de “se… então…”. 

## Proposição

A lógica proposicional permite representar afirmações do dia a dia que apresentam fatos ou transmitem informações. Chamamos de proposição (também conhecida como **sentença** ou **declaração**) qualquer oração declarativa que possa ser classificada como verdadeira ou falsa. 

:::{include} exemplos.md
:start-after: <!-- Start Exemplo 1.1 -->
:end-before: <!-- End Exemplo 1.1 -->
:::

Toda proposição apresenta três caracteísticas obrigatórias:

1. sendo oração, tem sujeito e predicado;
2. é declarativa (não é exclamativa nem interrogativa);
3. deve assumir um, e somente um, dos dois valores lógicos possíveis: ou é verdadeira  ($\color{red}{V}$) ou é falsa  ($\color{red}{F}$).

A linguagem da lógica proposicional é construída a partir dos seguintes símbolos primitivos:

1. Um conjunto numerável de **variáveis proposicionais**:

$$V_{Prop} = p, q, r, \dots, p_{1}, q_{2}, \dots$$

2. Conectivos lógicos, que permitem a formação de novas proposições a partir das existentes:
    - Conjunção ($\wedge$ ou $\&\&$): representa “e”.
    - Disjunção ($\vee$ ou $||$): representa “ou”.
    - Negação ($\neg$ ou ~): representa “não”.
    - Implicação ($\rightarrow$): representa “se… então…”.
    - Parênteses ( ), utilizados para agrupar proposições e indicar a ordem das operações.

Esses elementos formam a base da sintaxe da lógica proposicional, permitindo a construção de expressões lógicas que podem ser avaliadas como verdadeiras ou falsas. 

```{admonition} Observação!
Assim como em muitos livros de lógica, letras minúsculas são utilizadas para representar proposições e, por isso, são chamadas **letras de proposição**.  
```

````{admonition} Atenção!
:class: warning
Para formalizar a atribuição de valores de verdade (ou valoração) às proposições, usamos a função:  
  
$$ v : V_{Prop} \rightarrow \{V, F\} $$
  
que atribui um valor de verdade a cada variável proposicional.
````

## Negação

A partir de uma propopsição $\color{red}{p}$ qualquer, sempre podemos construir outra, denomina **negação de8* $\color{red}{p}$ e indicada com o símbolo $\color{red}{\neg p}$.

:::{include} exemplos.md
:start-after: <!-- Start Exemplo 1.2 -->
:end-before: <!-- End Exemplo 1.2 -->
:::

```{admonition} Atenção!
:class: warning
A proposição $\color{red}{\neg p}$ tem sempre o valor lógico oposto de $\color{red}{p}$, isto é, $\color{red}{\neg p}$ é verdadeira quando $\color{red}{p}$ é falsa e $\color{red}{\neg p}$ é falsa quando $\color{red}{p}$ é verdadeira.
```

```{grid}
:gutter: 2

:::{grid-item}
<br> <div style="text-align: justify;">
Esse critério está resumido na tabela, denominada **tabela-verdade** da proposição $\color{red}{\neg p}$. A tabela-verdade permite saber o valor de verdade de uma proposição composta a partir de todos os possíveis valores de verdade dos seus componentes. Cada linha da tabela-verdade representa uma das possíveis combinações de valores de verdade. </div>
:::

:::{grid-item}
:::{include} tabela_verdade.md
:start-after: <!-- Start Tabela Verdade 1 -->
:end-before: <!-- End Tabela Verdade 1 -->
:::
:::
```


## Proposição Composta - Conectivos

Ao falar ou escrever, é comum combinarmos frases simples por meio de conectivos como **e** e **ou** para formar sentenças compostas mais completas e significativas. Da mesma maneira, na lógica proposicional, podemos construir novas proposições a partir de proposições já dadas, utilizando dois símbolos lógicos chamados **conectivos**: o conectivo $\color{red}{\wedge}$ (lê-se: **e**) e o conectivo $\color{red}{\vee}$ (lê-se: **ou**).


### Conjunção 

Colocando o conectivo $\color{red}{\wedge}$ entre duas proposições $\color{red}{p}$ e $\color{red}{q}$, obtemos uma nova proposição, $\color{red}{p \wedge q}$, denominada **conjunção** das sentenças $\color{red}{p}$ e $\color{red}{q}$. Os termos $\color{red}{p}$ e $\color{red}{q}$ são chamados de **elementos** ou **fatores** dessa expressão. Dessa forma, se combinarmos duas afirmações verdadeiras, como “Seres humanos são mamíferos” e “Mamíferos são mortais”, a proposição resultante, “Seres humanos são mamíferos **e** mamíferos são mortais”, também será verdadeira. Concordamos, então, que, se $\color{red}{p}$ e $\color{red}{q}$ forem proposições verdadeiras, a proposição $\color{red}{p \wedge q}$ (leia-se: $\color{red}{p}$ *e* $\color{red}{q}$) deverá ser considerada verdadeira.

:::{include} exemplos.md
:start-after: <!-- Start Exemplo 1.3 -->
:end-before: <!-- End Exemplo 1.3 -->
:::

```{admonition} Atenção!
:class: warning
A conjunção $\color{red}{p \wedge q}$ é verdadeira se, e somente se, $\color{red}{p}$ e $\color{red}{q}$ forem ambas verdadeiras. Se ao menos uma delas for falsa, então $\color{red}{p \wedge q}$ será falsa.  
```

A tabela verdade do conectivo $\color{red}{\wedge}$ apresenta os valores lógicos de $\color{red}{p \wedge q}$ para todas as combinações possíveis de valores lógicos de $\color{red}{p}$ e $\color{red}{q}$.


:::{include} tabela_verdade.md
:start-after: <!-- Start Tabela Verdade 2 -->
:end-before: <!-- End Tabela Verdade 2 -->
:::


### Disjunção

Colocando o conectivo $\color{red}{\vee}$ entre duas proposições $\color{red}{p}$ e $\color{red}{q}$, obtemos uma nova proposição, $\color{red}{p \vee q}$, denominada **disjunção** das sentenças $\color{red}{p}$ e $\color{red}{q}$. A disjunção representa a ideia de “ou”, ou seja, a proposição resultante $\color{red}{p \vee q}$ será verdadeira sempre que pelo menos uma das proposições $\color{red}{p}$ ou $\color{red}{q}$ for verdadeira. Os termos $\color{red}{p}$ e $\color{red}{q}$ são os **elementos** ou **fatores**, da disjunção. 

:::{include} exemplos.md
:start-after: <!-- Start Exemplo 1.4 -->
:end-before: <!-- End Exemplo 1.4 -->
:::

```{admonition} Atenção!
:class: warning
A disjunção $\color{red}{p \vee q}$ é verdadeira se ao menos uma das proposições $\color{red}{p}$ ou $\color{red}{q}$ é verdadeira; se $\color{red}{p}$ ou $\color{red}{q}$ são ambas falsas, então $\color{red}{p \vee q}$ é falsa.
```

A tabela verdade do conectivo $\color{red}{\vee}$ apresenta os valores lógicos de $\color{red}{p \vee q}$ para todas as combinações possíveis de valores lógicos de $\color{red}{p}$ e $\color{red}{q}$.

:::{include} tabela_verdade.md
:start-after: <!-- Start Tabela Verdade 3 -->
:end-before: <!-- End Tabela Verdade 3 -->
:::

## Condicionais

Ainda a partir de propoisções dadas podemos construir novas proposições mediante o emprego de outros dois símbolos lógicos chamados **condicionais**: o condicional "*se... então...*" (símbolo: $\color{red}{\rightarrow}$) e o bicondicional "*... se, somente se, ...*" (símbolo: $\color{red}{\leftrightarrow}$).

### Condicional Simples

Colocando o condicional $\color{red}{\rightarrow}$ entre duas proposições $\color{red}{p}$ e $\color{red}{q}$, obtemos uma nova proposição, $\color{red}{p \rightarrow q}$, que se lê: "se $\color{red}{p}$, então $\color{red}{q}$", "$\color{red}{p}$ é condicição suficiente para $\color{red}{q}$", "$\color{red}{q}$ é condição necessária para $\color{red}{p}$". O conectivo lógico aqui é o **condicional** e significa que a verdade de $\color{red}{p}$ implica, ou leva a, a verdade de $\color{red}{q}$. No condicional $\color{red}{p \rightarrow q}$, a proposição $\color{red}{p}$ é chamada de **antecedente** e $\color{red}{q}$ é chamada **consequente**.

:::{include} exemplos.md
:start-after: <!-- Start Exemplo 1.5 -->
:end-before: <!-- End Exemplo 1.5 -->
:::

```{admonition} Atenção!
:class: warning
O condicional $\color{red}{p \rightarrow q}$ é falso somente quando $\color{red}{p}$ é verdadeira e $\color{red}{q}$ é falsa; caso contrário, $\color{red}{p \rightarrow q}$ é verdadeiro.
```

A tabela verdade do condicional $\color{red}{\rightarrow}$ apresenta os valores lógicos de $\color{red}{p \rightarrow q}$ para todas as combinações possíveis de valores lógicos de $\color{red}{p}$ e $\color{red}{q}$.

:::{include} tabela_verdade.md
:start-after: <!-- Start Tabela Verdade 4 -->
:end-before: <!-- End Tabela Verdade 4 -->
:::

### Bicondicional

Colocando o bicondicional $\color{red}{\leftrightarrow}$ entre duas proposições $\color{red}{p}$ e $\color{red}{q}$, obtemos uma nova proposição, $\color{red}{p \leftrightarrow q}$, que se lê: "$\color{red}{p}$ se, e somente se $\color{red}{q}$", "$\color{red}{p}$ é condicição necessária e suficiente para $\color{red}{q}$", "$\color{red}{q}$ é condição necessária e suficiente para $\color{red}{p}$" ou "se $\color{red}{p}$, então $\color{red}{q}$ e reciprocamente". Ao contrário da conjunção, disjunção e do condicional, o conectivo bicondicional não é, de fato, um conectivo fundamental, é um atalho conveniente. A expressão $\color{red}{p \leftrightarrow q}$ é uma abreviatua de $\color{red}{(p \rightarrow q) \wedge (q \rightarrow p)}$.

:::{include} exemplos.md
:start-after: <!-- Start Exemplo 1.6 -->
:end-before: <!-- End Exemplo 1.6 -->
:::


```{admonition} Atenção!
:class: warning
O condicional $\color{red}{p \leftrightarrow q}$ é verdadeiro somente quando $\color{red}{p}$ e $\color{red}{q}$ são ambas verdadeiras ou ambas falsas; se isso não acontecer, o condicional $\color{red}{\leftrightarrow}$ é falso.
```

A tabela verdade do condicional $\color{red}{\leftrightarrow}$ apresenta os valores lógicos de $\color{red}{p \leftrightarrow q}$ para todas as combinações possíveis de valores lógicos de $\color{red}{p}$ e $\color{red}{q}$.


:::{include} tabela_verdade.md
:start-after: <!-- Start Tabela Verdade 5 -->
:end-before: <!-- End Tabela Verdade 5 -->
:::
