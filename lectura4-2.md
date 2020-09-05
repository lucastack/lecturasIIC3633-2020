# Lectura: Document clustering based on non-negative matrix factorization. W Xu, X Liu, Y Gong (2003).

El paper comienza describiendo un problema nuevo hasta ahora en el curso: cómo clusterizar documentos de texto. Este problema surge de la necesidad de buscar información no tan específica acerca de un evento, lo cual no es posible hacer simplemente con un *text search* ya que no se tiene claro cuales serían las palabras claves (se tiene la intención de buscar información general acerca de un tema). En este caso, lo que se busca es agrupar los documentos según los temas que trata de tal forma que la búsqueda de tal información sea más eficiente.

En la sección 2 los autores describen algunos de los métodos utilizados para llevar a cabo esta tarea, dentro de los cuales destacan la descomposición matricial SVD, que según mencionan es de las más utilizadas. En ese punto se da a conocer el problema que conlleva usar esta técnica: transformar el espacio usando SVD no deja los documentos clusterizados, si no que debe acompañarse de otro proceso de clusterización como K-Means, es decir, aún es necesario más trabajo. Este punto es importante porque justifica y motiva la creación de un nuevo modelo que logre la clusterización directamente, osea, con menos esfuerzo de cómputo.

En vista de esto, los investigadores presentan un modelo basado en optimización
