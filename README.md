**Miembros del grupo:** Sara Sánchez García y Saúl Santana Santana

Ficheros a ejecutar:
===============================

<a href="https://github.com/SaraSanGar/vc/tree/main/Práctica%201%20-%20VC"><b>[Práctica 1 - VC]:</b></a>

Ejecutar el notebook "Tarea 1 - VC.ipynb" esto mostrará los resultados del trabajo sobre la práctica 1 de la asignatura donde para comprender de forma aplicada la representación de imágenes de grises y color, su modificación, visualización y tratamiento básico. Al finalizar la práctica, debes ser capaz de crear una imagen de un determinado tamaño, acceder a los valores asociados a un determinado píxel, modificar dichos valores, dibujar primitivas gráficas básicas sobre una imagen, abrir una imagen de disco, así como acceder a los fotogramas de un vídeo o captura de cámara. Para todo ello, se completan las distintas tareas propuestas.


<a href="https://github.com/SaraSanGar/vc/tree/main/Práctica%202%20-%20VC"><b>[Práctica 2 - VC]:</b></a>

Ejecutar el notebook "Tarea_2_vc.ipynb" esto mostrará los resultados del trabajo sobre la práctica 2 de la asignatura donde se recuerda en primer término la conversión de formato del espacio de color, tanto la conversión a grises, como a otros espacios de representación, que facilitan determinadas operaciones. Tras recuperar el manejo de dichas utilidades, el cuaderno cubre un conjunto de funciones básicas de procesamiento de imágenes disponibles en OpenCV, como son las utilidades ya mencionadas de conversión de espacio de color, añadiendo las de cálculo de bordes o contornos, umbralizado, histogramas, diferencias de fotogramas o sustracción de fondo done finalmente se porpone una tarea de seguimiento de inidividuos.


<a href="https://github.com/SaraSanGar/vc/tree/main/Práctica%203%20-%20VC"><b>[Práctica 3 - VC]:</b></a>

Ejecutar el notebook "Práctica_3.ipynb" esto mostrará los resultados del trabajo sobre la práctica 3 de la asignatura donde se pretende  extraer información geométrica de los objetos presentes en una imagen. Para ello, se presentan ejemplos haciendo uso de detección de contornos y cálculo de la transformada de Hough para la detección de formas circulares.

En una primera tarea se asume que todos los objetos de interés en la imagen son circulares, en concreto monedas de la UE. Tras mostrar diversas aproximaciones para obtener sus contornos, el reto o tarea consiste en determinar la cantidad de dinero presente en la imagen.

Para la segunda tarea, se proporcionan tres subimágenes de tres clases de microplásticos recogidos en playas canarias. La tarea propuesta consiste en determinar patrones en sus características geométricas que puedan permitir su clasificación en dichas imágenes y otras. Como fuente de partida, se proporciona enlace al trabajo SMACC: A System for Microplastics Automatic Counting and Classification en el que se adoptan algunas propiedades geométricas para dicho fin.


<a href="https://github.com/SaraSanGar/vc/tree/main/Práctica%204%20-%20VC#práctica-4---filtro"><b>[Práctica 4 - VC]:</b></a> Filtro Anonymous

Se debe ejecutar el fichero  "VC_P4_DLIB.ipynb". 

La práctica consiste en un filtro para la webcam el cual te pone en la cara la máscara de anonymous.
Para poder correr el código es necesario todos los archivos existentes en esta carpeta, además, sería necesario tener los ficheros "shape_predictor_68_face_landmarks.dat" y "shape_predictor_5_face_landmarks.dat" pero ya que estos fichero son muy grandes para ser subidos a Github no se han podido añadir al repositorio.

## DEMO resultado

![](https://github.com/SaraSanGar/vc/blob/main/Práctica%204%20-%20VC/Gift%20-%20Anonymous.gif)


<a href="https://github.com/SaraSanGar/vc/tree/main/Práctica%205%20-%20VC"><b>[Práctica 5 - VC]:</b></a> Detector de matriculas

Se debe ejecutar el fichero  "VC_P5.ipynb". 

Los dos primeros bloques de códigos son los correspondientes a las importaciones y preparación previa al código.

Luego, tenemos el detector utilizando el modelo Yolo. Utilizamos la webcam para detectar las matrículas de los coches. El funcionamiento de este detector se basa en primero detectar los coches de la imagen con yolo, a continuación, calculamos la mitad inferior del coche y ese fragmento de frame es el que le pasamos al OSR, el cual nos detectará el texto. Por ultimo, normalizamos el texto utlilizando una expresión regular y mostramos por pantalla la matricula detectada.
El cuarto bloque de código corresponde con un ejemplo de como usar el OSR sobre una imagen estática.
Por ultimo,  tenemos el bloque en el que utilizamos un modelo entrenado por nosotros. 

<a href="https://github.com/SaraSanGar/vc/tree/main/Práctica%206%20-%20VC"><b>[Práctica 6 - VC]:</b></a> Filtro por generos

Se debe ejecutar el fichero  "VC_P6_deepface_kfold.ipynb". 

Este notebook tiene tres puntos importantes: el entrenamiento de la detección de generos realizado con deepface, la detección de caras con mediapipe y en tratamiento de la información.

Los primeros tres bloques son los referentes a las importaciones y las instalaciones para poder trabajar en google colab.

Luego, están los bloques referentes al entrenamiento de la detección de generos realizado con deepface, detro se realiza la definición de variables, la carga del conjunto de datos, el diseño del conjunto experimental k-fold y lanzamos el experimento. 

Una vez ejecutados estos bloques ya tendríamos el detector de generos entrenado.

A continuación, tenemos el código que hay que ejectuar para detectar caras. En este primer bloque tenemos las funciones con las que trabaja mediapipe. Aprovechamos que cada vez que detecte una cara llame al detector de generos y dependiendo de los datos resultamos tratamos la imagen de un modo o de otro. 

La imagen va a poner la imagen más rosa a mayor número de mujeres haya en la foto en comparación con los hombres, en cambio, si hay un mayor números de hombres se aumenta el color verde.

Los últimos bloques son diferentes imagenes para apreciar el cambio de comportamiento dependiendo de lo que ocurre en la imagen.

<a href="https://github.com/SaraSanGar/vc/tree/main/Proyecto%20final%20-%20Monitorización%20de%20stops"><b>[Proyecto final - VC]:</b></a> Monitorización de Stops

La finalidad de esta propuesta es utilizar videos que muestran situaciones de stops, observando detenidamente el comportamiento de los vehículos involucrados para determinar si ejecutan correctamente dichas paradas. Esta herramienta se presenta como una solución ideal para monitorizar el cumplimiento de las normas de tránsito.

![]([https://github.com/SaraSanGar/vc/blob/main/Práctica%204%20-%20VC/Gift%20-%20Anonymous.gif](https://github.com/SaraSanGar/vc/blob/main/Proyecto%20final%20-%20Monitorización%20de%20stops/Caratula%20proyecto.png)https://github.com/SaraSanGar/vc/blob/main/Proyecto%20final%20-%20Monitorización%20de%20stops/Caratula%20proyecto.png

**Bibliografía:** Guión de prácticas del profesor

