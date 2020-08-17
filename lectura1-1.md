# Lectura: Item-based collaborative filtering recommendation algorithms. Sarwar, B., Karypis, G., Konstan, J., & Riedl, J. (2001).

## Resumen del paper

El paper comienza introduciendo el tema de los sistemas recomendadores y el desafío que presentan en cuanto a escalabilidad. Luego, se explican dos enfoques distintos: algoritmos *user-based* y algoritmos *item-based* para filtrado colaborativo. La tesis a demostrar es que el enfoque basado en items resuelve el problema de la escalabilidad, es decir, que entrega buenos resultados en términos de precisión y uso de recursos para una gran cantidad de datos. Finalmente se realizan experimentos computacionales con un conjunto de datos extraido de MovieLens, con lo cual los investigadores concluyen la validación de su tesis.   

## Crítica

Cuando se introduce el problema de escalabilidad se dice que los problemas se producen cuando tenemos una gran cantidad de datos: millones de usuarios o items, sin embargo, el conjunto de datos que se trabaja no coincide con esta descripción. Me parece que es necesario escoger una base de datos más grande y comparar los dos tipos de enfoque (*item-based*  vs *user-based*), cosa que no fue lo que se hizo. Con respecto a esta comparación, a pesar de que existen citas de literatura, creo que faltó adjuntar una tabla que muestre la cantidad de recomendaciones por segundo y del tiempo total utilizado (análogo a la Fig. 8) del enfoque basado en usuario, esto con el fin de despejar cualquier duda de que efectivamente el enfoque basado en items es el que resuelve el problema de la escalabilidad. 
