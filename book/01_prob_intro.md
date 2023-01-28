# 1. Introdução à probabilidade

Lidamos com incerteza o tempo todo em nossas vidas, ao escolhermos se devemos levar um guarda-chuva ao sair de casa, ao fazer escolhas financeiras ou outros assuntos em que temos informações limitadas e modelos pouco representativos da variabilidade do mundo (ou das pessoas). Ao lidar com esses problemas, muitas vezes atríbuimos probabilidades à eventos específicos. Por exemplo: qual a chance de chover? Definir probabilidade rigorosamente é bem mais difícil do que possa parecer, de fato a comunidade científica se divide em duas visões sobre o assunto:

* Abordagem frequentista (ou clássica): associada ao número de vezes que podemos repetir um experimento e obter o mesmo resultado, por exemplo ao lançar uma moeda 100 vezes e registrar o número de vezes que registramos cara virada para cima, podemos tomar o quociente entre os dois valores como a probabilidade de se obter cara.

* Abordagem Bayesiana: a descrição anterior é alvo de críticas. Por exemplo: considere uma eleição presidencial, ou a previsão do tempo para um dia específico. Nesses dois casos, os eventos não são repetidos: só há um dia 21/01/2023 ou uma eleição presidencial em 2022 (considere apenas um dos turnos). Em resumo, não são experimentos que podemos repetir e registrar os resultados para depois calcular a frequência. Mas ainda assim definimos probabilidades para eles. De fato, o que os Bayesianos argumentam é que probabilidade é uma medida da crença que temos em um evento, ou a possibilidade dele ocorrer.

Apesar das críticas e divergências das duas vertentes, os pilares que sustentam a probabilidade em ambos os campos são os mesmos. Durante esse material, será utilizada a abordagem frequentista. Um leitor atento pode ficar incomodado com a crítica anterior e a escolha desse caminho. Para esse caso, podemos assumir que apesar de alguns eventos não poderem ser repetidos, podemos ainda assim tomar essa medida para indicar se ele deve ocorrer. Conforme veremos, isso não nos imperidá de traçar resultados interessantes e entender como aplicar essa teoria em nossas tomadas de decisão e análises.

## 1.1. Definindo probabilidade

### 1.1.1 Eventos e espaço amostral

Para definir probabilidade precisamos estabelecer algumas nomenclaturas para os conceitos e grandezas que cercam nossa análise. Deonominamos **evento** o possível resultado de um experimento, por exemplo o lançamento de um dado e registro de um número (por exemplo 5) é um evento. Trata-se de uma observação nesse caso. A coleção de possíveis resultados de um experimento é denominado **espaço amostral**, usualmente ele é representado pela letra grega ômega maiúscula, $\Omega$. Vide os exemplos:

- Lançamento de um dado: $\Omega = \{1, 2, 3, 4, 5, 6\}$
- Lançamento de uma moeda: $\Omega = \{\textnormal{cara}, \textnormal{coroa}\}$, em alguns casos o lançamento de uma moeda aparece no formato $\Omega = \{\textnormal{H}, \textnormal{T}\}$ em referência às palavras em inglês heads (para cara) e tails (para coroa), isso é útil pois a inicial das palavras em português são iguais.

De forma genética podemos escrever $\Omega = \{\omega_1, \omega_2, ...\}$, em que $\omega_1, \omega_2,...$ são os possíveis resultados. 

Um espaço amostral nada mais é que um conjunto, como tal ele pode ser submetido a operações como partição, união, interesecão etc. Isso ficará mais claro a partir de um exemplo:

Considerde um dado de 6 lados. Tempos portanto o espaço amostral $\Omega = \{1, 2, 3, 4, 5, 6\}$. Podemos **particionar** esse conjunto com estratégias diferentes, por exemplo em números pares e ímpares: $P = \{2, 4, 6\}$ e $I = \{1, 3, 5\}$. Ou entre números maiores que $3$ ou não $M = \{4, 5, 6\}$ e $m = \{1, 2, 3\}$. Nesse caso usamos o critério maior que $3$ para classificar os números, como $3=3$ ele não é maior que si mesmo, e fica no segundo conjunto.

Sobre esses conjuntos veremos na próxima seção como atribuir probabilidades, mas antes vamos analisar duas operações de conjuntos:

1. **União**: chamamos de união o conjunto formado por todos os elementos de dois conjuntos, representamos a união de dois conjuntos $A$ e $B$ por $A \cup B$. Por exemplo, a união dos números pares e maiores que 3 é: $P \cup M = \{2, 4, 6\} \cup \{4, 5, 6\} = \{2, 4, 5, 6\}$.
2. **Intersecção**: chamamos de intersecção o conjunto formado pelos elementos que aparecem nos dois conjuntos, representamos a interseção de dois conjuntos $A$ e $B$ pro $A \cap B$. Por exemplo, a interseção entre os conjuntos de números ímpares e maiores que 3 é: $I \cap M = \{1, 3, 5\} \cap \{4, 5, 6\} = \{5\}$. Nesse caso temos um conjunto de apenas um elemento, pois somente ele aparece nos dois conjuntos.

Um conjunto sem nenhum elemento é chamado **conjunto vazio** e é representado por $\varnothing$. Dois conjuntos são chamados de **disjuntos** se sua interseção tem como resultado um conjunto vazio. Por exemplo, a intersecção entre os conjuntos dos números pares e ímpares: $P \cap I = \{2, 4, 6\} \cap \{1, 3, 5\} = \varnothing$, pois não há elemento em comum entre os conjuntos.