# Lectura: Performance of recommender algorithms on top-n recommendation tasks. Cremonesi, P., Koren, Y., & Turrin, R. (2010). 

## Comentario

Este paper trata principalmente acerca de la manera en que se evalúan los sistemas recomendadores. En la práctica lo que se hace es separar el conjunto de datos en un set de *training* y uno de *testing*, donde a partir de los datos del entrenamiento (y un determinado modelo o enfoque) se intentan predecir los datos del *testing set*. Luego, típicamente se evalúan los resultados obtenidos a través de alguna métrica de error promedio (RMSE o MAE). Aquí es donde ocurre un problema pues lo que es de interés es evaluar qué tan buena es la **lista** recomendada y no el error promedio de los ratings de las predicciones. El paper analiza la importancia de esta diferencia comparando distintos modelos en el estado del arte. 

Previo a realizar las comparaciones se realiza una importante apreciación acerca del proceso de evaluación: la manera en que se construye el *testing set*. Cuando se intenta testear con películas populares con rating promedio muy bueno (5), es muy probable que el valor a predecir sea también 5 pues así se minimiza el error. Sin embargo, ¿qué se gana haciendo algo así si es que **ya sabemos** que una película es muy buena? Por este motivo considero muy acertado que se haya construido un set de testeo específico a fin de evaluar la precisión de la lista Top-N recomendada.










