# Lectura: Collaborative filtering for implicit feedback datasets. Hu, Y., Koren, Y., & Volinsky, C. (2008).

## Resumen
El paper presenta un sistema de recomendación basado en feedback implícito. Primero comienza con presentar la problemática que motiva este método: existen situaciones en la que los usuarios no dejan explícitamente sus preferencias (como un rating de estrellas, por ejemplo) si no que los datos que se tienen corresponden a otro tipo de interacciones: búsquedas, clicks, compras, etc. Después presenta el modelo generado por los investigadores para un set de datos basado en el tiempo que los usuarios visualizan shows de televisión. La idea novedosa del modelo es introducir nuevas variables: confianza y preferencia, para cada par usuario-item. Las resultados se obtienen después al minimizar el error en las preferencias encontrando factores latentes, muy similar a la estrategia del SVD. Finalmente se compara el modelo propuesto con la recomendación *most popular* y con vecinos cercanos, obteniéndose recomendaciones mucho mejores.    

## Comentarios

En cuanto al modelo matemático propuesto, me pareció genial la idea de considerar los tiempos de visualización de un show como parámetros de preferencia y confianza, aún más, los investigadores comparan este modelamiento con no haberlos introducido, probando que su decisión es correcta. Una cosa que no se explica, y que creo que es importante, es el motivo de elección de la métrica euclidiana como término de regularización, y es que ésta no es la única forma de regularizar un problema de optimización.

Debido a que en este caso no existen los *missing values*, pues si un show no se ha visto simplemente se deja su tiempo en 0, el hecho de que la complejidad (en tiempo) del algoritmo sea lineal en la cantidad de datos es fundamental, ya que en otro caso el método no escalaría muy bien para casos con bases de datos más grandes.

Otro punto que considero destacable es que el modelo permite explicar de manera natural el motivo por el que se realizan las recomendaciones a los usuarios tal como en el recomendador item-KNN. Sin embargo, debido al álgebra empleada en este algoritmo, la similaridad entre items **no** es independiente del usuario, lo cual creo que tiene mucho sentido; es razonable que cada usuario decida que tan similares son dos items.

En la parte del experimento, con el set de test, me queda la duda de si es válido considerar que una persona que vio menos de la mitad de un show simplemente no lo vió. Pienso que existen muchos supuestos bastante razonables a lo largo del paper, sin embargo, este no es uno de ellos porque es posible que el usuario simplemente no haya podido continuar viendo el show. Además, los investigadores no agregan los resultados de sí considerar estos datos como "válidos".   

Con respecto a la cantidad de factores latentes escogidos, los investigadores declaran que en base a lo observado entre más factores el modelo predice mejor y que se debieran usar tantos como el poder computacional permita, sin embargo, no queda claro que tan "costoso" en términos de recursos es probar con 200 factores. Probablemente haya hecho falta algún gráfico acerca del tiempo necesario para hacer los cómputos, además de una descripción del equipo utilizado.  

Me parece muy bien que hayan hecho comparaciones con otros algoritmos de recomendación, de esta manera se justifica utilizar el modelo propuesto. Pero, conectándolo con el párrafo anterior, ¿qué ocurre si los otros modelos resultan ser mucho más rápidos? ¿es razonable utilizar más recursos por un poco más de rendimiento?, y si es así ¿cuanto es el *trade-off*?

Finalmente, me parece muy sensata la observación de cierre de la sección de discusión, que menciona que el objetivo último de un sistema recomendador como el propuesto debiera ser lograr que los usuarios descubran nuevos shows que les gusten, más allá de sólo recomendar shows puesto que si sabemos que a un usuario le gusta un cierto show ¿que ganamos con recomendárselo?.



