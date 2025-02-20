# Projeto de Visualização de Dados COVID-19 no Brasil

Este projeto tem o objetivo de analisar e visualizar dados relacionados à pandemia de COVID-19 no Brasil. As informações são extraídas de um arquivo CSV hospedado no GitHub.

### Bibliotecas Necessárias

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

### Carregando os Dados

Os dados são carregados a partir de um arquivo CSV hospedado no GitHub. As colunas 'ObservationDate' e 'Last Update' são interpretadas como datas durante a leitura dos dados.

```python
import pandas as pd

path = '/content/covid_19_data.csv'

df = pd.read_csv(path, parse_dates=['ObservationDate', 'Last Update'])
df
```

![image](https://github.com/user-attachments/assets/a26b9704-0e47-483c-953a-b7ef16a2e94f)


### Corrigindo as Colunas

Uma função chamada 'corrige_colunas' é definida para remover espaços e barras das colunas e convertê-las para letras minúsculas. Isso torna as colunas mais fáceis de usar e manipular.

```python
def corrige_colunas(col_name):
    return re.sub(r"[/| ]", "", col_name).lower()
```

### Plotando Casos Confirmados ao Longo do Tempo no Brasil

Os dados são filtrados para o Brasil e casos confirmados maiores que zero. Um gráfico de linha é criado usando Plotly Express para exibir o número de casos confirmados ao longo do tempo no Brasil.

### Plotando Novos Casos Diários ao Longo do Tempo no Brasil

O programa calcula o número de novos casos por dia e cria outro gráfico de linha para exibir os novos casos diários.

![image](https://github.com/user-attachments/assets/c3b93393-0695-4db1-a4b8-25cc28475989)


### Plotando Mortes ao Longo do Tempo no Brasil

Um gráfico de linha é criado para exibir o número de mortes ao longo do tempo no Brasil.

![image](https://github.com/user-attachments/assets/7ec13a30-72cd-4f1d-941c-f9cffc051dcf)


### Taxa de Crescimento

Duas funções são definidas para calcular a taxa de crescimento e a taxa de crescimento diária dos casos confirmados no Brasil. O programa então cria um gráfico de linha para exibir a taxa de crescimento ao longo do tempo.

![image](https://github.com/user-attachments/assets/d04c5fd9-bbf0-4a91-8f50-7ba8f6d7c696)

### Predição com Auto-ARIMA

O programa utiliza a função auto_arima da biblioteca pmdarima para realizar uma previsão automática das séries temporais de casos confirmados. Os valores previstos são plotados ao lado dos valores observados.

![image](https://github.com/user-attachments/assets/c06772e2-4dd0-4c47-bc4c-b37652f1f898)


### Previsão com Facebook Prophet

O programa utiliza a biblioteca Facebook Prophet para realizar previsões de casos confirmados. O conjunto de dados é dividido em conjuntos de treinamento e teste, e o modelo é treinado usando os dados de treinamento. As previsões são plotadas ao lado dos dados observados.

![image](https://github.com/user-attachments/assets/55278dda-b3c8-4761-b2fe-6f06ac42b577)

## Considerações Finais

Este é um programa em Python que utiliza técnicas de Machine Learning para visualizar e realizar previsões dos dados de COVID-19 no Brasil. Ele utiliza as bibliotecas Pandas, NumPy, Plotly, Matplotlib, Prophet e pmdarima para manipulação de dados, criação de gráficos interativos e realização de previsões.



