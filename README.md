# EFuzzCND-Results

As figuras abaixo apresentam os resultados obtidos pelos dois algoritmos para os datasets MOA3, RBF e SynEDC considerando diferentes valores de latência. Os resultados apresentados pelo algoritmo EFuzzCND, são relacionados às características de agrupamento fuzzy. Os resultados apresentados pelo algoritmo ECSMiner demonstram resultados relacionados às características de agrupamento crisp. Por apresentarem estratégias semelhantes de classificação e novelty detection, a comparação entre esses dois algoritmos podem nos ajudar a entender melhor as vantagens e desvantagens na utilização de agrupamento fuzzy e agrupamento crisp na detecço de novidades em fluxo de dados.

Os gráficos apresentados nas Figuras 1 e 2 apresentam os resultados obtidos pelos algoritmos para um valor de 2000 de latência. As Figuras 1 (a) (EFuzzCND) e 2 (a) (ECSMiner) apresentam os resultados obtidos pelos algoritmos para o dataset MOA3. É possível notar que ambos os algoritmos tiveram ótimos resultados,  mantendo a acurácia em 100\% durante todos os momentos de avaliação. Analisando a medida UnkR, é possível notar que o ECSMiner classificou menos exemplos como desconhecido. Enquato o EFuzzCND se manteve em uma média de 15\% durante todo o data stream, o ECSMiner não classificou nenhum exemplo como desconhecido até o momento de avaliação 25 e a partir daí, no geral, teve uma média abaixo dos 10\%. Apesar de ter tido uma taxa de desconhecidos superior, é possível notar que quando uma nova classe surgiu (representado pela linha vertical cinza), o EFuzzCND identificou rapidamente essa novidade, no mesmo momento de avaliação em que ela surgiu, enquanto o ECSMiner levou pelo menos 3 momentos de avaliação para identificá-la.

As Figuras 1 (b) (EFuzzCND) e 2 (b) (ECSMiner) apresentam os resultados obtidos pelos algoritmos para o dataset RBF. Nese caso, os algoritmos também apresentaram excelentes resultados, mantendo a acurácia em 100\% durante toda a análise. Em relação a medida UnkR, é possível notar que o EFuzzCND teve uma quantidade muito inferior de exemplos classificados como desconhecidos. No geral, a média dos algoritmos foram muito próximas, porém, nos momentos de avaliação 8 e 42, onde teve o surgimento de novas classes, o EFuzzCND teve 15\% e 5\%, respectivamente, enquanto o ECSMiner chegou perto dos 30\% e 25\% do número total de exemplos classificados como desconhecidos, além de demorar pelo menos 2 momentos de avaliação para identificar as novidades e se estabilizar.

As Figuras 1 (c) (EFuzzCND) e 2 (c) (ECSMiner) apresentam os resultados obtidos pelos algoritmos para o dataset SynEDC, que é um dataset que possui o desaparecimento e o reaparecimento de classes. É possível notar que o EFuzzCND manteve a acurácia em 100\% durante toda a análise, enquanto o ECSMiner teve sua acurácia em 99\% a partir do momento de avaliação 8. Essa diferença também é perceptível ao analsiar a medida UnkR. O EFuzzCND teve picos crescentes de desconhecidos em todos os momentos de avaliação em que novas classes surgiram. Já o ECSMiner não conseguiu identificar todas as novas classes com êxito, ele menteve sua taxa de desconhecido em 0\% até o momento de avaliação 20, classificando erroneamente os exemplos pertencentes a nova classe que chegou no momento de avaliação 8. No restante, os algoritmos tiveram comportamentos similares.

## Latência: 2000

### EFuzzCND
MOA3             |  RBF         | SynEDC
:-------------------------:|:------------------------:|:-------------------------:
![alt text](https://github.com/andrecristiani/EFuzzCND-Results/blob/main/Graphs/moa-efuzzcnd.png?raw=true)  |  ![alt text](https://github.com/andrecristiani/EFuzzCND-Results/blob/main/Graphs/rbf-efuzzcnd.png?raw=true) | ![alt text](https://github.com/andrecristiani/EFuzzCND-Results/blob/main/Graphs/synedc-efuzzcnd.png?raw=true)
Fig 1 (a)|Fig 1 (b)|Fig 1 (c)

### ECSMiner
MOA3             |  RBF         | SynEDC
:-------------------------:|:------------------------:|:-------------------------:
![alt text](https://github.com/andrecristiani/EFuzzCND-Results/blob/main/Graphs/moa-ecsminer.png?raw=true) | ![alt text](https://github.com/andrecristiani/EFuzzCND-Results/blob/main/Graphs/rbf-ecsminer.png?raw=true) | ![alt text](https://github.com/andrecristiani/EFuzzCND-Results/blob/main/Graphs/synedc-ecsminer.png?raw=true)
Fig 2 (a)|Fig 2 (b)|Fig 2 (c)

Os gráficos apresentados nas Figuras 3 e 4 apresentam os resultados obtidos pelos algoritmos para um valor de 5000 de latência. As Figuras 3 (a) (EFuzzCND) e 4 (a) (ECSMiner) apresentam os resultados obtidos pelos algoritmos para o dataset MOA3. É possível notar que mesmo aumentando o valor da latência, ambos os algoritmos continuaram apresentando bons resultados. O EFuzzCND manteve a acurácia em 100\% durante toda a análise, enquanto o ECSMiner oscilou e chegou próximo dos 95\%. Analisando a medida UnkR, é possível notar que o EFuzzCND apresentou uma medida estável, próximo de 3\%, durante todo o fluxo e chegou a 30\% e 35\%, somente nos momentos de avaliação em que surgiram novidades. O ECSMiner no teve exemplos classificados como desconhecidos até o momento de avaliação 25, porém, após esse momento de avaliação ele teve uma crescente, atingindo 30\% e se estabilizando acima de 10\%. Assim como ocorreu com o valor 2000 de latência, o EFuzzCND também identificou a novidade no mesmo momento de avaliaço em que ela surgiu, enquanto o ECSMiner teve um aumento de tempo para identificar essa novidade, demorando cerca de 5 momentos de avaliação para começar a reduzir a taxa de desconhecidos.

As Figuras 3 (b) (EFuzzCND) e 4 (b) (ECSMiner) apresentam os resultados obtidos pelos algoritmos para o dataset RBF. É possível notar que os algoritmos mantiveram a acurácia próximo de 100\% durante toda a análise. Assim como ocorreu para o dataset MOA3, o EFuzzCND reduziu significativamente o número de desconhecidos, principalmente nos dois momentos em que uma novidade surge. Além disso, O EFuzzCND identificou a novidade no mesmo momento de avaliação em que ela surge, reduzindo gradativamente a taxa de desconhecidos ao longo do tempo, enquanto o ECSMiner manteve estável a taxa de desconhecidos durante cerca de 7 momentos de avaliação após a chegada da novidade.

As Figuras 3 (c) (EFuzzCND) e 4 (c) (ECSMiner) apresentam os resultados obtidos pelos algoritmos para o dataset SynEDC. Neste caso é perceptível a influência do valor da latência no desempenho dos algoritmos. Enquanto o EFuzzCND, assim como no cenário onde foi considerado o valor de latência 2000, manteve a acurácia em 100%, o ECSMiner, diferentemente, quando surgiu a primeira novidade, teve sua acurácia reduzida, chegando próxima de 70\% e se estabilizando entre 90\% e 93\%. Essa queda para 70\% é reflexo da primeira novidade que surgiu, não identificada pelo ECSMiner. Considerando um valor de latência maior, mais exemplos pertencentes a essa novidade foram classificados erroneamente, até o momento em que o rótulo verdadeiro chegou.

## Latência: 5000

### EFuzzCND
MOA3             |  RBF         | SynEDC
:-------------------------:|:------------------------:|:-------------------------:
![alt text](https://github.com/andrecristiani/EFuzzCND-Results/blob/main/Graphs/moaefuzzcnd-5000.png?raw=true) | ![alt text](https://github.com/andrecristiani/EFuzzCND-Results/blob/main/Graphs/rbf-efuzzcnd-5000.png?raw=true) | ![alt text](https://github.com/andrecristiani/EFuzzCND-Results/blob/main/Graphs/synedc-efuzzcnd-5000.png?raw=true)
Fig 3 (a)|Fig 3 (b)|Fig 3 (c)

### ECSMiner
MOA3             |  RBF         | SynEDC
:-------------------------:|:------------------------:|:-------------------------:
![alt text](https://github.com/andrecristiani/EFuzzCND-Results/blob/main/Graphs/moa-ecsminer-5000.png?raw=true) | ![alt text](https://github.com/andrecristiani/EFuzzCND-Results/blob/main/Graphs/rbf-ecsminer-5000.png?raw=true) | ![alt text](https://github.com/andrecristiani/EFuzzCND-Results/blob/main/Graphs/synedc-ecsminer-5000.png?raw=true)
Fig 4 (a)|Fig 4 (b)|Fig 4 (c)

Os gráficos apresentados nas Figuras 5 e 6 apresentam os resultados obtidos pelos algoritmos para um valor de 10000 de latência. As Figuras 5 (a) (EFuzzCND) e 6 (a) (ECSMiner) apresentam os resultados obtidos pelos algoritmos para o dataset MOA3. Neste caso, mesmo com o aumento no valor da latência, os algoritmos conseguiram manter bons resultados. Assim como para os outros valores de latência, para esse o EFuzzCND também manteve 100\% de acurácia durante as análises. O ECSMiner teve um pouco mais de oscilação, mas manteve a acurácia entre 96\% e 100\%. Mesmo aumentando o valor da latência, o EFuzzCND continuou precisando de apenas um momento de avaliação para identificar as novidades e começar a estabilizar a taxa de desconhecidos, enquanto o ECSMiner precisou de cerca de 10 momentos de avaliação para isso.

As Figuras 3 (b) (EFuzzCND) e 4 (b) (ECSMiner) apresentam os resultados obtidos pelos algoritmos para o dataset RBF. Neste caso, as acurácias tabém se mantiveram próximas a 100\% durante toda a análise, para ambos os algoritmos. A maior diferença pode ser encontrada ao analisar a taxa de desconhecidos entre os dois algoritmos. É possível notar, que também neste cenário, o EFuzzCND reduziu significativamente a taxa de desconhecidos, identificando as novidades nos momentos de avaliação em que elas aparecem. 

As Figuras 3 (c) (EFuzzCND) e 4 (c) (ECSMiner) apresentam os resultados obtidos pelos algoritmos para o dataset SynEDC. Neste caso, o EFuzzCND se adaptou bem às mudanças mesmo com o alto valor da latência, mantendo a acurácia em 100\% durante toda a análise. Esse foi o cenário em que o desempenho do ECSMiner teve maior queda, chegando a ficar com a acurácia em torno de 65\%. Após a queda, ele teve uma crescente a atingiu cerca de 93\% de acurácia. Analisando a taxa de desconhecidos, ambos tiveram desempenhos semelhantes, tendo uma quantidade muito próxima de exemplos classificados como desconhecidos, com exceção da primeira novidade que surgiu, que assim como nos outros valores de latência, o ECSMiner não conseguiu identificar.

## Latência: 10000

### EFuzzCND
MOA3             |  RBF         | SynEDC
:-------------------------:|:------------------------:|:-------------------------:
![alt text](https://github.com/andrecristiani/EFuzzCND-Results/blob/main/Graphs/moa-efuzzcnd-results-10000.png?raw=true) | ![alt text](https://github.com/andrecristiani/EFuzzCND-Results/blob/main/Graphs/rbf-efuzzcnd-10000.png?raw=true) | ![alt text](https://github.com/andrecristiani/EFuzzCND-Results/blob/main/Graphs/synedc-efuzzcnd-10000-png.png?raw=true)
Fig 5 (a)|Fig 5 (b)|Fig 5 (c)

### ECSMiner
MOA3             |  RBF         | SynEDC
:-------------------------:|:------------------------:|:-------------------------:
![alt text](https://github.com/andrecristiani/EFuzzCND-Results/blob/main/Graphs/moa-ECSMiner-results-10000.png?raw=true) | ![alt text](https://github.com/andrecristiani/EFuzzCND-Results/blob/main/Graphs/rbf-ecsminer-results-10000.txt.png?raw=true) | ![alt text](https://github.com/andrecristiani/EFuzzCND-Results/blob/main/Graphs/synedc-ecsminer-10000.png?raw=true)
Fig 6 (a)|Fig 6 (b)|Fig 6 (c)

Apesar de adotarem estratégias diferentes, sendo agrupamento fuzzy para o EFuzzCND, e agrupamento crisp para o ECSMiner, no geral, ambos os algoritmos apresentaram bons resultados tanto na tarefa de classificação, quanto na identificação de novas classes, quando considerado cenários com valores de latência menores. Nos experimentos realizados, foi possível notar que o valor da latência impacta diretamente no desempenho dos algoritmos. É natural que a taxa de desconhecidos aumente de acordo com o valor da latência, mas isso não deveria impactar na acurácia do algoritmo, isso foi bem representado nos experimentos feitos com o EFuzzCND. Pelo contrário, o ECSMiner teve seu desempenho muito afetado em valores de latência maiores, aumentando significativamente o número de desconhecidos, pois demorava muito mais tempo para identificar as novidades que apareciam, além de ter sua acurácia reduzida nos datasets MOA3 e SynEDC, sendo uma queda muito significativa nesse segundo. Com o desempenho do ECSMiner, foi possível notar que pequenas falhas ocorridas em baixas latências, podem tomar proporções muito maiores em altos valores de latência.

A utilização de agrupamento fuzzy demonstrou proporcionar diversos ganhos quando comparado ao agrupamento crisp, principalmente na identificação de outliers. O agrupamento fuzzy demonstrou maior rigidez na identificação de outliers, o que reflete em um aumento no número de exemplos classificados como desconhecidos. Porém, a flexibilidade dada aos micro-grupos fez com que outliers pertencentes a novas classes, recém chegadas ao classificador e com poucos micro-grupos, fossem classificadas por um micro-grupo pertencente a essa nova classe, isso explica o comportamento do EFuzzCND, de identificar os exemplos pertencentes as novidades e diminuir a taxa de desconhecidos no mesmo momento de avaliação em que elas surgem. O agrupamento crisp, adotado pelo ECSMiner, não proporcionou essa flexibilidade, neste caso, novas classes identificadas pelo algoritmo não conseguia classificar outliers pertencentes a essa nova classe, por conta disso o ECSMiner demorava vários momentos de avaliação para diminuir e estabilizar a taxa de desconhecidos.
