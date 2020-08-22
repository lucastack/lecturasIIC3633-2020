# Lectura: BPR: Bayesian personalized ranking from implicit feedback. Rendle, S., Freudenthaler, C., Gantner, Z., & Schmidt-Thieme, L. (2009).

## Resumen
Este paper presenta un nuevo enfoque para generar modelos de sistemas recomendadores con feedback implícito. Provee de un modelo de optimización (una función a optimizar) que denominan BPR-Opt, el cual es básicamente maximizar el valor de un operador relacionado con la probabilidad a posteriori, además de un método de aprendizaje para hallar tal óptimo: LearnBPR, que consiste en usar algoritmo de gradiente estocástico con bootstraping sin reemplazo. Se utiliza este enfoque con los modelos kNN y factorización matricial y se encuentran resultados muy superiores a las estrategias de aprendizaje "tradicionales" (o no bayesianos).

## Comentario

El origen de este enfoque es considerar que lo que se busca es **ordenar** los items de acuerdo a su preferencia para un cierto usuario. Por este motivo, a diferencia de los otros modelos que hemos visto, se trabaja con pares de items $(i,j)$
