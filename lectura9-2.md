# Lectura: Carousel Personalization in Music Streaming Apps with Contextual Bandits. Bendada, W., Salha, G., & Bontempelli, T. (2020)

El paper presenta el problema de la recomendación de un carrusel de items en el contexto de la música: dado con conjunto de usuarios se deben hacer recomendaciones acerca de un conjunto de playlists o álbumes. La cantidad de items que se recomiendan para cada usuario se considera constante. La propuesta de los investigadores es comparar distintos bandits donde cada brazo corresponde a una playlist, además, se presentan dos maneras de utilizar estos bandits: una completamente personalizada (a cada usuario un item) y otra semi personalizada (a cada cluster de usuarios un item).

Los clusters de usuarios son generados a partir del siguiente proceso: primero se factoriza la matriz de usuarios-items, obteniéndose vectores de representación para cada usuario. Luego, sobre ese conjunto de vectores se utiliza el algoritmo de k-Means para generar los clusters. De esta manera, usuarios que pertenecen al mismo cluster se les recomiendan los mismos items. El objetivo de esto es reducir la carga computacional de la recomendación pues podríamos agrupar 1000000 de usuarios en 100 clusters y hacer solamente 100 recomendaciones. Esto es muy importante cuando se quiere tener rapidez en una recomendación online.

Un aspecto que destaco del paper es que también toma en cuenta la manera en cómo se muestran las recomendaciones a los usuarios y en base a eso considera de una manera distinta las interacciones que tienen estos con el sistema. A partir de esas consideraciones formula una manera de hacer los updates (*Cascade update*)  en los brazos de los *bandits*. Esto es interesante pues considera el factor de la interfaz gráfica como algo que afecta el desempeño de las recomendaciones al dificultar la visualización de estas.

En la sección de resultados, me impresionó mucho que con sólo 100 clusters se podían obtener resultados del mismo orden que con métodos completamente personalizados, sin embargo, creo necesario presentar los tiempos que toma hacer las recomendaciones o iteraciones de los *badits* respectivos pues de otra manera no se visualiza la ganancia que genera la propuesta en términos de recursos computacionales. En este mismo aspecto, sería interesante discutir que tan buena es la clusterización ya que en el paper no está detallado ese proceso, y como bien sabemos, no existe una única manera de hacerlo. Esto abre la posibilidad de estudiar como afecta la representación de los usuarios en los distintos *bandits* contextuales.






