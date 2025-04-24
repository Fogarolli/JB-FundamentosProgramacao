# Introdução a Programação

<div class="box-content">
  <strong>
    “Todos deveriam aprender a programar um computador, porque isso ensina a pensar.” — <a href=https://www.youtube.com/watch?v=vD3vCmRbclI> Steve Jobs
    </a> 
  </strong>
</div>

Vivemos em uma era digital, na qual dispositivos eletrônicos, como computadores, *smartphones* e até mesmo roupas inteligentes, estão presentes em praticamente todos os momentos do nosso dia. Esses dispositivos funcionam processando **dados** sob o controle de conjuntos de instruções chamados **programas de computador**. Esses programas orientam o funcionamento das máquinas, seguindo sequências ordenadas de ações criadas por pessoas chamadas **programadores**.

## O que é programação?

A programação, também conhecida como codificação, é o processo de criação de instruções que computadores e outros dispositivos eletrônicos podem executar. Essas instruções são escritas em diferentes **linguagens de programação**  que os computadores conseguem interpretar. Programar é, essencialmente, “conversar” com o computador, dizendo-lhe exatamente o que fazer.

Além de permitir o controle e a automação de dispositivos, aprender a programar desenvolve uma habilidade essencial: a **resolução de problemas**. Programar exige formular problemas, pensar criativamente sobre soluções e expressar essas soluções de maneira clara e precisa. Assim, o processo de aprendizado da programação se torna uma excelente oportunidade para desenvolver o raciocínio lógico e a capacidade de resolver desafios de forma estruturada.

## O que é um programa de computador?

Um **programa** (ou ***software***) é um conjunto de **instruções** que um computador segue para concluir uma tarefa, como realizar um cálculo. A computação pode ser matemática, como resolver um sistema de equações ou encontrar as raízes de um polinômio, mas também pode ser simbólica, como pesquisar e substituir texto em um documento ou compilar um programa.

Podemos comparar um programa a uma receita: assim como uma receita informa as etapas para preparar um prato, um programa informa ao computador quais passos tomar para executar uma tarefa. Ao usar um navegador da web, um processador de texto ou um videogame, você está utilizando um programa.

Os programas são escritos em diferentes linguagens de programação, como **Python**, JavaScript, R ou C++. Cada linguagem tem suas próprias regras (sintaxe) e é usada para diferentes tipos de tarefas. Por exemplo, o JavaScript é comum no desenvolvimento web, enquanto o Python é popular para análise e ciência de dados.

Para escrever um programa, você precisa aprender uma linguagem de programação e saber resolver problemas de maneira lógica. É como aprender um novo idioma, mas, em vez de se comunicar com pessoas, você se comunica com computadores.


## Aplicações

Com o avanço da tecnologia, a programação se tornou essencial em nosso dia a dia. Ela está presente em diversas situações cotidianas: quando nos comunicamos com outras pessoas, realizamos pagamentos, postamos fotos em redes sociais ou jogamos videogames. A programação é fundamental para a revolução tecnológica, conectando dispositivos como celulares, carros inteligentes, computadores, eletrodomésticos e até roupas inteligentes.

Independentemente da área de atuação, o conhecimento em programação é uma ferramenta valiosa. Ele não apenas se tornou uma habilidade importante no mercado de trabalho, mas também promove a resolução de problemas complexos, além de estimular o pensamento crítico e a criatividade.

A programação está presente em praticamente todas as áreas do conhecimento. Aqui estão algumas aplicações comuns:

- **Automação de tarefas**: Redução do trabalho manual em processos repetitivos.
- **Ciência de Dados e Inteligência Artificial**: Análise e interpretação de grandes volumes de dados para tomada de decisões.
- **Engenharia de Produção**: Modelagem, simulação e otimização de processos industriais.
- **Desenvolvimento de Software e Web**: Criação de aplicativos, sites e sistemas.
- **Jogos Digitais**: Desenvolvimento de jogos e ambientes interativos.

## Por que aprender a programar?

Saber programar é uma habilidade essencial no mundo moderno, que vai além da criação de *softwares* e resolução de problemas computacionais. Aprender a programar promove o desenvolvimento do pensamento lógico e analítico, proporcionando inúmeros benefícios, como:


1. **Pensamento lógico e estruturado**: Ensina a decompor problemas complexos em partes menores e a encontrar soluções eficientes.
2. **Automação e eficiência**: Permite automatizar tarefas repetitivas, economizando tempo e esforço.
3. **Alta demanda no mercado de trabalho**: Empresas de diversos setores buscam profissionais com habilidades em programação.
4. **Capacidade de inovação**: Facilita a criação de novas ferramentas, produtos e serviços.
5. **Tomada de decisão baseada em dados**: Auxilia na interpretação e análise de informações de forma mais eficaz.

<!--
## (⚠️ Em construção) História da Programação
-->

## Linguagem de Programação

Os programadores escrevem instruções usando diversas linguagens de programação. Enquanto algumas são diretamente compreendidas pelos computadores, outras precisam ser traduzidas antes da execução. As linguagens de programação funcionam como uma ponte entre humanos e máquinas, facilitando a comunicação além dos códigos binários (0s e 1s), que são a única forma de linguagem que os dispositivos compreendem diretamente.


### Tipos de Linguagem de Programação

As linguagens de programação são classificadas em três grandes grupos:

- **Linguagens de Máquina**:Códigos binários que o *hardware* interpreta diretamente.
- **Linguagens Assembly**: Próximas da linguagem de máquina, mas com comandos mais compreensíveis para humanos.
- **Linguagens de Alto Nível**: Mais próximas da linguagem humana, com sintaxe intuitiva. Exemplos incluem Python, Java, C++ e JavaScript.

Linguagens de alto nível tornam a programação mais acessível. O código escrito nelas é convertido em linguagem de máquina através de tradutores, como **compiladores** ou **interpretadores**.


### Comparação entre Linguagens

Abaixo, comparamos um mesmo algoritmo — a geração da sequência de Fibonacci — escrito em Python e em Assembly:


```{admonition} Python (Linguagem de Alto Nível)
:class: examples codes
```python
number = 10
n1, n2 = 0, 1

for i in range(1, number + 1):
  print(n1)
  next_term = n1 + n2
  n1, n2 = n2, next_term
```

Neste exemplo, o código é direto e legível, usando estruturas como variáveis e loops.

```{admonition} Assembly (Linguagem de Baixo Nível)
:class: examples codes
```asm
AREA ascen, CODE, READONLY
  ENTRY
  CODE32
  ADR r0, thumb
  BX r0
  CODE16
thumb
  MOV r0, #00
  SUB r0, r0, #01
  MOV r1, #01
  MOV r4, #10
  LDR r2, 0x40000000
back
  ADD r0, r1
  STR r0, [r2]
  ADD r2, #04
  MOV r3, r0
  MOV r0, r1
  MOV r1, r3
  SUB r4, #01
  CMP r4, #00
  BNE back
  END
```


Aqui, vemos um código mais extenso e técnico, exigindo maior conhecimento da arquitetura do processador.

Ambos os exemplos geram a mesma sequência de Fibonacci, mas a legibilidade do código em Python destaca o valor das linguagens de alto nível, especialmente para iniciantes. No entanto, linguagens de baixo nível, como Assembly, são essenciais para entender e otimizar o funcionamento do hardware.
