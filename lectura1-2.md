# Lectura: FunkSVD - Netflix Update: Try This at Home

## Resumen
La publicación trata acerca de un algoritmo recomendador basado en descomposición matricial utilizado en el concurso de Netflix. Esta descomposición consiste en dos matrices: una asociada a las películas y otra a los usuarios, cada una con 40 *features* (que se ven como filas o columnas respectivamente) que caracterizan preferencias o cualidades. Para hallar las entradas de estas matrices se utiliza el algoritmo de descenso, tal cual como en técnicas de Machine Learning. Con este método el autor y su equipo logran llegar al tercer puesto del concurso.

## Comentarios

Me parece genial que el autor haya hecho este post porque muestra que es posible resolver problemas complejos con tan sólo un computador desde la casa. Creo que la solución presentada, debido a su naturaleza intrínseca como algoritmo de aprendizaje, es altamente sofisticada matemáticamente pues está basada en tópicos de optimización convexa. Además, considero **muy** creativo el approach de encontrar factores latentes que caracterizan las preferencias, no se me habría ocurrido hacer algo así.

Un punto que podría trabajarse mejor es el *learning rate* utilizado. El autor señala que intentó distintos valores y que se quedó con el que entregaba mejores resultados simplemente. Sin embargo, hay algo que no intentó (o que quizás no menciona, no lo sabemos), y es que el *learning rate* no necesariamente tiene que ser constante. Sería interesante probar qué ocurriría con distintos tipos de valores, quizás se logre evitar el rápido overfitting que se produce con tan solo 120 iteraciones y se mejoren los resultados.

Además, con respecto a esto mismo, podría haber analizado cómo se comporta el overfitting según distintos valores de la constante de regularización K. Se menciona que existe dependencia entre el valor de K y la cantidad de factores latentes, sin embargo, no se explica más a detalle como se hace la elección. Probablemente, como típicamente ocurre, un modelo más complejo (con mayor número de factores latentes) experimente mayor overfitting, pero esto no es discutido.   
