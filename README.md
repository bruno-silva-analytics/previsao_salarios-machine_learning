# 📊 Previsão de Salários com Machine Learning

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-11557c?style=for-the-badge&logo=python&logoColor=white)
![Seaborn](https://img.shields.io/badge/Seaborn-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)
![Google Colab](https://img.shields.io/badge/Google%20Colab-F9AB00?style=for-the-badge&logo=googlecolab&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=for-the-badge&logo=jupyter&logoColor=white)


Projeto de **Ciência de Dados** voltado à análise exploratória e predição salarial a partir dos anos de experiência profissional utilizando **Regressão Linear Simples** (`scikit-learn`).

## 🎯 Objetivo do Projeto

Investigar como a experiência profissional impacta a remuneração e construir um modelo preditivo capaz de estimar salários para diferentes faixas de experiência, avaliando sua precisão estatística e generalização em cenários projetados.

## 📁 Fonte dos Dados

Os dados utilizados neste projeto foram obtidos no Kaggle:
- **Dataset:** [Salary Dataset - Simple Linear Regression](https://www.kaggle.com/datasets/abhishek14398/salary-dataset-simple-linear-regression)
- **Arquivo:** `Salary_dataset.csv` (30 registros após limpeza e padronização de colunas: `ano_experiencia` e `salario`).

## 🔍 Etapas Realizadas

1. **Importação e Configuração:** carregamento das bibliotecas (`pandas`, `numpy`, `matplotlib`, `seaborn`, `scikit-learn`) e formatação numérica para visualização.
2. **Qualidade e Limpeza dos Dados:** verificação de dimensões, tipos de dados, valores duplicados (`0`) e valores ausentes (`0`), além da remoção de coluna de índice redundante e renomeação das variáveis para o português (`ano_experiencia` e `salario`).
3. **Análise Exploratória de Dados (EDA):**
   - Estatísticas descritivas (média de ~5,41 anos de experiência; salário mínimo de `37.732,00` e máximo de `122.392,00`).
   - Matriz de correlação e gráfico de dispersão evidenciando forte correlação linear positiva (`~0,98`) entre tempo de experiência e salário.
   - Ranking dos 10 maiores salários médios por anos de experiência e *boxplots* para análise de distribuição e mediana.
   - Agrupamento salarial por faixas de 5 anos de experiência.
4. **Modelagem e Avaliação:**
   - Treinamento de um modelo de **Regressão Linear Simples** (`LinearRegression`).
   - Geração de previsões para cenários de **12 a 30 anos de experiência**.
   - Avaliação do ajuste no conjunto analisado por meio de métricas de erro e explicabilidade.

## 📈 Resultados e Métricas do Modelo

| Métrica | Valor | Interpretação |
| :--- | :--- | :--- |
| **R² (Coeficiente de Determinação)** | `0.9570` | O modelo explica **95,70%** da variância salarial a partir dos anos de experiência. |
| **MAE (Erro Absoluto Médio)** | `4.644,20` | Desvio médio absoluto entre valores reais e previstos. |
| **RMSE (Raiz do Erro Quadrático Médio)** | `5.592,04` | Penaliza com maior peso os erros de maior magnitude. |

> **Observação metodológica:** em projetos de produção ou avaliação externa, recomenda-se dividir os dados em treino e teste (`train_test_split`) e interpretar projeções muito acima do intervalo observado (`> 10,6` anos) com cautela, devido ao tamanho amostral (`n = 30`) e à ausência de outras variáveis (como cargo, setor, formação ou localização).
