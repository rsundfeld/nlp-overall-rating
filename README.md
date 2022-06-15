**Abordagem**: modelagem de classificação multiclasse utilizando variáveis dummies criadas a partir do texto original, seguindo as seguintes etapas:
- verificação de nulos
- tratamento de acentuação, pontuação e stopwords
- aplicação do método TF-IDF

**Otimização do algoritmo**: Os algoritmos testados foram Naive Bayes (NB, usual em problemas de textos) e Random Forest (RF, ajuste paralelizável e mais rápido). Há três versões de modelos ao final (uma primeira usando apenas o texto, a segunda acrescentando algumas variáveis do reviewer e a terceira após balanceamento de classes). Todas seguem as etapas:
- separação entre treino e teste
- manipulações na base de treino (fit transform) e apenas aplicação na base de teste (transform)
- otimização de hiperparâmetros da RF utilizando grid search com validação cruzada apenas na base de treino
- ajuste final da RF e do NB na base de treino
- cálculo da acurácia global e visualização da matriz de confusão 5x5 para ambos os algoritmos
