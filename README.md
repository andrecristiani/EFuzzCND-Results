# EFuzzCND-Results

As figuras abaixo apresentam os resultados obtidos pelos dois algoritmos para os datasets MOA3, RBF e SynEDC considerando diferentes valores de latência. Os resultados apresentados pelo algoritmo EFuzzCND, são relacionados às características de agrupamento fuzzy. Os resultados apresentados pelo algoritmo ECSMiner demonstram resultados relacionados às características de agrupamento crisp. Por apresentarem estratégias semelhantes de classificação e novelty detection, a comparação entre esses dois algoritmos podem nos ajudar a entender melhor as vantagens e desvantagens na utilização de agrupamento fuzzy e agrupamento crisp na detecço de novidades em fluxo de dados.

## Latência: 2000

### EFuzzCND
MOA3             |  RBF         | SynEDC
:-------------------------:|:------------------------:|:-------------------------:
![alt text](https://github.com/andrecristiani/EFuzzCND-Results/blob/main/Graphs/moa-efuzzcnd.png?raw=true)  |  ![alt text](https://github.com/andrecristiani/EFuzzCND-Results/blob/main/Graphs/rbf-efuzzcnd.png?raw=true) | ![alt text](https://github.com/andrecristiani/EFuzzCND-Results/blob/main/Graphs/synedc-efuzzcnd.png?raw=true)
:Fig 1 (a):|:Fig 1 (b):|:Fig 1 (c):

### ECSMiner
MOA3             |  RBF         | SynEDC
:-------------------------:|:------------------------:|:-------------------------:
![alt text](https://github.com/andrecristiani/EFuzzCND-Results/blob/main/Graphs/moa-ecsminer.png?raw=true) | ![alt text](https://github.com/andrecristiani/EFuzzCND-Results/blob/main/Graphs/rbf-ecsminer.png?raw=true) | ![alt text](https://github.com/andrecristiani/EFuzzCND-Results/blob/main/Graphs/synedc-ecsminer.png?raw=true)
:Fig 2 (a):|:Fig 2 (b):|:Fig 2 (c):

As Figuras 1 (a) (EFuzzCND) e 2 (a) (ECSMiner) apresentam os resultados obtidos pelos algoritmos para o dataset MOA3. É possível notar que ambos os algoritmos tiveram ótimos resultados,  mantendo a acurácia em 100\% durante todos os momentos de avaliação. Analisando a medida UnkR, é possível notar que o ECSMiner classificou menos exemplos como desconhecido. Enquato o EFuzzCND se manteve em uma média de 15\% durante todo o data stream, o ECSMiner não classificou nenhum exemplo como desconhecido até o momento de avaliação 25 e a partir daí, no geral, teve uma média abaixo dos 10\%. Apesar de ter tido uma taxa de desconhecidos superior, é possível notar que quando uma nova classe surgiu (representado pela linha vertical cinza), o EFuzzCND identificou rapidamente essa novidade, no mesmo momento de avaliação em que ela surgiu, enquanto o ECSMiner levou pelo menos 3 momentos de avaliação para identificá-la.

As Figuras 1 (b) (EFuzzCND) e 2 (b) (ECSMiner) apresentam os resultados obtidos pelos algoritmos para o dataset RBF. Nese caso, os algoritmos também apresentaram excelentes resultados, mantendo a acurácia em 100\% durante toda a análise. Em relação a medida UnkR, é possível notar que o EFuzzCND teve uma quantidade muito inferior de exemplos classificados como desconhecidos. No geral, a média dos algoritmos foram muito próximas, porém, nos momentos de avaliação 8 e 42, onde teve o surgimento de novas classes, o EFuzzCND teve 15\% e 5\%, respectivamente, enquanto o ECSMiner chegou perto dos 30\% e 25\% do número total de exemplos classificados como desconhecidos, além de demorar pelo menos 2 momentos de avaliação para identificar as novidades e se estabilizar.

As Figuras 1 (c) (EFuzzCND) e 2 (c) (ECSMiner) apresentam os resultados obtidos pelos algoritmos para o dataset SynEDC, que é um dataset que possui o desaparecimento e o reaparecimento de classes. É possível notar que o EFuzzCND manteve a acurácia em 100\% durante toda a análise, enquanto o ECSMiner teve sua acurácia em 99\% a partir do momento de avaliação 8. Essa diferença também é perceptível ao analsiar a medida UnkR. O EFuzzCND teve picos crescentes de desconhecidos em todos os momentos de avaliação em que novas classes surgiram. Já o ECSMiner não conseguiu identificar todas as novas classes com êxito, ele menteve sua taxa de desconhecido em 0\% até o momento de avaliação 20, classificando erroneamente os exemplos pertencentes a nova classe que chegou no momento de avaliação 8. No restante, os algoritmos tiveram comportamentos similares.


## Latência: 5000

### EFuzzCND
MOA3             |  RBF         | SynEDC
:-------------------------:|:------------------------:|:-------------------------:
![alt text](https://github.com/andrecristiani/EFuzzCND-Results/blob/main/Graphs/moaefuzzcnd-5000.png?raw=true) | ![alt text](https://github.com/andrecristiani/EFuzzCND-Results/blob/main/Graphs/rbf-efuzzcnd-5000.png?raw=true) | ![alt text](https://github.com/andrecristiani/EFuzzCND-Results/blob/main/Graphs/synedc-efuzzcnd-5000.png?raw=true)
:Fig 3 (a):|:Fig 3 (b):|:Fig 3 (c):

### ECSMiner
MOA3             |  RBF         | SynEDC
:-------------------------:|:------------------------:|:-------------------------:
![alt text](https://github.com/andrecristiani/EFuzzCND-Results/blob/main/Graphs/moa-ecsminer-5000.png?raw=true) | ![alt text](https://github.com/andrecristiani/EFuzzCND-Results/blob/main/Graphs/rbf-ecsminer-5000.png?raw=true) | ![alt text](https://github.com/andrecristiani/EFuzzCND-Results/blob/main/Graphs/synedc-ecsminer-5000.png?raw=true)
:Fig 4 (a):|:Fig 4 (b):|:Fig 4 (c):

## Latência: 10000

### EFuzzCND
MOA3             |  RBF         | SynEDC
:-------------------------:|:------------------------:|:-------------------------:
![alt text](https://github.com/andrecristiani/EFuzzCND-Results/blob/main/Graphs/moa-efuzzcnd-results-10000.png?raw=true) | ![alt text](https://github.com/andrecristiani/EFuzzCND-Results/blob/main/Graphs/rbf-efuzzcnd-10000.png?raw=true) | ![alt text](https://github.com/andrecristiani/EFuzzCND-Results/blob/main/Graphs/synedc-efuzzcnd-10000-png.png?raw=true)
:Fig 5 (a):|:Fig 5 (b):|:Fig 5 (c):

### ECSMiner
MOA3             |  RBF         | SynEDC
:-------------------------:|:------------------------:|:-------------------------:
![alt text](https://github.com/andrecristiani/EFuzzCND-Results/blob/main/Graphs/moa-ECSMiner-results-10000.png?raw=true) | ![alt text](https://github.com/andrecristiani/EFuzzCND-Results/blob/main/Graphs/rbf-ecsminer-results-10000.txt.png?raw=true) | ![alt text](https://github.com/andrecristiani/EFuzzCND-Results/blob/main/Graphs/synedc-ecsminer-10000.png?raw=true)
:Fig 6 (a):|:Fig 6 (b):|:Fig 6 (c):


