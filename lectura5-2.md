# Lectura: Combining predictions for accurate recommender systems. Jahrer, M., Töscher, A. and Legenstein, R. (2010).

Este paper trata acerca de cómo se pueden combinar los distintos modelos *state-of-the-art* (para la época) para hacer mejores recomendaciones que utilizándolos de manera individual. La idea principal es entrenar varios de estos modelos pequeños para posteriormente ensamblarlos, lo que se hace mediante una combinación lineal de los output de cada uno de ellos. Se observa, con el dataset de Netflix Prize, que con este esquema se obtienenen mejores recomendaciones que con los modelos individuales según el RMSE. 

Una de los puntos más importantes a mi parecer, es que como el tamaño del probe set de entrenamiento es muy grande, es demasiado costoso realizar el entrenamiento de algunos modelos sobre todo el conjunto, por lo que se hace necesario entrenar sobre fracciones de este. Esto permite que cada modelo vaya observando muestras distintas del conjunto de entrenamiento, adaptándose a ellas, lo cual es consistente con el enfoque que se quiere dar: obtener distintos modelos y combinarlos. Esto da mayor variabilidad a los modelos (a pesar de que se ocupen dos iguales, se entrenan sobre conjuntos distintos), lo que posiblemente hace que se reduzca el overfitting del ensamble final y mejore los resultados.  

Me sorprendió que a pesar de utilizar muestras relativamente pequeñas con respecto al total de datos, las redes neuronales tomaran tanto tiempo en entrenar considerando que su tamaño (cantidad de neuronas y capas) no es tan grande. Sin embargo, sus tamaños reducidos prueban su poder al ser capaces de hacer millones de recomendaciones en muy poco tiempo. Algo que podría agregarse es una tabla comparando los distintos RMSE de estas redes cambiando los parámetros pues se menciona que los valores presentados funcionan mejor, pero no hay una tabla comparativa que lo muestre.

En la sección de resultados, se muestra que hacer un ensamble de muchos KNN prácticamente mejora muy poco con respecto a utilizar uno sólo. Esto es importante pues muestra que el éxito de un ensamble es dependiente de la clase de los modelos pequeños. En este caso, a pesar de que los investigadores proponen una idea de por qué ocurre esto, creo que otro motivo puede ser que la variabilidad de los KNN no es muy alta a pesar de ser entrenados en muestras aleatorias distintas. Esto podría verificarse analizando que tan distintas son las recomendaciones que hace cada uno de los modelos, lo cual no se discute, y esto aplica para todos los ensambles que se generaron.




