# Monitorización de stops
## Motivación del trabajo
En la actualidad, la conducción se ha convertido en una actividad cada vez más arriesgada, especialmente durante esta temporada. Uno de los principales problemas que contribuyen a este riesgo es la falta de cumplimiento adecuado de las normas de tránsito, en particular, las infracciones relacionadas con los stops. Con el objetivo de abordar esta problemática, hemos desarrollado un proyecto centrado en la detección de stops y la posterior evaluación de su correcta ejecución.

## Objetivo de la propuesta
La finalidad de esta propuesta es utilizar videos que muestran situaciones de stops, observando detenidamente el comportamiento de los vehículos involucrados para determinar si ejecutan correctamente dichas paradas. Esta herramienta se presenta como una solución ideal para monitorizar el cumplimiento de las normas de tránsito.

## Descripción técnica del trabajo realizado
Nuestra labor se desglosa en dos tareas fundamentales. En primer lugar, implementamos un código encargado de calcular el punto medio de la línea de stop, realizando este cálculo únicamente en el primer fotograma para optimizar recursos computacionales. Para determinar la ubicación de la línea de parada, aplicamos el operador Sobel, identificando la fila con mayor cantidad de píxeles blancos como el punto de referencia para la parada. Posteriormente, nos enfocamos en analizar el movimiento del vehículo. En cada fotograma, detectamos el automóvil y almacenamos las coordenadas de la parte inferior del mismo. Si la posición del vehículo no experimenta cambios entre un fotograma y el anterior, incrementamos el contador de fotogramas detenidos. La diferencia entre un fotograma y otro puede oscilar entre 1 y 0 píxeles debido a la falta de trípode durante la grabación del video, generando cierto ruido en la imagen. Finalmente, verificamos que la coordenada del automóvil no haya cruzado la línea de stop y que haya permanecido al menos 60 fotogramas detenidos, dado que el video se reproduce a 20 fotogramas por segundo.

Adicionalmente, en cada fotograma, el recuadro que delimita al automóvil y el texto ubicado en la esquina superior izquierda indican en verde si el stop ha sido ejecutado correctamente o en rojo si no es así.

## Fuentes y tecnologías utilizadas
Hemos utilizado herramientas ya trabajadas en clase como yolo para detectar el coche, sobel para detectar la línea de stop y opencv para el análisis y modificación del video.

## Conclusiones y propuestas de ampliación
La etapa que demandó más tiempo en nuestro proyecto fue la adquisición de material de análisis apropiado para la implementación del detector de stops. Esto se debió a la necesidad de contar con una línea de stop claramente marcada, ya que de lo contrario, el operador Sobel no sería capaz de identificar correctamente el punto de parada del vehículo. Además, era crucial que en el video solo apareciera un automóvil, ya que la presencia de múltiples vehículos podría generar errores en los cálculos.

En cuanto a conclusiones, hemos logrado implementar con éxito un detector de stops basado en la detección de la línea de parada y el análisis del movimiento del vehículo. Esta herramienta se ha demostrado efectiva en situaciones controladas con una línea de stop bien definida y la presencia de un solo automóvil en el video.

Para futuras ampliaciones, proponemos explorar la posibilidad de mejorar la robustez del detector en condiciones menos ideales, como líneas de stop desgastadas o la presencia de múltiples vehículos en el video. 

## Indicación de herramientas/tecnologías con las que les hubiera gustado contar
Una mejoría considerable en el trabajo sería que los videos fueron grabados desde un trípode para que el punto de referencia de la línea de stop no se vea modificado. Además, actualmente el detector podría inducir un fallo si hubiese más de un coche en la imagen.

## Caratula
![](https://github.com/SaraSanGar/vc/blob/main/Proyecto%20final%20-%20Monitorización%20de%20stops/Caratula%20proyecto.png)
