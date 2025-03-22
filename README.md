# Predição de Gastos com Planos de Saúde

## 1. Descrição do Projeto

Este projeto tem como objetivo prever os gastos com planos de saúde com base em características demográficas e de saúde dos segurados. Utilizando a base de dados do livro Machine Learning with R de Brett Lantz, o projeto explora a relação entre variáveis como idade, índice de massa corporal (IMC), gênero, entre outras, e o custo do plano de saúde.

## 2. Objetivos

- Analisar a influência de variáveis demográficas e de saúde nos custos dos planos de saúde.

- Aplicar técnicas de Machine Learning para construir um modelo de regressão.

- Avaliar o desempenho do modelo utilizando métricas apropriadas.

## 3. Tecnologias Utilizadas

- Linguagem: Python

- Bibliotecas: Pandas, NumPy, Matplotlib, Seaborn, Scikit-Learn

## 4. Etapas do Projeto

### 4.1 - Análise Exploratória de Dados (EDA)

- Análise estatística e visualizações para entender a distribuição das variáveis.

- Verificação de outliers e dados faltantes.

### 4.2. Pré-Processamento

- Codificação de variáveis categóricas.

- Escalonamento das variáveis numéricas utilizando MinMaxScaler e StandardScaler.

### 4.3. Construção do Modelo

- Divisão do conjunto de dados em treino e teste.

- Teste de diferentes algoritmos de regressão, como Regressão Linear, Random Forest e XGBoost.

### 4.4 Avaliação do Modelo: Métricas utilizadas:

- Mean Absolute Error (MAE)

- Mean Squared Error (MSE)

- Root Mean Squared Error (RMSE)

- R² Score

## 5. Resultados

- Identificação das variáveis mais influentes no custo dos planos de saúde.

- Comparativo de desempenho entre os modelos testados.

## 6. Conclusão

O projeto demonstrou como variáveis demográficas e de saúde influenciam diretamente o custo dos planos de saúde. Os modelos desenvolvidos apresentam um bom desempenho, oferecendo insights valiosos para o setor de seguros de saúde.


## 7. Como executar o projeto

Clone o repositório:
```python
git clone https://github.com/seu-usuario/seu-repositorio.git
```
Instale as dependências:
```python
pip install -r requirements.txt
```
Execute o projeto:
```python
Projeto 2 - Regressão usando Scikit Learn.ipynb
```
