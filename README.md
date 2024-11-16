# VisionArtificial_ManoArduino
Este código de Python se utiliza para detectar los dedos de una mano en tiempo real a través de una cámara weeb. Los gestos de la mano son utilizados 
para controlar como una placa Arduino. 

Para operar con él, es necesario importar las siguientes bibliotecas:
  •	cv2: Para capturar y procesar imágenes de la cámara.
  •	mediapipe: Para la detección de manos y puntos clave.
  •	numpy: Para operaciones matemáticas y de matrices.
  •	math: Para cálculos matemáticos.
  •	pyfirmata: Para interactuar con una placa Arduino.

A continuación se da una descripcion general del código: 
1.	Función palm_centroid:
  •	Calcula el centroide de la palma de la mano a partir de una lista de coordenadas.

2.	Configuración de MediaPipe y OpenCV:
  •	Inicializa los módulos de dibujo y detección de manos de MediaPipe.
  •	Configura la captura de video desde la cámara web.
  •	Conecta a una placa Arduino en el puerto COM.

3.	Puntos clave de la mano:
  •	Define los puntos clave para el pulgar, la palma y las puntas y bases de los dedos.

4.	Bucle principal:
  •	Captura fotogramas de la cámara en un bucle.
  •	Procesa cada fotograma para detectar manos y sus puntos clave.
  •	Calcula el ángulo del pulgar y determina si está extendido.
  •	Calcula las distancias entre el centroide de la palma y las puntas y bases de los dedos para determinar si los dedos están extendidos.
  •	Identifica los dedos extendidos y controla los respectivos pines digitales de la placa Arduino.

5.	Visualización y control de Arduino:
  •	Dibuja los puntos clave y las conexiones de la mano en el fotograma.
  •	Controla los pines digitales de la placa Arduino para encender o apagar LEDs según los dedos detectados.



