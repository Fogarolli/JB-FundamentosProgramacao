# Estruturas de Repetição

Em muitos problemas computacionais, é necessário executar um mesmo conjunto de instruções diversas vezes. Para evitar a repetição manual de código e tornar o algoritmo mais eficiente e organizado, utilizamos as chamadas **estruturas de repetição** ou **laços de repetição**. Essas estruturas permitem que um bloco de comandos seja executado repetidamente, até que uma condição específica seja atendida. O fluxo do algoritmo é controlado por essa condição, que pode determinar tanto o número de repetições quanto o momento exato em que o laço deve ser encerrado. Essa abordagem é essencial para situações em que é preciso, por exemplo, percorrer todos os elementos de uma lista, realizar cálculos em série ou aguardar que determinado critério seja alcançado.

Ao utilizar estruturas de repetição, garantimos que o código seja mais conciso, legível e de fácil manutenção, evitando a necessidade de duplicar comandos para cada execução. A seguir, vamos conhecer dois tipos fundamentais de laços de repetição: o comando Para, utilizado quando sabemos antecipadamente o número de vezes que o bloco será repetido, e o comando Enquanto, indicado quando a quantidade de repetições não é conhecida.

## Estrutura do PARA

O comando $para$ é uma das formas mais comuns de implementar estruturas de repetição em algoritmos. Essa estrutura é utilizada quando o número de repetições é conhecido previamente, seja durante a elaboração do algoritmo ou fornecido como um dado de entrada durante a execução. Com o comando $para$, determinamos de forma clara quantas vezes um determinado bloco de instruções será executado, facilitando tanto a leitura quanto a mantenção do código. Essa previsibilidade torna essa estrutura ideal para situações em que o total de repetições é fixo ou pode ser calculado antes de iniciar o laço.

Um exemplo típico de uso do comando $para$ é na varredura de listas, vetores ou tabelas, onde sabemos exatamente a quantidade de elementos a ser percorrida. A seguir, vamos conhecer a sintaxe e alguns exemplos de utilização dessa estrutura.

```{code} 
para (valor inicial; < condição >; < valor do incremento >){

    bloco de comandos 

}
```

## Estrutura do Enquanto

Diferente do comando $para$, o comando $enquanto$ é recomendado para situações em que não se sabe previamente o número de repetições que devem ser executadas. Nessa estrutura, o controle do laço é feito por meio de uma condição lógica, que é testada antes de cada repetição. O bloco de comandos será executado enquanto essa condição for verdadeira; quando a condição se tornar falsa, o laço é interrompido. Esse tipo de estrutura é ideal para cenários em que a quantidade de repetições depende de algum evento ou critério externo, como a leitura de dados até o fim de um arquivo, a entrada de um valor específico pelo usuário, ou até o alcance de uma determinada meta durante o processamento.

É importante destacar que, como o teste condicional ocorre antes da execução do bloco, pode acontecer da condição ser falsa logo na primeira verificação. Nesses casos, o bloco de comandos dentro da estrutura não será executado nenhuma vez. A seguir, vamos conhecer a sintaxe e exemplos de uso do comando $enquanto$, que demonstram sua aplicação em diferentes contextos de repetição.

```{code} 
enquanto ( condição ) {

    bloco de comandos 

}
```

## Exemplos
