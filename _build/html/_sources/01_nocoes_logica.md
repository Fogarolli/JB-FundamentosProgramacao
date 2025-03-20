# Noções de Lógica

A lógica é a disciplina que estuda os argumentos, analisando quais são válidos e quais não são. Um argumento é composto por um conjunto de **proposições**, onde cada proposição é uma **afirmação** que pode ser classificada como **verdadeira** (V) ou **falsa** (F). Para garantir a validade do raciocínio, a lógica se baseia em princípios fundamentais conhecidos como leis da lógica, entre as quais se destacam a **lei da identidade** (uma proposição é idêntica a si mesma), a **lei da não-contradição** (uma proposição não pode ser simultaneamente verdadeira e falsa) e a **lei do terceiro excluído** (uma proposição é verdadeira ou falsa, não havendo uma terceira possibilidade).

A lógica formal estabelece um método estruturado e rigoroso para a formulação de argumentos, sendo essencial em diversas áreas do conhecimento, como investigações científicas e processos de tomada de decisão. No campo da computação e da programação, a lógica desempenha um papel central, pois fornece a base para a construção de algoritmos, a definição de estruturas de controle e a modelagem de processos computacionais. Entre os diversos ramos da lógica formal, a **lógica proposicional** se destaca por sua aplicabilidade na representação e manipulação de informações de maneira precisa. Utilizando operadores lógicos e regras bem definidas, ela permite estabelecer relações entre proposições, servindo como fundamento para circuitos digitais, linguagens formais e verificação de programas. Neste capítulo, exploraremos os princípios da lógica proposicional.


## Lógica Proposicional

A lógica proposicional, cujas raízes remontam a Aristóteles, foi desenvolvida com o objetivo de modelar o raciocínio humano. Ela se baseia no uso de proposições, que são sentenças declarativas com valores de verdade bem definidos — podem ser verdadeiras (V) ou falsas (F). A partir dessas proposições, novas expressões lógicas podem ser construídas utilizando conectivos lógicos fundamentais, tais como:

- **Negação** ($\neg$) — inverte o valor lógico de uma proposição; 
- **Conjunção** ($\wedge$) — representa a ideia de “e”; 
- **Disjunção** ($\vee$) — representa a ideia de “ou”; 
- **Condicional** ($\rightarrow$) — estabelece uma relação de “se… então…”. 


## Proposição

A lógica proposicional permite representar afirmações do dia a dia que apresentam fatos ou transmitem informações. Chamamos de proposição (também conhecida como **sentença** ou **declaração**) qualquer oração declarativa que possa ser classificada como verdadeira ou falsa. 

```{admonition} Exemplos!
:class: examples dropdown
a. Macapá é a capital do estado do Amapá. `(  )`  
b. Ele é muito talentoso. `(  )`  
c. Cinco é menor que doze. ($5 < 12$) `(  )`  
d. Nove vezes três é igual a vinte e cinco. ($9 \times 3 = 25$) `(  )`  
e. Dez é um número inteiro. ($10 \in \mathbb{Z}$) `(  )`  
```{dropdown} Análises
A sentença **(a)** é uma proposição, pois expressa um fato verificável e verdadeiro. A sentença **(b)** não é falsa nem verdadeira, pois "ele" não está especificado, tornando a sentença ambígua; por isso, (b) não é uma proposição. A sentença **(c)** é uma proposição, pois expressa um fato matemático verdadeiro. A sentença **(d)** é uma proposição, pois pode ser classificada como falsa (o correto seria $9 \times 3 = 27$). A sentença **(e)** é uma proposição, pois é uma afirmação verdadeira sobre um número.
```

Toda proposição apresenta três caracteísticas obrigatórias:

1. sendo oração, tem sujeito e predicado;
2. é declarativa (não é exclamativa nem interrogativa);
3. deve assumir um, e somente um, dos dois valores lógicos possíveis: ou é verdadeira (V) ou é falsa (F).

A linguagem da lógica proposicional é construída a partir dos seguintes símbolos primitivos:

1. Um conjunto numerável de **variáveis proposicionais**:

$$V_{Prop} = p, q, r, \dots, p_{1}, q_{2}, \dots$$

```{admonition} Observação!
Assim como em muitos livros de lógica, letras minúsculas são utilizadas para representar proposições e, por isso, são chamadas **letras de proposição**.  
```

2. Conectivos lógicos, que permitem a formação de novas proposições a partir das existentes:
    - Conjunção ($\wedge$): representa “e”.
    - Disjunção ($\vee$): representa “ou”.
    - Negação ($\neg$): representa “não”.
    - Implicação ($\rightarrow$): representa “se… então…”.
    - Parênteses ( ), utilizados para agrupar proposições e indicar a ordem das operações.

Esses elementos formam a base da sintaxe da lógica proposicional, permitindo a construção de expressões lógicas que podem ser avaliadas como verdadeiras ou falsas. 


````{admonition} Atenção!
:class: warning
Para formalizar a atribuição de valores de verdade (ou valoração) às proposições, usamos a função:  
  
$\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;  v : V_{Prop} \rightarrow \{V, F\}$  
  
que atribui um valor de verdade a cada variável proposicional.
````


## Negação

A partir de uma propopsição $p$ qualquer, sempre podemos construir outra, denomina **negação de $p$** e indicada com o símbolo $\neg p$.

```{admonition} Exemplos!
:class: examples dropdown

| Proposição |  Negação |
|----------|------------|
| a. O céu é azul.                  | $\neg $a. O céu não é azul.                   |
| b. O número 7 é um número primo.  | $\neg $b. O número 7 não é um número primo.   |
| c. 5 é um número par.             | $\neg $c. 5 não é um número par.              |
| d. A porta está aberta.           | $\neg $d. A porta não está aberta.            |
| e. Hoje é segunda-feira.          | $\neg $e. Hoje não é segunda-feira.           |
````


```{admonition} Atenção!
:class: warning
A proposição $\neg p$ tem sempre o valor lógico oposto de $p$, isto é, $\neg p$ é verdadeira quando $p$ é falsa e $\neg p$ é falsa quando $p$ é verdadeira.
```


```{grid}
:gutter: 2

:::{grid-item}  
<br><br>
Esse critério está resumido na tabela, denominada **tabela-verdade** da proposição $\neg p$. A tabela-verdade permite saber o valor de verdade de uma proposição composta a partir de todos os possíveis valores de verdade dos seus componentes. Cada linha da tabela-verdade representa uma das 
possíveis combinações de valores de verdade.
:::

:::{grid-item}
<!DOCTYPE html>
<html lang="pt">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tabela Verdade</title>
    <link rel="stylesheet" href="/Users/rafaelvieira/Documents/00_Codigos/JB-FundamentosProgramacao/_statics/custom.css">
</head>
<body>
    <p class="table-title"><strong>Tabela Verdade da Negação</strong></p>
    <div class="table-container">
        <table>
            <thead>
                <tr>
                    <th>p</th>
                    <th>&not; p</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td>V</td>
                    <td>F</td>
                </tr>
                <tr>
                    <td>F</td>
                    <td>V</td>
                </tr>
            </tbody>
        </table>
    </div>
</body>
</html>
:::
```





## Proposição Composta - Conectivos

Ao falar ou escrever, é comum combinarmos frases simples por meio de conectivos como **e** e **ou** para formar sentenças compostas mais completas e significativas. Da mesma maneira, na lógica proposicional, podemos construir novas proposições a partir de proposições já dadas, utilizando dois símbolos lógicos chamados **conectivos**: o conectivo $\wedge$ (lê-se: e) e o conectivo $\vee$ (lê-se: ou).

### Conjunção 

Colocando o conectivo $\wedge$ entre duas proposições $p$ e $q$, obtemos uma nova proposição, $p \wedge q$, denominada **conjunção** das sentenças $p$ e $q$. Os termos $p$ e $q$ são chamados de **elementos** ou **fatores** dessa expressão. Dessa forma, se combinarmos duas afirmações verdadeiras, como “Seres humanos são mamíferos” e “Mamíferos são mortais”, a proposição resultante, “Seres humanos são mamíferos **e** mamíferos são mortais”, também será verdadeira. Concordamos, então, que, se $p$ e $q$ forem proposições verdadeiras, a proposição $p \wedge q$ (leia-se: $p$ *e* $q$) deverá ser considerada verdadeira.

```{admonition} Exemplos!
:class: examples dropdown
1.  
    $a$. Macapá é a capital do estado do Amapá. `(  )`  
    $b$. A capital do Amapá é quente. `(  )`  
    $a \wedge b$. Macapá é a **capital** do estado do Amapá *e* a capital do Amapá é quente. `(  )`   
2.  
    $p$. O Sol nasce no leste. `(  )`  
    $q$. A água ferve a 100°C ao nível do mar. `(  )`  
    $p \wedge q$. O Sol nasce no leste *e* a água ferve a 100°C ao nível do mar. `(  )`  
````

```{admonition} Atenção!
:class: warning
A conjunção $p \wedge q$ é verdadeira se, e somente se, $p$ e $q$ forem ambas verdadeiras. Se ao menos uma delas for falsa, então $p \wedge q$ será falsa.  
```

A tabela verdade do conectivo $\wedge$ apresenta os valores lógicos de $p \wedge q$ para todas as combinações possíveis de valores lógicos de $p$ e $q$.


<!DOCTYPE html>
<html lang="pt">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tabela Verdade</title>
    <link rel="stylesheet" href="/Users/rafaelvieira/Documents/00_Codigos/JB-FundamentosProgramacao/_statics/custom.css">
</head>
<body>
    <p class="table-title"><strong>Tabela Verdade da Conjunção p ∧ q</strong></p>
    <div class="table-container">
        <table>
            <thead>
                <tr>
                    <th>p</th>
                    <th>q</th>
                    <th>p ∧ q</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td>V</td>
                    <td>V</td>
                    <td>V</td>
                </tr>
                <tr>
                    <td>V</td>
                    <td>F</td>
                    <td>F</td>
                </tr>
                <tr>
                    <td>F</td>
                    <td>V</td>
                    <td>F</td>
                </tr>
                <tr>
                    <td>F</td>
                    <td>F</td>
                    <td>F</td>
                </tr>
            </tbody>
        </table>
    </div>
</body>
</html>


### Disjunção

Colocando o conectivo $\vee$ entre duas proposições $p$ e $q$, obtemos uma nova proposição, $p \vee q$, denominada **disjunção** das sentenças $p$ e $q$. A disjunção representa a ideia de “ou”, ou seja, a proposição resultante $p \vee q$ será verdadeira sempre que pelo menos uma das proposições $p$ ou $q$ for verdadeira. Os termos $p$ e $q$ são os **elementos** ou **fatores**, da disjunção. 

```{admonition} Exemplos!
:class: examples dropdown
1.  
    $a$. Os gorilas são mamiferos. `(  )`  
    $b$. A África é um país. `(  )`  
    $a \vee b$. Os gorilas são mamiferos $\vee$ A África é um país.`(  )`     
2.  
    $p$. Um quadrado tem seia lados. `(  )`  
    $q$. A terra é plana. `(  )`   
    $p \vee q$. Um quadrado tem seia lados $\vee$ A terra e plana. `(  )`    
````

```{admonition} Atenção!
:class: warning
A disjunção $p \vee q$ é verdadeira se ao menos uma das proposições $p$ ou $q$ é verdadeira; se $p$ ou $q$ são ambas falsas, então $p \vee q$ é falsa.
```

A tabela verdade do conectivo $\vee$ apresenta os valores lógicos de $p \vee q$ para todas as combinações possíveis de valores lógicos de $p$ e $q$.

<!DOCTYPE html>
<html lang="pt">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tabela Verdade</title>
    <link rel="stylesheet" type="text/css" href="/Users/rafaelvieira/Documents/00_Codigos/JB-FundamentosProgramacao/_statics/custom.css">
</head>
<body>
    <p class="table-title"><strong>Tabela Verdade da Disjunção p v q</strong></p>
    <div class="table-container">
        <table>
            <thead>
                <tr>
                    <th>p</th>
                    <th>q</th>
                    <th>p v q</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td>V</td>
                    <td>V</td>
                    <td>V</td>
                </tr>
                <tr>
                    <td>V</td>
                    <td>F</td>
                    <td>V</td>
                </tr>
                <tr>
                    <td>F</td>
                    <td>V</td>
                    <td>V</td>
                </tr>
                <tr>
                    <td>F</td>
                    <td>F</td>
                    <td>F</td>
                </tr>
            </tbody>
        </table>
    </div>
</body>
</html>


## Condicionais

Ainda a partir de propoisções dadas podemos construir novas proposições mediante o emprego de outros dois símbolos lógicos chamados **condicionais**: o condicional "*se... então...*" (símbolo: $\rightarrow$) e o bicondicional "*... se, somente se, ...*" (símbolo: $\leftrightarrow$).

### Condicional`

Colocando o condicional $\rightarrow$ entre duas proposições $p$ e $q$, obtemos uma nova proposição, $p \rightarrow q$, que se lê: "se $p$, então $q$", "$p$ é condicição suficiente para $q$", "$q$ é condição necessária para $p$". O conectivo lógico aqui é o **condicional** e significa que a verdade de $p$ implica, ou leva a, a verdade de $q$. No condicional $p \rightarrow q$, a proposição $p$ é chamada de **antecedente** e $q$ é chamada **consequente**.

```{admonition} Exemplos!
:class: examples dropdown
a. Se chover, então o solo ficará molhado.  
b. Se um número for divisível por 2, então ele é um número par.  
c. Se João estudar, então ele passará na prova.  
d. Se a lâmpada estiver queimada, então ela não acenderá.  
e. Se um aluno faltar muitas aulas, então ele poderá ser reprovado.  
````

```{admonition} Atenção!
:class: warning
O condicional $p \rightarrow q$ é falso somente quando $p$ é verdadeira e $q$ é falsa; caso contrário, $p \rightarrow q$ é verdadeiro.
```

A tabela verdade do condicional $\rightarrow$ apresenta os valores lógicos de $p \rightarrow q$ para todas as combinações possíveis de valores lógicos de $p$ e $q$.


<!DOCTYPE html>
<html lang="pt">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tabela Verdade</title>
    <link rel="stylesheet" href="/Users/rafaelvieira/Documents/00_Codigos/JB-FundamentosProgramacao/_statics/custom.css">
</head>
<body>
    <p class="table-title"><strong> Tabela Verdade do Condicional p &rarr; q </p></strong> 
    <div class="table-container">
        <table>
            <thead>
                <tr>
                    <th>p</th>
                    <th>q</th>
                    <th>p &rarr; q</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td>V</td>
                    <td>V</td>
                    <td>V</td>
                </tr>
                <tr>
                    <td>V</td>
                    <td>F</td>
                    <td>F</td>
                </tr>
                <tr>
                    <td>F</td>
                    <td>V</td>
                    <td>V</td>
                </tr>
                <tr>
                    <td>F</td>
                    <td>F</td>
                    <td>V</td>
                </tr>
            </tbody>
        </table>
    </div>
</body>
</html>


### Bicondicional

Colocando o bicondicional $\leftrightarrow$ entre duas proposições $p$ e $q$, obtemos uma nova proposição, $p \leftrightarrow q$, que se lê: "$p$ se, e somente se $q$", "$p$ é condicição necessária e suficiente para $q$", "$q$ é condição necessária e suficiente para $p$" ou "se $p$, então $q$ e reciprocamente". Ao contrário da conjunção, disjunção e do condicional, o conectivo bicondicional não é, de fato, um conectivo fundamental, é um atalho conveniente. A expressão $p \leftrightarrow q$ é uma abreviatua de $(p \rightarrow q) \wedge (q \rightarrow p)$.

```{admonition} Exemplos!
:class: examples dropdown
a. Uma figura é um quadrado se, e somente se, possui quatro lados iguais e quatro ângulos retos.  
b. Um número é par se, e somente se, é divisível por 2.  
c. Uma pessoa é maior de idade se, e somente se, tem 18 anos ou mais.  
d. Um número é múltiplo de 3 se, e somente se, a soma de seus dígitos for um múltiplo de 3.  
e. Um número é primo se, e somente se, ele for divisível apenas por 1 e por ele mesmo.  
````

```{admonition} Atenção!
:class: warning
O condicional $p \leftrightarrow q$ é verdadeiro somente quando $p$ e $q$ são ambas verdadeiras ou ambas falsas; se isso não acontecer, o condicional $\leftrightarrow$ é falso.
```

A tabela verdade do condicional $\leftrightarrow$ apresenta os valores lógicos de $p \leftrightarrow q$ para todas as combinações possíveis de valores lógicos de $p$ e $q$.



<!DOCTYPE html>
<html lang="pt">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tabela Verdade</title>
    <link rel="stylesheet" href="/Users/rafaelvieira/Documents/00_Codigos/JB-FundamentosProgramacao/_statics/custom.css">
</head>
<body>
    <p class="table-title"><strong> Tabela Verdade do Bicondicional p &harr; q </p></strong>
    <div class="table-container">
        <table>
            <thead>
                <tr>
                    <th>p</th>
                    <th>q</th>
                    <th>p &harr; q</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td>V</td>
                    <td>V</td>
                    <td>V</td>
                </tr>
                <tr>
                    <td>V</td>
                    <td>F</td>
                    <td>F</td>
                </tr>
                <tr>
                    <td>F</td>
                    <td>V</td>
                    <td>F</td>
                </tr>
                <tr>
                    <td>F</td>
                    <td>F</td>
                    <td>V</td>
                </tr>
            </tbody>
        </table>
    </div>
</body>
</html>

<br><br><br>

# Fórmula Bem-Formadas

Como já vimos, podemos combinar variáveis proposicionais, conectivos lógicos e parênteses para formar novas expressões lógicas. Por exemplo:

<p align="center">(p &rarr; q) ∧ (q &rarr; p)</p>

No entanto, para que uma expressão seja considerada válida, ela deve obedecer a certas **regras de sintaxe**, que determinam quais sequências de símbolos formam expressões bem-formadas. Por exemplo, a seguinte cadeia de símbolos:

<p align="center"> p))  ∧ &rarr; ∧ qp</p>

não é uma expressão válida. Uma sequência válida que obedece às regras de formação é chamada de **fórmula bem-formada** (**fbf**). Formalmente, uma fbf é definida de maneira indutiva pelas seguintes regras:

1. uma variável proposicional $p$ é uma fbf.
2. se $q$ é uma fbf, então $\neg q$ é uma fbf.
3. se $p$ e $q$ são fbfs, então ($p \wedge q$), ($p \vee q$) e ($p \rightarrow q$) também são fbfs.  

Para reduzir o número de parênteses necessários em uma fbf, estipulamos uma ordem de aplicação dos conectivos lógicos. Essa ordem de precedência segue a seguinte hierarquia:

1.	Parênteses ( ) – utilizados para agrupar expressões e definir explicitamente a ordem das operações.
2.	Negação $\neg$ – operador unário que tem prioridade sobre os conectivos binários.
3.	Conjunção $\wedge$ e Disjunção $\vee$ – avaliadas antes das implicações.
4.	Condicional $\rightarrow$ – processada após os operadores anteriores.
5.	Bicondicional $\leftrightarrow$ – tem a menor precedência, sendo avaliada por último.

Essa convenção reduz a necessidade de parênteses em expressões lógicas, tornando a notação mais enxuta e intuitiva.

## Tautologias

Seja $v$ uma fbf formada a partir de proposições ($p$, $q$, $r$, $\cdots$) por meio do uso de conectivos lógicos ($\wedge$, $\vee$), modificadores ($\neg$) ou condicionais ($\rightarrow$, $\leftrightarrow$). Dizemos que $v$ é uma **tautologia** ou **proposição logicamente verdadeira** quando seu valor lógico é sempre V (verdadeiro), independentemente dos valores lógicos das proposições $p$, $q$, $r$, etc.

```{admonition} Exemplos!
:class: examples dropdown
a. Se Pedro está em casa, então Pedro está em casa.  
b. Ou hoje é segunda-feira, ou hoje não é segunda-feira.  
c. Se está chovendo, então está chovendo, ou não está chovendo.
````

```{admonition} Atenção!
:class: warning
Uma tautologia é intrinsecamente verdadeira devido à sua própria estrutura, ou seja, sua veracidade não depende dos valores lógicos atribuídos às suas variáveis proposicionais.
```

A tabela verdade da tautologia apresenta os valores lógicos da fbf para todas as combinações possíveis de valores lógicos de suas variáveis proposicionais.

<!DOCTYPE html>
<html lang="pt">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tabela Verdade</title>
    <link rel="stylesheet" href="/Users/rafaelvieira/Documents/00_Codigos/JB-FundamentosProgramacao/_statics/custom.css">
</head>
<body>
    <p class="table-title"><strong> Tabela Verdade da Tautologia </strong></p>
    <div class="table-container">
        <table>
            <thead>
                <tr>
                    <th>p</th>
                    <th>q</th>
                    <th>r</th>
                    <th>(p v q)</th>
                    <th>(p v q v r)</th>                    
                    <th>(p v q) &rarr; (p v q v r)</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td> </td>
                    <td> </td>
                    <td> </td>
                    <td> </td>
                    <td> </td>
                    <td> </td>
                </tr>
                <tr>
                    <td> </td>
                    <td> </td>
                    <td> </td>
                    <td> </td>
                    <td> </td>
                    <td> </td>
                </tr>
                <tr>
                    <td> </td>
                    <td> </td>
                    <td> </td>
                    <td> </td>
                    <td> </td>
                    <td> </td>
                </tr>
                <tr>
                    <td> </td>
                    <td> </td>
                    <td> </td>
                    <td> </td>
                    <td> </td>
                    <td> </td>
                </tr>
                <tr>
                    <td> </td>
                    <td> </td>
                    <td> </td>
                    <td> </td>
                    <td> </td>
                    <td> </td>
                </tr>
                <tr>
                    <td> </td>
                    <td> </td>
                    <td> </td>
                    <td> </td>
                    <td> </td>
                    <td> </td>
                </tr>
                <tr>
                    <td> </td>
                    <td> </td>
                    <td> </td>
                    <td> </td>
                    <td> </td>
                    <td> </td>
                </tr>
                <tr>
                    <td> </td>
                    <td> </td>
                    <td> </td>
                    <td> </td>
                    <td> </td>
                    <td> </td>
                </tr>
            </tbody>
        </table>
    </div>
</body>
</html>


## Contradições 

Seja $f$ uma fbf formada a partir de proposições ($p$, $q$, $r$, $\cdots$) por meio do uso de conectivos lógicos ($\wedge$, $\vee$), modificadores ($\neg$) ou condicionais ($\rightarrow$, $\leftrightarrow$). Dizemos que $f$ é uma **contradição** ou **proposição logicamente falsa** quando seu valor lógico é sempre F (falso), independentemente dos valores lógicos das proposições $p$, $q$, $r$, etc.

```{admonition} Exemplos!
:class: examples dropdown
a. Está chovendo e não está chovendo ao mesmo tempo.  
b. Um número é maior que 10 e menor que 5 ao mesmo tempo.  
c. Se João é um estudante, então João não é um estudante.  
````

```{admonition} Atenção!
:class: warning
Uma contradição é intrinsecamente falsa devido à sua própria estrutura, ou seja, sua falsidade não depende dos valores lógicos atribuídos às suas variáveis proposicionais,
```

A tabela verdade de uma contradição apresenta os valores lógicos para todas as combinações possíveis de valores lógicos das variaveis proposicionais.


<!DOCTYPE html>
<html lang="pt">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tabela Verdade</title>
    <link rel="stylesheet" href="/Users/rafaelvieira/Documents/00_Codigos/JB-FundamentosProgramacao/_statics/custom.css">
</head>
<body>
    <p class="table-title"></strong> Tabela Verdade da Contradição </strong></p>
    <div class="table-container">
        <table>
            <thead>
                <tr>
                    <th>p</th>
                    <th>q</th>
                    <th>r</th>
                    <th>(p v q)</th>
                    <th>(¬p ∧ ¬q ∧ ¬r)</th>                    
                    <th>(p ∨ q) ∧ (¬p ∧ ¬q ∧ ¬r)</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td> </td>
                    <td> </td>
                    <td> </td>
                    <td> </td>
                    <td> </td>
                    <td> </td>
                </tr>
                <tr>
                    <td> </td>
                    <td> </td>
                    <td> </td>
                    <td> </td>
                    <td> </td>
                    <td> </td>
                </tr>
                <tr>
                    <td> </td>
                    <td> </td>
                    <td> </td>
                    <td> </td>
                    <td> </td>
                    <td> </td>
                </tr>
                <tr>
                    <td> </td>
                    <td> </td>
                    <td> </td>
                    <td> </td>
                    <td> </td>
                    <td> </td>
                </tr>
                <tr>
                    <td> </td>
                    <td> </td>
                    <td> </td>
                    <td> </td>
                    <td> </td>
                    <td> </td>
                </tr>
                <tr>
                    <td> </td>
                    <td> </td>
                    <td> </td>
                    <td> </td>
                    <td> </td>
                    <td> </td>
                </tr>
                <tr>
                    <td> </td>
                    <td> </td>
                    <td> </td>
                    <td> </td>
                    <td> </td>
                    <td> </td>
                </tr>
                <tr>
                    <td> </td>
                    <td> </td>
                    <td> </td>
                    <td> </td>
                    <td> </td>
                    <td> </td>
                </tr>
            </tbody>
        </table>
    </div>
</body>
</html>


## Relação de Implicação

Dadas as proposições $p$ e $q$, dizemos que "$p$ **implica** $q$" quando na tabela verdade de $p$ e $q$ não ocorre **VF** em nenhuma linha, isto é, quando não temos simultaneamente $p$ verdadeira e $q$ falsa. Quando $p$ implica em $q$, indicamos $p \Rightarrow q$.


1. Notemos que $p$ implica $q$ quando o condicional $p \rightarrow q$ é verdeiro.
2. Todo teorema é uma implicação da forma: 
<p align="center">hipótese &rArr; tese</p>

```{admonition} Exemplos!
:class: examples dropdown
a. Se uma pessoa é brasileira, então ela nasceu no Brasil.  
b. Se um carro está sem combustível, então ele não funciona.  
c. Se hoje é segunda-feira, então amanhã será terça-feira.  
```

## Relação de Equivalência

Dadas as proposições $p$ e $q$, dizemos que "$p$ é **equivalente** a $q$" quando $p$ e $q$ têm tabelas-verdades iguais, isto é, quando $p$ e $q$ têm sempre o mesmo valor lógico. Quando $p$ é equivalente a $q$, indicamos: $p \Leftrightarrow q$

1. Notemos que $p$ equivale a $q$ quando o condicional $p \leftrightarrow q$ é verdadeiro.
2. Todo teorema cujo recíproco também é verdadeiro é uma equivalência. 
<p align="center">hipótese &hArr; tese</p>


```{admonition} Exemplos!
:class: examples dropdown
a. “Está chovendo ou não está chovendo” é equivalente a “Isso sempre será verdadeiro.”  
b. “Se hoje é segunda-feira, então amanhã será terça-feira” é equivalente a “Se amanhã não for terça-feira, então hoje não é segunda-feira.”  
```

## Sentenças Abertas e Quantificadores

Orações que contêm variáveis são chamadas **funções proposicionais** ou **sentenças abertas**. Tais orações não são prosições, pois seu valor lógico (V ou F) é discutível, depende do valor dado às variáveis.

Uma sentença aberta é uma expressão que contém variáveis e, por isso, não pode ser classificada como verdadeira ou falsa até que essas variáveis sejam substituídas por valores específicos. Dessa forma, sentenças abertas não são proposições, pois seu valor lógico depende da atribuição de valores às variáveis.

Há, entretanto, duas maneiras de transformar sentenças abertas em proposições:

1. **atribuindo valores específicos às variáveis**, tornando-a uma afirmação concreta, passível de ser classificada como verdadeira ou falsa.
2. **utilizando quantificadores**, que indicam a abrangência da afirmação sobre um conjunto de elementos.

Os **quantificadores** são símbolos utilizados para expressar a quantidade de elementos do universo de discurso para os quais uma sentença aberta se torna verdadeira.

- **Quantificador Universal** ($\forall$): representado pelo símbolo $\forall$, é lido como “para todo”, “para cada” ou “qualquer que seja”. Ele indica que a sentença é válida para todos os elementos de um determinado conjunto.
- **Quantificador Existencial** ($\exists$): representado pelo símbolo $\exists$, é lido como “existe”, “existe pelo menos um” ou “há um”. Ele afirma que a sentença é verdadeira para pelo menos um elemento do conjunto.
- **Quantificador Existencial Único** ($\exists!$ ou $\exists |$): Representado pelo símbolo $\exists!$ (ou, em algumas notações, $\exists |$), é lido como “existe um único”, “existe um e apenas um”, enfatizando que há exatamente um elemento que satisfaz a sentença.

```{admonition} Exemplos!
:class: examples dropdown
a. $\forall x \in \mathbb{N}, x + x = 2x.$  
   (*Para todo número natural $x$, a soma de $x$ consigo mesmo é igual ao dobro de $x$.*)

b. $\exists x \in \mathbb{Z}, x^2 = 9.$  
   (*Existe pelo menos um número inteiro $x$ cujo quadrado é 9.*)

c. $\exists! x \in \mathbb{R}, x^2 = 0.$  
   (*Existe um único número real $x$ cujo quadrado é 0.*)

d. $\forall x \in \mathbb{Z}, x + 0 = x.$  
   (*Para todo número inteiro $x$, a soma de $x$ com 0 é igual a $x$.*)
```

## Como Negar Proposições Compostas

A negação de uma proposição composta segue regras específicas baseadas na equivalência lógica. É importante ter cuidado ao negar proposições, especialmente quando se trata de proposições compostas, pois a aplicação incorreta da negação pode levar a erros na interpretação lógica. O uso adequado de parênteses e a compreensão da estrutura da proposição original são fundamentais para evitar ambiguidades. 

A seguir, veremos como negar diferentes tipos de proposições.

### Negação de uma Conjunção

A negação de uma conjunção segue a seguinte equivalência lógica:

$$\neg(p \wedge q) \Leftrightarrow \neg p \vee \neg q$$

Ou seja, a negação de ”$p$ e $q$ são verdadeiros” equivale a dizer que “pelo menos um deles é falso”, ou seja, ”$p$ é falso ou $q$ é falso”.

```{admonition} Exemplos!
:class: examples dropdown
a. João estuda e Maria trabalha.  
$\neg$ a. João não estuda ou Maria não trabalha.

b. O número $x$ é positivo e par.    
$\neg$ b. O número $x$ não é positivo ou não é par.
```

### Negação de uma Disjunção

A negação de uma disjunção segue a seguinte equivalência lógica:

$$\neg(p \vee q) \Leftrightarrow \neg p \wedge \neg q$$

Ou seja, a negação de “pelo menos um entre $p$ e $q$ é verdadeiro” equivale a dizer que “ambos são falsos”.

```{admonition} Exemplos!
:class: examples dropdown
a. Pedro gosta de matemática ou de física.  
$\neg$ a. Pedro não gosta de matemática e não gosta de física.

b. O número $x$ é par ou múltiplo de 3.  
$\neg$ b. O número $x$ não é par e não é múltiplo de 3.
```

### Negação de um Condicional

A negação de uma proposição condicional segue a seguinte equivalência lógica:

$$\neg(p \rightarrow q) \Leftrightarrow p \wedge \neg q$$

Ou seja, a negação de “se $p$, então $q$” equivale a dizer que ”$p$ acontece, mas $q$ não acontece”.

```{admonition} Exemplos!
:class: examples dropdown
a. Se chove, então levo guarda-chuva.  
$\neg$ a. Chove e não levo guarda-chuva.

ba Se um número é divisível por 4, então ele é par.  
$\neg$ b. O número é divisível por 4 e não é par.
```

### Negação de Proposições Quantificadas

A negação de proposições quantificadas segue uma regra geral: o quantificador é trocado pelo seu oposto, e a proposição dentro dele é negada.

- Quantificador Universal:
    
    Uma sentença quantificada com o quanttificador universal, do tipo $(\forall x)(p(x))$, é negada assim: substitui-se o quantificador existencial e nega-se $p(x)$, obtendo: $(\exists x)(\neg p(x))$. Ou seja, a negação de “para todo $x$, $p(x)$ é verdadeiro” é “existe pelo menos um $x$ tal que $p(x)$ é falso”.

    ```{admonition} Exemplos!
    :class: examples dropdown
    a. Todos os alunos passaram na prova.  
    $\neg$ a. Existe pelo menos um aluno que não passou na prova.

    b. Para todo número real $x$, $x^2 \geq 0$.  
    $\neg$ b. Existe pelo menos um número real $x$ tal que $x^2 < 0$.
    ```

- Quantifacador Existencial:
    
    Uma sentença quantificada com o quanttificador universal, do tipo $(\exists x)(p(x))$, é negada assim: substitui-se o quantificador existencial e nega-se $p(x)$, obtendo: $(\forall x)(\neg p(x))$. Ou seja, a negação de “existe pelo menos um $x$ tal que $p(x)$ é verdadeiro” é “para todo $x$, $p(x)$ é falso”.

    ```{admonition} Exemplos!
    :class: examples dropdown
    a. Existe um aluno que entende lógica proposicional.  
    $\neg$ a. Nenhum aluno entende lógica proposicional.

    b. Existe um número natural $x$ tal que $x + 5 = 2$.  
    $\neg$ b. Para todo número natural $x$, $x + 5 \neq 2$.
    ```










