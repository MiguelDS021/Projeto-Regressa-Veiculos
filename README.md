Previsão de Preços de Carros com Regressão Linear

Projeto de ciência de dados com o objetivo de prever o preço de um carro a partir de suas características técnicas, 
usando um modelo de Regressão Linear.

📊 Sobre o dataset

Foi utilizado o Automobile Dataset, da UCI Machine Learning Repository — um conjunto de dados com 205 carros e 26 características 
(motor, dimensões, tipo de combustível, potência, consumo, entre outras).

🎯 Objetivo

Construir um modelo capaz de prever a variável price (preço do carro) com base em características técnicas do veículo, 
aplicando um fluxo completo de ciência de dados: da limpeza dos dados brutos até a avaliação do modelo treinado.

🛠️ Etapas do projeto
Importação e carregamento dos dados — leitura do CSV (sem cabeçalho), atribuição dos nomes de colunas conforme documentação da UCI, tratamento do caractere "?" como valor nulo.

Limpeza de dados
Remoção de linhas com valores nulos na variável alvo (price)
Preenchimento de nulos em colunas numéricas com a mediana
Preenchimento de nulos em coluna categórica com a moda
Verificação de duplicatas (nenhuma encontrada)
Análise de outliers — detecção via IQR (intervalo interquartil). Outliers identificados em price correspondiam a marcas de luxo 
(BMW, Jaguar, Porsche, Mercedes-Benz) e foram mantidos, por representarem dados legítimos.

Análise exploratória (EDA) — visualização de relações entre variáveis (scatter plots) e análise de correlação com a variável alvo.

Feature engineering
Seleção de features numéricas com maior correlação com price, removendo colunas redundantes por multicolinearidade
Seleção de features categóricas relevantes, evitando colunas com muitos valores únicos (risco de overfitting)
Codificação de variáveis categóricas com OneHotEncoder
Padronização de variáveis numéricas com StandardScaler

Modelagem — divisão treino/teste (80/20) e treinamento de um modelo de Regressão Linear.

Avaliação — métricas de MAE, RMSE e R², além de visualização gráfica (valores reais vs. previstos).

📈 Resultados
Métrica	Valor
MAE	≈ 1.969
RMSE	≈ 2.745
R²	≈ 0.90

O modelo explica cerca de 90% da variação dos preços dos carros. O erro tende a ser maior em veículos de luxo (faixa de preço mais alta),
por serem menos representados no dataset.

🧰 Tecnologias utilizadas

Python
Pandas
NumPy
Matplotlib
Scikit-learn

🚀 Próximos passos

Testar outros modelos (Random Forest, Ridge, Lasso) e comparar performance
Aplicar transformação logarítmica na variável alvo

Validação cruzada (cross-validation)
