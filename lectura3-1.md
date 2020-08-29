# Lectura: Performance of recommender algorithms on top-n recommendation tasks. Cremonesi, P., Koren, Y., & Turrin, R. (2010). 

## Comentario

Este paper trata principalmente acerca de la manera en que se evalúan los sistemas recomendadores. En la práctica lo que se hace es separar el conjunto de datos en un set de *training* y uno de *testing*, donde a partir de los datos del entrenamiento (y un determinado modelo o enfoque) se intentan predecir los datos del *testing set*. Luego, típicamente se evalúan los resultados obtenidos a través de alguna métrica de error promedio (RMSE o MAE). Aquí es donde ocurre un problema pues lo que es de interés es evaluar qué tan buena es la **lista** recomendada y no el error promedio de los ratings de las predicciones.







