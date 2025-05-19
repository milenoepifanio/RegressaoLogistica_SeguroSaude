# Predição de Gastos com Planos de Saúde

## 1. Descrição do Projeto
Este projeto tem como objetivo prever os gastos com planos de saúde com base em características demográficas e de saúde dos segurados. O foco é entender como variáveis como idade, IMC, número de filhos, hábito de fumar, sexo e região influenciam o custo do seguro.

## 2. Problema que Queremos Solucionar
O problema que queremos solucionar é prever os gastos com planos de saúde de acordo com as características do segurado. 

Essa previsão pode ser útil:
- Para **segurados**, que desejam entender quais fatores tornam seus planos mais caros ou mais baratos.
- Para **seguradoras**, que precisam manter o equilíbrio financeiro e definir preços de forma mais justa e estratégica com base no perfil de risco de cada pessoa.


## 3. Objetivos
- Analisar a influência de variáveis demográficas e de saúde nos custos dos planos.
- Construir modelos de regressão com diferentes algoritmos.
- Avaliar o desempenho preditivo utilizando métricas apropriadas.

## 4. Tecnologias Utilizadas
- Linguagem: Python
- Bibliotecas: Pandas, NumPy, Matplotlib, Seaborn, Scikit-Learn, Statsmodels

## 5. Etapas do Projeto

### 5.1 Análise Exploratória de Dados (EDA)
- Visualização das distribuições das variáveis numéricas.
- Análise de correlações e pairplots.
- Detecção de outliers e compreensão dos dados.

### 5.2 Pré-Processamento
- Codificação binária (sexo, fumante).
- One-hot encoding para a variável de região.
- Normalização das variáveis com MinMaxScaler.

### 5.3 Construção dos Modelos
- Separação em dados de treino e teste.
- Modelos aplicados:
  - Regressão Linear
  - Árvore de Decisão
- Validação cruzada (10 folds) com avaliação via RMSE.

### 5.4 Avaliação dos Modelos
- Métricas utilizadas:
  - Root Mean Squared Error (RMSE)
  - R² Score
- Comparativo de desempenho entre os modelos via boxplot.
- Análise dos coeficientes e p-valores com `statsmodels`.

## 6. Resultados

- A regressão linear apresentou melhor desempenho em comparação à árvore de decisão, com menor RMSE médio e maior estabilidade entre os folds da validação cruzada. Isso indica que a relação entre as variáveis e o custo do seguro é majoritariamente linear.
- A árvore de decisão demonstrou maior variabilidade e propensão ao overfitting.
- O valor de R² obtido com os dados de teste foi **0.78**, o que indica que aproximadamente 78% da variação nos custos dos planos pode ser explicada pelas variáveis utilizadas.

### Validação com Novos Dados (Inputs Reais)

- Para testar a capacidade de generalização, o modelo foi avaliado com **novos dados fornecidos manualmente pelo usuário via `input()`**, sem reutilizar a base de teste. Isso garante que o modelo **não tinha conhecimento prévio desses dados**.

- Os valores inseridos foram:

```python
idade = input()                     # '27'
indice_massa_corporal = input()    # '43'
criancas = input()                 # '0'
fumante = input("1 para fumante, 0 para não fumante: ")  # '0'
sexo = input("1 para mulher, 0 para homem: ")            # '0'
```
Após normalização com o MinMaxScaler, os valores utilizados no modelo foram:
```
array([[0.19565217, 0.72746839, 0., 0., 0.]])
```

A predição gerada pelo modelo foi:
```
array([[8903.40]])
```

Esse experimento confirma que o modelo consegue prever com boa precisão o custo de um plano de saúde baseado em características reais de entrada.

## 7. Como executar o projeto

Clone o repositório:
```python
git clone https://github.com/milenoepifanio/RegressaoLogistica_SeguroSaude.git
```
Instale as dependências:
```python
pip install -r requirements.txt
```
Execute o projeto:
```python
Projeto 2 - Regressão usando Scikit Learn.ipynb
```