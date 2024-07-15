# Previsão de Churn com Redes Neurais Artificiais

## Visão Geral

Este projeto é um estudo sobre redes neurais artificiais (RNA) utilizando Keras para prever o churn de clientes. O objetivo é analisar e prever a perda de clientes, ajudando a entender e prever o número de clientes que deixam de utilizar os serviços ou produtos da empresa ao longo do tempo.

## Introdução

A análise de churn de clientes acompanha e analisa a taxa de perda de clientes ao longo do tempo. O objetivo principal deste projeto é prever o churn de clientes utilizando uma rede neural artificial construída com Keras.

## Conjunto de Dados

O conjunto de dados utilizado neste projeto contém informações sobre clientes, incluindo dados demográficos, de conta e de transações. A variável alvo é `Exited`, indicando se um cliente deixou de utilizar o serviço.

## Pré-processamento

1. **StandardScaler:** Utilizado para transformar os dados de modo que a distribuição tenha média zero e variância unitária. Isso ajuda os algoritmos de aprendizado de máquina a trabalharem melhor com dados que podem ter diferentes escalas e distribuições.

2. **Label Encoding:** Utilizado para transformar variáveis categóricas em números inteiros. Isso é útil porque muitos algoritmos de aprendizado de máquina funcionam melhor com dados numéricos.

## Construção do Modelo

A construção do modelo foi realizada utilizando o Keras. O modelo é uma rede neural sequencial com várias camadas densas e camadas de dropout para evitar overfitting. A camada de entrada tem o mesmo número de neurônios dos atributos do conjunto de dados.

## Treinamento

O modelo foi compilado com o otimizador Adam e a função de perda `binary_crossentropy`. O treinamento foi realizado com um número especificado de épocas e tamanho de lote.

## Avaliação

As previsões foram feitas no conjunto de teste e diversas métricas foram calculadas para avaliar o desempenho do modelo, incluindo acurácia, F1 Score, recall, precisão e matriz de confusão.

## Conclusão

Os resultados mostraram que o modelo alcança uma boa acurácia, mas há espaço para melhorias no recall e F1 Score. Ajustes adicionais no modelo podem melhorar a detecção de churn.

* A acurácia de 86% indica que o modelo está performando bem na classificação geral, mas é importante observar que o recall e o F1 Score estão relativamente mais baixos. Isso sugere que o modelo pode estar perdendo alguns casos de churn (baixo recall) enquanto mantém uma boa precisão geral (71%).
* Para melhorar o desempenho, seria interessante explorar ajustes adicionais no modelo, como otimização de hiperparâmetros, seleção de características mais relevantes ou até mesmo considerar o uso de outras técnicas como balanceamento de classes para melhorar a detecção de churn (aumentando o recall).

