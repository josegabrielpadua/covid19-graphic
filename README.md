# Projeto de Visualização de Dados COVID-19 no Brasil

Este projeto tem o objetivo de analisar e visualizar dados relacionados à pandemia de COVID-19 no Brasil. As informações são extraídas de um arquivo CSV hospedado no GitHub.

#### Bibliotecas Necessárias

- pandas: Biblioteca para manipulação e análise de dados em Python.
- numpy: Biblioteca para suporte a operações matemáticas em arrays multidimensionais.
- datetime: Biblioteca para manipulação de datas e horas.
- plotly.express: Biblioteca para criação de gráficos interativos e visuais.
- plotly.graph_objects: Biblioteca para criação de gráficos personalizados.
- re: Módulo para manipulação de expressões regulares em Python.
- pmdarima.arima: Biblioteca para análise e previsão de séries temporais usando modelos ARIMA.
- statsmodels.tsa.seasonal: Módulo para decomposição de séries temporais em componentes sazonais.
- matplotlib.pyplot: Biblioteca para criação de gráficos estáticos.
- prophet: Biblioteca para previsões de séries temporais desenvolvida pelo Facebook.
- plotly.io: Módulo para interação com o Plotly e exportação de gráficos.

#### Carregando os Dados

Os dados são carregados a partir de um arquivo CSV hospedado no GitHub. As colunas 'ObservationDate' e 'Last Update' são interpretadas como datas durante a leitura dos dados.

#### Corrigindo as Colunas

Uma função chamada 'corrige_colunas' é definida para remover espaços e barras das colunas e convertê-las para letras minúsculas. Isso torna as colunas mais fáceis de usar e manipular.

#### Plotando Casos Confirmados ao Longo do Tempo no Brasil

Os dados são filtrados para o Brasil e casos confirmados maiores que zero. Um gráfico de linha é criado usando Plotly Express para exibir o número de casos confirmados ao longo do tempo no Brasil.

#### Plotando Novos Casos Diários ao Longo do Tempo no Brasil

O programa calcula o número de novos casos por dia e cria outro gráfico de linha para exibir os novos casos diários.

#### Plotando Mortes ao Longo do Tempo no Brasil

Um gráfico de linha é criado para exibir o número de mortes ao longo do tempo no Brasil.

#### Taxa de Crescimento

Duas funções são definidas para calcular a taxa de crescimento e a taxa de crescimento diária dos casos confirmados no Brasil. O programa então cria um gráfico de linha para exibir a taxa de crescimento ao longo do tempo.

#### Predição com Auto-ARIMA

O programa utiliza a função auto_arima da biblioteca pmdarima para realizar uma previsão automática das séries temporais de casos confirmados. Os valores previstos são plotados ao lado dos valores observados.

#### Previsão com Facebook Prophet

O programa utiliza a biblioteca Facebook Prophet para realizar previsões de casos confirmados. O conjunto de dados é dividido em conjuntos de treinamento e teste, e o modelo é treinado usando os dados de treinamento. As previsões são plotadas ao lado dos dados observados.


#### Como Utilizar o Programa

1. Certifique-se de ter todas as bibliotecas instaladas em seu ambiente Python.
2. Execute o programa e aguarde o carregamento e processamento dos dados.
3. Os gráficos interativos serão exibidos automaticamente. Você pode explorar os dados interativamente usando as ferramentas de zoom e pan.
4. As previsões também serão exibidas junto com os dados observados.


## Considerações Finais

Este é um programa em Python que utiliza técnicas de Machine Learning para visualizar e realizar previsões dos dados de COVID-19 no Brasil. Ele utiliza as bibliotecas Pandas, NumPy, Plotly, Matplotlib, Prophet e pmdarima para manipulação de dados, criação de gráficos interativos e realização de previsões.



