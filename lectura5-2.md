# Lectura: Combining predictions for accurate recommender systems. Jahrer, M., Töscher, A. and Legenstein, R. (2010).

Este paper trata acerca de cómo se pueden combinar los distintos modelos *state-of-the-art* (para la época) para hacer mejores recomendaciones que utilizándolos de manera individual. La idea principal es entrenar varios de estos modelos pequeños para posteriormente ensamblarlos, lo que se hace mediante una combinación lineal de los output de cada uno de ellos. Se observa, con el dataset de Netflix Prize, que con este esquema se obtienenen mejores recomendaciones que con los modelos individuales según el RMSE. 

Una de los puntos más importantes a mi parecer, es que como el tamaño del probe set de entrenamiento es muy grande, es demasiado costoso realizar el entrenamiento de algunos modelos sobre todo el conjunto, por lo que se hace necesario entrenar sobre fracciones de este. Esto permite que cada modelo vaya observando muestras distintas del conjunto de entrenamiento, adaptándose a ellas, lo cual es consistente con el enfoque que se quiere dar: obtener distintos modelos y ponderarlos. Esto da mayor variabilidad a los modelos (a pesar de que se ocupen dos iguales, se entrenan sobre conjuntos distintos), lo que posiblemente hace que se reduzca el overfitting del ensamble final.  


