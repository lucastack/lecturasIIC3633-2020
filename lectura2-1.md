# Lectura: Collaborative filtering for implicit feedback datasets. Hu, Y., Koren, Y., & Volinsky, C. (2008).

## Resumen
El paper presenta un sistema de recomendación basado en feedback implícito. Primero comienza con presentar la problemática que motiva este método: existen situaciones en la que los usuarios no dejan explícitamente sus preferencias (como un rating de estrellas, por ejemplo) si no que los datos que se tienen corresponden a otro tipo de interacciones: búsquedas, clicks, compras, etc. Después presenta el modelo generado por los investigadores para un set de datos basado en el tiempo que los usuarios visualizan shows de televisión. La idea novedosa del modelo es introducir nuevas variables: confianza y preferencia, para cada par usuario-item. Las resultados se obtienen después al minimizar el error en las preferencias encontrando factores latentes, muy similar a la estrategia del SVD. Finalmente se compara el modelo propuesto con la recomendación *most popular* y con vecinos cercanos, obteniéndose recomendaciones mucho mejores.    

## Comentarios
