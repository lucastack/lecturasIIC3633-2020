# Lectura: Multi-armed recommender system bandit ensembles. Cañamares, R., Redondo, M., & Castells, P. (2019).

El paper comienza introduciendo una nueva manera de hacer las recomendaciones. Típicamente, dado un conjunto de datos de ratings separado en un set de entrenamiento y testeo, nos interesa encontrar el mejor modelo para llevar a cabo las recomendaciones, una vez hecho esto el problema está resuelto. El anterior enfoque es estático pues el modelo ya quedó fijado y también así las recomendaciones, y en caso de tener nuevos datos tendríamos que correr los algoritmos desde el principio. Los investigadores presentan el problema de recomendación como uno dinámico: a medida que nuevos datos llegan el sistema recomendador los incorpora y genera nuevas recomendaciones para los usuarios.    

En este contexto, los autores proponen utilizar *multi armed bandits* para resolver el problema. La idea principal es generar ensambles de modelos y que cada brazo del *bandit* corresponda a un conjunto de parámetros que determina al ensamble. Dicho de manera más práctica, esto significa que a medida que se reciben nuevos datos el bandit entrega un nuevo ensamble (o sus nuevos parámetros) para realizar nuevas recomendaciones.

Con respecto al problema de recomendación en si, me parece que es mucho más realista la versión dinámica que la estática del problema, y es que en muchos contextos de producción o de industria las recomendaciones se deben actualizar en tiempo real. En este punto es importante que los modelos propuestos sean capaces de generar nuevas recomendaciones rápidamente, y es por eso que un modelo dinámico es más apropiado dado que no necesita arrancar desde 0. Además, dado que está bien respaldada la superioridad de los ensambles por sobre los modelos individuales, es natural pensar en un modelo dinámico como aquel ensamble que modifique sus parámetros, por este motivo, creo que el mayor aporte del paper consiste en cómo incorporar *bandits* en ese esquema. En particular, ellos proponen utilizar los bandits *Thompson sampling* y *ε-greedy* para los ensambles.







