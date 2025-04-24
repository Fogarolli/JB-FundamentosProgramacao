# Fórmula Bem-Formadas

Como já vimos, podemos combinar variáveis proposicionais, conectivos lógicos e parênteses para formar novas expressões lógicas. Por exemplo:

$$
(p \rightarrow q) \wedge (q \rightarrow p)
$$

No entanto, para que uma expressão seja considerada válida, ela deve obedecer a certas **regras de sintaxe**, que determinam quais sequências de símbolos formam **expressões bem-formadas**. Por exemplo, a seguinte cadeia de símbolos:

$$
p)) \; \wedge \rightarrow \wedge \; qp \vee rq
$$
não é uma expressão válida. Uma sequência válida que obedece às regras de formação é chamada de **fórmula bem-formada** (**fbf**). Formalmente, uma fbf é definida de maneira indutiva pelas seguintes regras:

1. uma variável proposicional $\color{red}{p}$ é uma fbf.
2. se $\color{red}{q}$ é uma fbf, então $\color{red}{\neg q}$ é uma fbf.
3. se $\color{red}{p}$ e $\color{red}{q}$ são fbfs, então ($\color{red}{p \wedge q}$), ($\color{red}{p \vee q}$) e ($\color{red}{p \rightarrow q}$) também são fbfs.  

Para reduzir o número de parênteses necessários em uma fbf, estipulamos uma ordem de aplicação dos conectivos lógicos. Essa ordem de precedência segue a seguinte hierarquia:

1.	Parênteses ( ) – utilizados para agrupar expressões e definir explicitamente a ordem das operações.
2.	Negação $\color{red}{\neg}$ – operador unário que tem prioridade sobre os conectivos binários.
3.	Conjunção $\color{red}{\wedge}$ e Disjunção $\color{red}{\vee}$ – avaliadas antes das implicações.
4.	Condicional $\color{red}{\rightarrow}$ – processada após os operadores anteriores.
5.	Bicondicional $\color{red}{\leftrightarrow}$ – tem a menor precedência, sendo avaliada por último.

```{admonition} Nota!
Essa convenção reduz a necessidade de parênteses em expressões lógicas, tornando a notação mais enxuta e intuitiva.
```

## Tautologias

Seja $\color{red}{v}$ uma fbf formada a partir de proposições ($\color{red}{p}$, $\color{red}{q}$, $\color{red}{r}$, $\color{red}{\cdots}$) por meio do uso de conectivos lógicos ($\color{red}{\wedge}$, $\color{red}{\vee}$), modificadores ($\color{red}{\neg}$) ou condicionais ($\color{red}{\rightarrow}$, $\color{red}{\leftrightarrow}$). Dizemos que $\color{red}{v}$ é uma **tautologia** ou **proposição logicamente verdadeira** quando seu valor lógico é sempre V (verdadeiro), independentemente dos valores lógicos das proposições $\color{red}{p}$, $\color{red}{q}$, $\color{red}{r}$, etc.


:::{include} exemplos.md
:start-after: <!-- Start Exemplo 1.7 -->
:end-before: <!-- End Exemplo 1.7 -->
:::

```{admonition} Atenção!
:class: warning
Uma tautologia é intrinsecamente verdadeira devido à sua própria estrutura, ou seja, sua veracidade não depende dos valores lógicos atribuídos às suas variáveis proposicionais.
```

A tabela verdade da tautologia apresenta os valores lógicos da fbf para todas as combinações possíveis de valores lógicos de suas variáveis proposicionais.

:::{include} tabela_verdade.md
:start-after: <!-- Start Tabela Verdade 6 -->
:end-before: <!-- End Tabela Verdade 6 -->
:::

## Contradições 

Seja $\color{red}{f}$ uma fbf formada a partir de proposições ($\color{red}{p}$, $\color{red}{q}$, $\color{red}{r}$, $\color{red}{\cdots}$) por meio do uso de conectivos lógicos ($\color{red}{\wedge}$, $\color{red}{\vee}$), modificadores ($\color{red}{\neg}$) ou condicionais ($\color{red}{\rightarrow}$, $\color{red}{\leftrightarrow}$). Dizemos que $\color{red}{f}$ é uma **contradição** ou **proposição logicamente falsa** quando seu valor lógico é sempre F (falso), independentemente dos valores lógicos das proposições $\color{red}{p}$, $\color{red}{q}$, $\color{red}{r}$, etc.


:::{include} exemplos.md
:start-after: <!-- Start Exemplo 1.8 -->
:end-before: <!-- End Exemplo 1.8 -->
:::

```{admonition} Atenção!
:class: warning
Uma contradição é intrinsecamente falsa devido à sua própria estrutura, ou seja, sua falsidade não depende dos valores lógicos atribuídos às suas variáveis proposicionais,
```

A tabela verdade de uma contradição apresenta os valores lógicos para todas as combinações possíveis de valores lógicos das variaveis proposicionais.

:::{include} tabela_verdade.md
:start-after: <!-- Start Tabela Verdade 7 -->
:end-before: <!-- End Tabela Verdade 7 -->
:::

## Relação de Implicação

Dadas as proposições $\color{red}{p}$ e $\color{red}{q}$, dizemos que "$\color{red}{p}$ **implica** $\color{red}{q}$" quando na tabela verdade de $\color{red}{p}$ e $\color{red}{q}$ não ocorre **VF** em nenhuma linha, isto é, quando não temos simultaneamente $\color{red}{p}$ verdadeira e $\color{red}{q}$ falsa. Quando $\color{red}{p}$ implica em $\color{red}{q}$, indicamos $\color{red}{p \Rightarrow q}$.


1. Notemos que $\color{red}{p}$ implica $\color{red}{q}$ quando o condicional $\color{red}{p \rightarrow q}$ é verdeiro.
2. Todo teorema é uma implicação da forma: 

$$
\text{hipótese} \Rightarrow \text{tese}
$$

:::{include} exemplos.md
:start-after: <!-- Start Exemplo 1.9 -->
:end-before: <!-- End Exemplo 1.9 -->
:::

## Relação de Equivalência

Dadas as proposições $\color{red}{p}$ e $\color{red}{q}$, dizemos que "$\color{red}{p}$ é **equivalente** a $\color{red}{q}$" quando $\color{red}{p}$ e $\color{red}{q}$ têm tabelas-verdades iguais, isto é, quando $\color{red}{p}$ e $\color{red}{q}$ têm sempre o mesmo valor lógico. Quando $\color{red}{p}$ é equivalente a $\color{red}{q}$, indicamos: $\color{red}{p \Leftrightarrow q}$

1. Notemos que $\color{red}{p}$ equivale a $\color{red}{q}$ quando o condicional $\color{red}{p \leftrightarrow q}$ é verdadeiro.
2. Todo teorema cujo recíproco também é verdadeiro é uma equivalência. 

$$
\text{hipótese} \Leftrightarrow \text{tese}
$$

:::{include} exemplos.md
:start-after: <!-- Start Exemplo 1.10 -->
:end-before: <!-- End Exemplo 1.10 -->
:::

## Sentenças Abertas e Quantificadores

Orações que contêm variáveis são chamadas **funções proposicionais** ou **sentenças abertas**. Tais orações não são prosições, pois seu valor lógico (V ou F) é discutível, depende do valor dado às variáveis.

Uma sentença aberta é uma expressão que contém variáveis e, por isso, não pode ser classificada como verdadeira ou falsa até que essas variáveis sejam substituídas por valores específicos. Dessa forma, sentenças abertas não são proposições, pois seu valor lógico depende da atribuição de valores às variáveis.

```{admonition} Atenção!!
:class: warning
Há, entretanto, duas maneiras de transformar sentenças abertas em proposições:

1. **atribuindo valores específicos às variáveis**, tornando-a uma afirmação concreta, passível de ser classificada como verdadeira ou falsa.
2. **utilizando quantificadores**, que indicam a abrangência da afirmação sobre um conjunto de elementos.
```

Os **quantificadores** são símbolos utilizados para expressar a quantidade de elementos do universo de discurso para os quais uma sentença aberta se torna verdadeira.

- **Quantificador Universal** ($\color{red}{\forall}$): representado pelo símbolo $\color{red}{\forall}$, é lido como “para todo”, “para cada” ou “qualquer que seja”. Ele indica que a sentença é válida para todos os elementos de um determinado conjunto.
- **Quantificador Existencial** ($\color{red}{\exists}$): representado pelo símbolo $\color{red}{\exists}$, é lido como “existe”, “existe pelo menos um” ou “há um”. Ele afirma que a sentença é verdadeira para pelo menos um elemento do conjunto.
- **Quantificador Existencial Único** ($\color{red}{\exists!}$ ou $\color{red}{\exists |}$): Representado pelo símbolo $\color{red}{\exists!}$ (ou, em algumas notações, $\color{red}{\exists |}$), é lido como “existe um único”, “existe um e apenas um”, enfatizando que há exatamente um elemento que satisfaz a sentença.

:::{include} exemplos.md
:start-after: <!-- Start Exemplo 1.11 -->
:end-before: <!-- End Exemplo 1.11 -->
:::



## Como Negar Proposições Compostas

A negação de uma proposição composta segue regras específicas baseadas na equivalência lógica. É importante ter cuidado ao negar proposições, especialmente quando se trata de proposições compostas, pois a aplicação incorreta da negação pode levar a erros na interpretação lógica. O uso adequado de parênteses e a compreensão da estrutura da proposição original são fundamentais para evitar ambiguidades. 

A seguir, veremos como negar diferentes tipos de proposições.


### Negação de uma Conjunção

A negação de uma conjunção segue a seguinte equivalência lógica:

$$\neg(p \wedge q) \Leftrightarrow \neg p \vee \neg q$$

Ou seja, a negação de ”$\color{red}{p}$ e $\color{red}{q}$ são verdadeiros” equivale a dizer que “pelo menos um deles é falso”, ou seja, ”$\color{red}{p}$ é falso ou $\color{red}{q}$ é falso”.

:::{include} exemplos.md
:start-after: <!-- Start Exemplo 1.12 -->
:end-before: <!-- End Exemplo 1.12 -->
:::


### Negação de uma Disjunção

A negação de uma disjunção segue a seguinte equivalência lógica:

$$\neg(p \vee q) \Leftrightarrow \neg p \wedge \neg q$$

Ou seja, a negação de “pelo menos um entre $\color{red}{p}$ e $\color{red}{q}$ é verdadeiro” equivale a dizer que “ambos são falsos”.

:::{include} exemplos.md
:start-after: <!-- Start Exemplo 1.13 -->
:end-before: <!-- End Exemplo 1.13 -->
:::


### Negação de um Condicional

A negação de uma proposição condicional segue a seguinte equivalência lógica:

$$\neg(p \rightarrow q) \Leftrightarrow p \wedge \neg q$$

Ou seja, a negação de “se $\color{red}{p}$, então $\color{red}{q}$” equivale a dizer que ”$\color{red}{p}$ acontece, mas $\color{red}{q}$ não acontece”.

:::{include} exemplos.md
:start-after: <!-- Start Exemplo 1.14 -->
:end-before: <!-- End Exemplo 1.14 -->
:::

### Negação de Proposições Quantificadas

A negação de proposições quantificadas segue uma regra geral: o quantificador é trocado pelo seu oposto, e a proposição dentro dele é negada.

- **Quantificador Universal**:
    
    Uma sentença quantificada com o quanttificador universal, do tipo $\color{red}{(\forall x)(p(x))}$, é negada assim: substitui-se o quantificador existencial e nega-se $\color{red}{p(x)}$, obtendo: $\color{red}{(\exists x)(\neg p(x))}$. Ou seja, a negação de “para todo $\color{red}{x}$, $\color{red}{p(x)}$ é verdadeiro” é “existe pelo menos um $\color{red}{x}$ tal que $\color{red}{p(x)}$ é falso”.

    :::{include} exemplos.md
    :start-after: <!-- Start Exemplo 1.15 -->
    :end-before: <!-- End Exemplo 1.15 -->
    :::

- **Quantifacador Existencial**:
    
    Uma sentença quantificada com o quanttificador universal, do tipo $\color{red}{(\exists x)(p(x))}$, é negada assim: substitui-se o quantificador existencial e nega-se $\color{red}{p(x)}$, obtendo: $\color{red}{(\forall x)(\neg p(x))}$. Ou seja, a negação de “existe pelo menos um $\color{red}{x}$ tal que $\color{red}{p(x)}$ é verdadeiro” é “para todo $\color{red}{x}$, $\color{red}{p(x)}$ é falso”.

    :::{include} exemplos.md
    :start-after: <!-- Start Exemplo 1.16 -->
    :end-before: <!-- End Exemplo 1.16 -->
    :::