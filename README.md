
# Aprendizado Supervisionado - Classificação

Este projeto explora técnicas de **aprendizado supervisionado** voltadas para **classificação** de dados, utilizando algoritmos de Machine Learning e estratégias de otimização de desempenho.

## Objetivos e Dados utilizados

O dataset é composto por informações extraídas de imagens digitalizadas de exames  de massas mamárias. Para cada amostra (ou seja, cada massa mamária), foram calculadas diversas características dos núcleos celulares presentes na imagem. O objetivo deste projeto é utilizar os dados para que modelos de machine learning de Classificação sejam treinados para prever se um tumor é maligno ou benigno com base nessas características.


## Conteúdo do Projeto

- **Introdução ao Aprendizado Supervisionado**
  - Diferenças entre **Regressão** e **Classificação**.
- **Modelos de Classificação Utilizados**
  - K-Nearest Neighbors (KNN)
  - Random Forest
  - Regressão Logística
- **Técnicas de Redução de Dimensionalidade**
  - Extração de características com **PCA** (Principal Component Analysis)
  - Seleção de características (Feature Selection)
- **Otimização de Modelos**
  - Ajuste de hiperparâmetros utilizando **GridSearchCV**.
- **Avaliação de Modelos**
  - Relatórios de Classificação (Classification Report)
  - Matrizes de Confusão (Confusion Matrix)

## Tecnologias Utilizadas

- Python
- Bibliotecas:
  - `scikit-learn`
  - `numpy`
  - `pandas`
  - `matplotlib`
  - `scipy`
    


## Resultados

O projeto demonstra:
- Como diferentes classificadores se comportam em bases de dados reduzidas ou selecionadas.
- A importância da escolha dos parâmetros corretos para melhorar a acurácia.
- A visualização de métricas e gráficos de avaliação de desempenho.

## Conclusão

Com base nos resultados obtidos para os modelos e cenários testados:

- **KNN**:
  - Sem redução de dimensionalidade: Acurácia **0.96** com Dados de Teste. Cross-validation score **0.965** com dados de treino.
  - Com PCA (7 componentes): Acurácia **0.95** com Dados de Teste. Cross-validation score **0.969** com dados de treino.

- **Random Forest**:
  - Sem redução de dimensionalidade: Acurácia **0.97** com Dados de Teste. Cross-validation score **0.962** com dados de treino.
  - Com PCA: Acurácia **0.96** com Dados de Teste. Cross-validation score **0.950** com dados de treino.
  - Com Select From Model: Acurácia **0.96** com Dados de Teste. Cross-validation score **0.965** com dados de treino.

- **Regressão Logística**:
  - Sem redução de dimensionalidade: Acurácia **0.98** com Dados de Teste. Cross-validation score **0.980** com dados de treino.
  - Com PCA: Acurácia **0.98** com Dados de Teste. Cross-validation score **0.967** com dados de treino.
  - Com Select From Model: Acurácia **0.96** com Dados de Teste. Cross-validation score **0.980** com dados de treino.

### Melhor Modelo

A melhor escolha foi a **Regressão Logística sem Redução de Dimensionalidade**, pois:
- Obteve um **alto valor de acurácia (0.98)** com os dados de teste.
- Apresentou **excelentes valores de precisão, recall e f1-score**.
- Mostrou um desempenho consistente nos dados de treino e teste, com score médio elevado utilizando 3 folds na validação cruzada dos dados de treino.
