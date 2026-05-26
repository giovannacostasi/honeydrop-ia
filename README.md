# HoneyDrop-IA

## HoneyDrop - Inteligência Artificial

Projeto desenvolvido para a disciplina de Inteligência Artificial, com o objetivo de aplicar técnicas de Machine Learning para analisar e prever o consumo alimentar de animais em situação de rua.

## Integrantes

•⁠  ⁠Giovanna da Costa - 10418366
•⁠  ⁠Luíza Liao - 10416957
•⁠  ⁠Luiza Sayuri - 10416872

## Descrição do projeto

O HoneyDrop propõe o uso de um comedouro inteligente como apoio ao cuidado de animais em situação de rua. A ideia do projeto é utilizar dados relacionados ao consumo de ração para prever a quantidade consumida e auxiliar na tomada de decisão sobre o reabastecimento.

Nesta etapa do projeto, foi utilizado um dataset simulado, representando o funcionamento de um comedouro ao longo de 30 dias, com quatro medições diárias.

## Dataset

O dataset utilizado possui 120 registros e contém as seguintes colunas:

•⁠  ⁠⁠ data ⁠: data da medição;
•⁠  ⁠⁠ hora ⁠: horário da medição;
•⁠  ⁠⁠ temperatura_c ⁠: temperatura simulada em graus Celsius;
•⁠  ⁠⁠ dia_semana ⁠: dia da semana;
•⁠  ⁠⁠ periodo ⁠: período do dia;
•⁠  ⁠⁠ peso_inicial_g ⁠: quantidade de ração disponível antes do consumo;
•⁠  ⁠⁠ consumo_g ⁠: quantidade de ração consumida;
•⁠  ⁠⁠ peso_final_g ⁠: quantidade de ração restante após o consumo;
•⁠  ⁠⁠ reabastecimento ⁠: indicação de necessidade de reabastecimento.

Como os dados são simulados e não possuem informações pessoais ou sensíveis, não foi necessária anonimização.

## Análise exploratória

Foi realizada uma análise exploratória dos dados utilizando Python e Pandas. Foram verificados:

•⁠  ⁠primeiras linhas do dataset;
•⁠  ⁠estrutura dos dados;
•⁠  ⁠tipos das variáveis;
•⁠  ⁠estatísticas descritivas;
•⁠  ⁠existência de valores ausentes;
•⁠  ⁠consumo médio por período do dia;
•⁠  ⁠consumo médio por horário;
•⁠  ⁠relação entre temperatura e consumo.

A análise mostrou que o dataset não possui valores nulos e permitiu observar padrões gerais de consumo de ração.

## Modelo de Machine Learning

Foi utilizado um modelo de Regressão Linear para prever a variável ⁠ consumo_g ⁠, que representa o consumo de ração em gramas.

Antes do treinamento, as variáveis categóricas foram transformadas em valores numéricos utilizando ⁠ pd.get_dummies ⁠.

Para evitar vazamento de dados, as colunas ⁠ peso_final_g ⁠ e ⁠ reabastecimento ⁠ foram removidas das variáveis de entrada, pois essas informações dependem do consumo já ocorrido.

## Resultados

O modelo apresentou os seguintes resultados:

•⁠  ⁠MAE: 12,99 g
•⁠  ⁠RMSE: 16,79 g
•⁠  ⁠R²: 0,829

Esses resultados indicam que o modelo conseguiu prever o consumo de ração com bom desempenho no dataset simulado, explicando aproximadamente 82,9% da variação dos dados.

## Tecnologias utilizadas

•⁠  ⁠Python
•⁠  ⁠Google Colab
•⁠  ⁠Pandas
•⁠  ⁠Matplotlib
•⁠  ⁠Scikit-learn

## Arquivos do repositório

•⁠  ⁠⁠ HoneyDrop-IA (1).pdf ⁠: relatório do projeto
•⁠  ⁠⁠ HoneyDropAE.ipynb ⁠: notebook com dataset, análise exploratória, modelo e resultados
•⁠  ⁠⁠ honeydrop_dataset.csv ⁠: dataset utilizado
•⁠  ⁠⁠ README.md ⁠: descrição geral do projeto

## Conclusão

O projeto demonstrou que é possível utilizar Machine Learning para prever o consumo de ração em um comedouro inteligente. Os resultados obtidos foram satisfatórios para uma primeira versão com dados simulados. Como melhoria futura, pretende-se utilizar dados reais coletados por sensores e integrar o sistema a alertas automáticos para voluntários.
