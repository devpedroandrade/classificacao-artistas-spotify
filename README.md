# Classificação de Identidade Sonora via Atributos Acústicos: Uma Abordagem com Machine Learning

![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)
![Scikit-Learn](https://img.shields.io/badge/Library-Scikit--Learn-orange)
![Machine Learning](https://img.shields.io/badge/AI-Supervised_Learning-success)

## Resumo do Projeto
O presente repositório contém o código-fonte, a base de dados e as análises estatísticas referentes ao projeto de classificação multiclasse de assinaturas sonoras. O objetivo central é avaliar a eficácia de algoritmos de aprendizagem supervisionada na identificação de cinco artistas musicais de géneros distintos, utilizando exclusivamente variáveis matemáticas extraídas do sinal acústico, isolando a perceção humana subjetiva.

## Contexto Académico
Este projeto foi desenvolvido como requisito de avaliação final para a disciplina MATA64 - Inteligência Artificial, do curso de Ciência da Computação da Universidade Federal da Bahia (UFBA), sob a docência da Prof.ª Dra. Tatiane Nogueira.

## Metodologia e Engenharia de Dados
A modelagem foi estruturada a partir de dados reais extraídos de plataformas de streaming, parametrizados pelas seguintes variáveis contínuas: Danceability, Energy, Acousticness e Valence.

Para mitigar o viés estatístico de classe majoritária, aplicou-se a técnica de subamostragem (Undersampling). A base de dados original foi tratada de forma a garantir uma distribuição perfeitamente simétrica, resultando num dataset final de 210 instâncias (42 faixas autênticas e independentes para cada uma das cinco classes-alvo: Björk, Gal Costa, Ivete Sangalo, Lana Del Rey e Madonna).

## Modelos de Aprendizado Supervisionado
O experimento implementa uma análise comparativa entre duas abordagens probabilísticas e estruturais distintas:

1. Gaussian Naive Bayes (Baseline Probabilístico):
   Utilizado como modelo de referência para avaliar a capacidade de classificação sob a premissa de independência condicional entre os atributos acústicos. A sua natureza gaussiana é ideal para o mapeamento de variáveis preditoras contínuas.

2. Random Forest Classifier (Abordagem Ensemble):
   Implementado como a solução avançada para superar as limitações do modelo baseline. Através da construção simultânea de múltiplos estimadores (Árvores de Decisão), o modelo é capaz de mapear a correlação não linear entre as variáveis musicais, além de fornecer a extração da relevância dos atributos (Feature Importance).

## Estrutura do Repositório
* Analise_Identidade_Sonora.ipynb: Jupyter Notebook contendo o pipeline completo de dados, treino, predição e geração das Matrizes de Confusão.
* alltracksdoubled.csv: Base de dados bruta original.
* alltracksdoubled_balanceado.csv: Base de dados tratada após aplicação do método de Undersampling.

## Reproducibilidade
Para replicar o experimento localmente ou no Google Colab:
1. Realize o clone deste repositório:
   ```bash
   git clone [https://github.com/SEU-USUARIO/NOME-DO-REPOSITORIO.git](https://github.com/SEU-USUARIO/NOME-DO-REPOSITORIO.git)
