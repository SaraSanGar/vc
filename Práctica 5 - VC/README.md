<b> Práctica 5 - VC: </b>etector de matrículas

Se debe ejecutar el fichero  "VC_P5.ipynb". 

Los dos primeros bloques de códigos son los correspondientes a las importaciones y preparación previa al código.

Luego, tenemos el detector utilizando el modelo Yolo. Utilizamos la webcam para detectar las matrículas de los coches. El funcionamiento de este detector se basa en primero detectar los coches de la imagen con yolo, a continuación, calculamos la mitad inferior del coche y ese fragmento de frame es el que le pasamos al OSR, el cual nos detectará el texto. Por ultimo, normalizamos el texto utlilizando una expresión regular y mostramos por pantalla la matricula detectada.
El cuarto bloque de código corresponde con un ejemplo de como usar el OCR sobre una imagen estática.
Por ultimo,  tenemos el bloque en el que utilizamos un modelo entrenado por nosotros. 

Para la resolucion del problema de detección de matriculas hemos presentado dos aproximaciones, en la primera usamos YOLO v8 para detectar coches simplemente teniendo en cuenta la clase coche que ya posee el modelo. Una vez detectado el coche tomamos un segmento de la sección donde se dectecta el coche, en este caso, hemos decicdo tomar el tercio inferior de la imagen para usarlo como zona donde muy probablemente este la matrícula. Una vez tomada esta seccion se la pasamos al OCR de pytheseract para detectar el texto presente, usamos la opcion 6 para leer todo el texto posible debido a la alta cantidad de ruido que podemos obtener en el fragmento de imagen a procesar.

En la segund aproximacion hemos aplicado una versión de Yolo entrenada especificamente para detectar matrículs y pasarle al OCR la seccion concreta de la placa de matricula y así minimizar el ruido.

Por último hemos probado aplicando una expresión regular para limpizar posibles salidas ruidosas del OCR intentado buscar en la misma texto con formato de matrícula europea.
