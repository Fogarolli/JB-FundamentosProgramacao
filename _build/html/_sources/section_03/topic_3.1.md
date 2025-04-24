
# Estrutura Sequencial e Conceitos Fundamentais


A estrutura sequencial representa o modelo mais simples e direto de execução de um algoritmo. Nesse tipo de estrutura, as instruções são realizadas uma após a outra, respeitando exatamente a ordem em que foram escritas. Ou seja, cada comando só é executado após a conclusão do comando anterior, garantindo um fluxo contínuo e previsível. De modo geral, um algoritmo sequencial segue uma sequência lógica de passos: inicia-se com a declaração das **variáveis**, passa pelos **comandos de entrada** de dados e/ou **atribuições**, realiza o **processamento das informações** e, por fim, apresenta os resultados por meio dos **comandos de saída** de dados.

Essa estrutura é a base para a construção de algoritmos e programas, servindo como ponto de partida antes da introdução de estruturas mais complexas, como seleção e repetição. A seguir, vamos explorar cada um desses elementos fundamentais que compõem a estrutura sequencial: variáveis, expressões, atribuição, comandos de entrada e saída.

## Variável

Uma **variável** é um local na memória principal, ou seja, um endereço que armazena um determinado conteúdo. Em linguagens de alto nível, é possível atribuir um nome a esse endereço para facilitar a programação. O conteúdo armazenado pode assumir diferentes tipos, como inteiro, real, caractere, lógico, entre outros. Em algoritmos, as variáveis serão definidas no início, por meio do comando definido:

```
tipo da variável   nome da variável   ;
```

```{admonition} Atenção!
:class: warning
Quando formos dar nome às variáveis, se faz necessário seguirmos algumas regras. É bom ressaltar que estas regras irão variar de acordo com a linguagem. As seguintes regras:
1. O primeiro caractere é uma **letra**.
2. Se houver mais de um caractere, só poderemos usar: **letra** ou **algarismo**.
3. Nomes de variáveis escritas com letras maiúsculas serão diferentes de letras minúsculas. Lembre-se: media é **diferente** de MEDIA.
4. Nenhuma palavra reservada poderá ser nome de uma variável.
```

:::{include} exemplos.md
:start-after: <!-- Start Exemplos 01 -->
:end-before: <!-- End Exemplos 01 -->
:::

### Tipos de variávels

- **Númericas**: Variáveis numéricas são aquelas que armazenam dados numéricos, podendo ser divididas em duas classes:
    - **int**: Os números inteiros são aqueles que **não** possuem componentes decimais ou fracionários, podendo ser positivos ou negativos.
    - **real** (também chamado de **float**): Os números reais são aqueles que podem possuir componentes decimais ou fracionários, podendo também ser positivos ou reais.
- **string** (também chamado de **str**): Também conhecida como caractere, alfanumérica ou literal. Esse tipo de variável armazena dados que contêm letras dígitos e/ou símbolos especiais.
- **logico** (também chamado de **booleano** ou **bool**): Também conhecido como booleano. É representado no algoritmo pelo dois únicos valores lógicos possíveis: verdadeiro ou falso.

### Vetores e Matrizes

Na programação, frequentemente lidamos com a necessidade de armazenar e manipular coleções de dados. Para isso, utilizamos estruturas de dados como vetores e matrizes, que permitem organizar essas informações de forma eficiente. Um vetor é um arranjo de elementos armazenados um após o outro, todos sob o mesmo nome, mas acessados por meio de um índice. A ideia é semelhante à de uma matriz linha na matemática, ou seja, uma sequência de elementos dispostos em uma única linha com várias colunas. Essa estrutura é útil quando precisamos armazenar uma série de valores relacionados, como as notas de uma turma, os preços de uma lista de produtos ou qualquer outro conjunto de dados onde a ordem importa e cada elemento pode ser identificado por sua posição.

Quando precisamos representar dados em duas dimensões — por exemplo, em linhas e colunas — utilizamos as matrizes. Assim como os vetores, as matrizes armazenam elementos do mesmo tipo, mas organizados em formato de tabela, permitindo o acesso a cada elemento por meio de dois índices: um para a linha e outro para a coluna. Essa estrutura é especialmente útil em situações como armazenamento de tabelas numéricas, imagens (que podem ser vistas como matrizes de pixels) ou qualquer cenário onde as informações estejam naturalmente dispostas em duas dimensões. A seguir, apresentaremos a sintaxe de declaração de vetores e matrizes.

```
tipo da variável   vator[dimensão]   ;
tipo da variável   matriz[dimensão][dimensão]   ;
```



## Expressões

O conceito de expressão em termos computacionais está intimamente ligado ao conceito de expressão (ou fórmula) matemática, onde um conjunto de variáveis e constantes numéricas relaciona-se por meio de operadores compondo uma fórmula que, uma vez avaliada, resulta num valor. As expressões dividem-se em:

- **Aritméticas**. Expressões aritméticas são aquelas cujo resultado da avaliação é do tipo numérico, seja ele inteiro ou real. Somente o uso de operadores aritméticos e variáveis numéricas é permitido em expressões deste tipo.
    - Como exemplo de operadores e expressões aritméticas temos: soma ($\color{red}{+}$), subtração ($\color{red}{-}$), multiplicação ($\color{red}{\times}$), divisão ($\color{red}{\div}$), exponenciação ($\color{red}{x^{y}}$) e o resto ($\color{red}{\%}$).

- **Relacionais**. Uma expressão relacional, ou simplesmente relação, é uma comparação realizada entre dois valores de mesmo tipo básico. Estes valores são representados na relação através de constantes, variáveis ou expressões aritméticas.
    - Como exemplos de operadores relacionais matematicamente conhecidos temos: $\color{red}{=}$, $\color{red}{\neq}$, $\color{red}{>}$, $\color{red}{<}$, $\color{red}{\geq}$ e $\color{red}{\leq}$.

- **Lógica ou Boolena**. Denomina-se expressão lógica a expressão cujos operadores são lógicos e cujos operandos são relações, constantes e/ou variáveis do tipo lógico.
    - Como exemplo de operadores lógicos, matematicamente conhecidos, temos: $\color{red}{\land}$, $\color{red}{\lor}$, $\color{red}{\neg}$, $\color{red}{\rightarrow}$ e $\color{red}{\leftrightarrow}$.

## Atribuição

É a principal forma de se armazenar um dado em uma variável. Esse comando permite que você forneça um valor a uma variável, onde o tipo desse valor tem de ser compatível com a variável.

```
identificador  <-  expressão  ;
```

- **identificador**: é o nome da variável à qual está sendo atribuído um valor.
- **<-**: é o símbolo de atribuição, formado pelos sinais $\color{red}{<}$ e $\color{red}{-}$.
- **expressão**: pode ser uma expressão aritmética, uma expressão lógica ou literal cuja avaliação (resultado) é atribuída ao identificador (variável).
- **;** (porto e vírgula): finaliza o comando.

:::{include} exemplos.md
:start-after: <!-- Start Exemplos 02 -->
:end-before: <!-- End Exemplos 02 -->
:::

## Comando de Saída

É o comando responsável por exibir um resultado, uma informação ao usuário. O valor de cada variável é buscado na memória e inserido em um dispositivo de saída. Através desse comando o computador pode emitir os resultados e outras mensagens para o usuário através da tela do computador ou uma impressora.

```
imprima  expressão_ou_variável_ou_constantes ;
```

:::{include} algoritmos.md
:start-after: <!-- Start Algoritmo 07 -->
:end-before: <!-- End Algoritmo 07 -->
:::

:::{include} algoritmos.md
:start-after: <!-- Start Algoritmo 08 -->
:end-before: <!-- End Algoritmo 08 -->
:::



## Comando de Entrada

É o comando que permite que o usuário digite dados, possibilitando um “diálogo com o computador”. O dado digitado é armazenado temporariamente em um registrador e, depois, copiado para a posição de memória indicada no comando. Lembre-se de que o nome de uma variável representa uma posição de memória.

```
leia  nome_de_uma_variável ;
```

:::{include} algoritmos.md
:start-after: <!-- Start Algoritmo 09 -->
:end-before: <!-- End Algoritmo 09 -->
:::

:::{include} algoritmos.md
:start-after: <!-- Start Algoritmo 10 -->
:end-before: <!-- End Algoritmo 10 -->
:::


## Exemplos