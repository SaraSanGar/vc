# Práctica 6 - Detector de generos DeepFace y detector de cara MediaPipe
Se debe ejecutar el fichero  "VC_P6_deepface_kfold.ipynb". 

Este notebook tiene tres puntos importantes: el entrenamiento de la detección de generos realizado con deepface, la detección de caras con mediapipe y en tratamiento de la información.

Los primeros tres bloques son los referentes a las importaciones y las instalaciones para poder trabajar en google colab.

Luego, están los bloques referentes al entrenamiento de la detección de generos realizado con deepface, detro se realiza la definición de variables, la carga del conjunto de datos, el diseño del conjunto experimental k-fold y lanzamos el experimento. 

Una vez ejecutados estos bloques ya tendríamos el detector de generos entrenado.

A continuación, tenemos el código que hay que ejectuar para detectar caras. En este primer bloque tenemos las funciones con las que trabaja mediapipe. Aprovechamos que cada vez que detecte una cara llame al detector de generos y dependiendo de los datos resultamos tratamos la imagen de un modo o de otro. 

La imagen va a poner la imagen más rosa a mayor número de mujeres haya en la foto en comparación con los hombres, en cambio, si hay un mayor números de hombres se aumenta el color verde.

Los últimos bloques son diferentes imagenes para apreciar el cambio de comportamiento dependiendo de lo que ocurre en la imagen.
