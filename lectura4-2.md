# Lectura: Document clustering based on non-negative matrix factorization. W Xu, X Liu, Y Gong (2003).

El paper comienza describiendo un problema nuevo hasta ahora en el curso: cómo clusterizar documentos de texto. Este problema surge de la necesidad de buscar información no tan específica acerca de un evento, lo cual no es posible hacer simplemente con un *text search* ya que no se tiene claro cuales serían las palabras claves (se tiene la intención de buscar información general acerca de un tema). En este caso, lo que se busca es agrupar los documentos según los temas que trata de tal forma que la búsqueda de tal información sea más eficiente.

En la sección 2 los autores describen algunos de los métodos utilizados para llevar a cabo esta tarea, dentro de los cuales destacan la descomposición matricial SVD, que según mencionan es de las más utilizadas. En ese punto se da a conocer el problema que conlleva usar esta técnica: transformar el espacio usando SVD no deja los documentos clusterizados, si no que debe acompañarse de otro proceso de clusterización como K-Means, es decir, aún es necesario más trabajo. Este punto es importante porque justifica y motiva la creación de un nuevo modelo que logre la clusterización directamente, osea, con menos esfuerzo de cómputo.

En vista de esto, los investigadores presentan NMF, un modelo basado en optimización y factorización de la matriz de términos de los documentos a clusterizar. Se destacan dos diferencias claves en utilizar este modelo en lugar de SVD: primero, que los vectores columna de la factorización no necesariamente son ortogonales, si no que están directamente relacionados con los clusters en el sentido de que para hallar la etiqueta de un documento basta con hallar la columna con la que tenga mayor proyección; y segundo, que los documentos tienen únicamente "componentes positivas" sobre las direcciones del espacio generado por NMF. 

Cada uno de los puntos anteriores tiene ventajas sobre la factorización SVD. Con respecto al primero es que no es necesario aplicar otro método de clusterización sobre el espacio generado pues en este caso tal tarea es directa. En cuanto al segundo, es que es mucho más razonable o natural que un documento sea la suma de distintas clases en lugar de la resta de ellas (en el sentido de tener proyecciones negativas sobre algunos vectores de la factorización). Esto es fundamental porque precisamente es lo que se plantean encontrar los investigadores en el presente trabajo.

En cuanto a la derivación matemática del modelo, la única parte que me parece que debiera ser explicada mejor es por qué la matriz a factorizar (X) se debe escribir con un factor logarítmico (vea sección 3.1). Comprendo que la definición dada X queda como una matriz con entradas no nulas, sin embargo, existen muchas formas de hacer esto. Es probable que esta forma de definir la matriz de términos-documentos sea bastante estándar en la literatura, pero creo que es importante explicar por qué tiene esta forma y no otra ¿Existen otras? ¿Cómo cambian los resultados?

En cuanto a los resultados y los experimentos creo que es una muy buena práctica el trabajo de filtrado que hicieron con el dataset a trabajar. Esto es debido a que no tiene mucho sentido intentar clusterizar outliers o hacer clusters demasiado pequeños en relación a la muestra. No haber hecho esta limpieza posiblemente habría ensuciado los resultados obtenidos por los modelos.






