# Estruturas de Seleção

Ao desenvolver um algoritmo, muitas vezes é necessário tomar decisões ao longo da execução. Para isso, utilizamos as estruturas de seleção, também conhecidas como estruturas condicionais. Essas estruturas permitem que o fluxo do algoritmo siga caminhos diferentes de acordo com o resultado de uma condição lógica.

A estrutura de seleção funciona como um controle de fluxo que permite executar diferentes comandos dependendo do resultado de uma condição. Ou seja, se a condição for verdadeira, um ou mais comandos são executados; caso contrário, outros comandos podem ser realizados. Essa capacidade de “escolher caminhos” é fundamental para a construção de algoritmos adaptáveis, pois permite lidar com diferentes situações e entradas de maneira dinâmica. 

Existem dois tipos básicos de estruturas de seleção:
- **Estrutura de seleção simples**: Descrevem ações que serão executadas somente quando uma condição for satisfeita.
- **Estrutura de seleção composta**: Descrevem tanto as ações que serão executadas quando a condição for verdadeira, como as ações
para o caso contrário (condição falsa). 

A seguir, vamos conhecer a sintaxe básica dessa estrutura e entender como ela pode ser utilizada em nossos algoritmos.

- **Seleção Simples**
    ```
    se ( condição )  
    {  
        comando ; ou  
        < sequência de comandos separados por ; >  
    }
    ```

- **Seleção Composta**
    ```
    se ( condição )
    {
        comando ; ou
        < sequência de comandos separados por ; >
    }
    senao
    {
        comando ; ou
        < sequência de comandos separados por ; >
    }
    ```

## A execução do comando se:

- Primeiro, a **condição** é avaliada pela Unidade Aritmética e Lógica (ULA), sendo a condição uma expressão que possa retornar um valor lógico ($\color{red}{V}$ ou $\color{red}{F}$).
    - A condição pode ser uma simples expressão relacional formada de dois operandos do mesmo tipo e de um operador relacional ($\color{red}{=}$, $\color{red}{\neq}$, $\color{red}{>}$, $\color{red}{<}$, $\color{red}{\geq}$ e $\color{red}{\leq}$.).
    - A condição pode ser uma expressão lógica formada de pelo menos duas expressões relacionais que precisarão ser unidas por um dos operadores lógicos ($\color{red}{\land}$ ou $\color{red}{\lor}$).
- Se o valor retornado for $\color{red}{V}$, todos os comandos que se encontram entre o primeiro par de chaves serão executados; após a execução dos comandos, o fluxo do algoritmo passa para o primeiro comando depois do fechamento do bloco do senao, representado pelo símbolo $\color{red}{\}}$ (se existir); caso contrário, será executado o primeiro comando depois de $\color{red}{\}}$ do próprio bloco.
- Se o valor retornado for $\color{red}{F}$, todos os comandos que se encontram entre o primeiro par de chaves serão ignorados e, se existir o comando senao, serão executados os comandos que se encontram entre o segundo par de chaves; caso contrário, nada acontecerá e o fluxo do algoritmo seguirá para o próximo comando.

```{admonition} Estrutura condicional no cotidiano.

Podemos constatar que esta estrutura faz parte do nosso cotidiano:

- Se eu não tiver prova, vou à praia; senão vou estudar.
- Se eu tiver aumento, troco de carro; senão espero o 13º salário.
- Se minha média for maior ou igual a sete, passo direto; senão vou à prova final.

A única coisa diferente é a forma como iremos escrevê-la, pois as chaves **{ }** são **obrigatórias**, uma vez que delimitam os comandos que pertencem a cada bloco, assim como os parênteses **( )**, que delimitam a condição.

Essa é uma estrutura muito importante em algoritmos, pois nos dá a possibilidade de **verificar o que foi digitado pelo usuário** ou **qual o conteúdo de uma variável após o processamento**, entre outras aplicações.
```

## Exemplos