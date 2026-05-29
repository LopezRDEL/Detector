# Detector

#### Proposito
  El proposito de este proyecto es el desarrollo de un chatbot que identifica ciertas partes de un computador 

Entre estas encontramos 

- Procesador (CPU)
- Memoria RAM
- Placa Base (Motherboard)
- Disco duro (O SSD)
- Tarjeta grafica
- Fuente de poder
- Monitor
- Teclado
- Mouse
- Gabinete

# Paso a paso

## Descargar imagenes

1. Descargamos la extension ¨Download all images¨ en la google web store puede usar el siguiente link (https://chromewebstore.google.com/detail/download-all-images/nnffbdeachhbpfapjklmpnmjcgamcdmm)
   
<img width="1141" height="241" alt="Captura de pantalla 2026-05-28 185304" src="https://github.com/user-attachments/assets/072d41db-b6bf-464a-a22f-350809a0d43a" />

2. Se realiza la busqueda del objeto que se quiere escanear por medio de la camara en este caso se buscara el mouse
<img width="1232" height="960" alt="image" src="https://github.com/user-attachments/assets/71c52886-f0ab-4662-80ae-1939376cb15d" />

3. Se abre la extension Download all images y saldra el siguente menú. Se recomiendan por lo menos descargar 100 imagenes de cada objeto para asi mismo tener mayor probabilidad de exito al momento de identificar los elementos.
   
   <img width="931" height="792" alt="image" src="https://github.com/user-attachments/assets/9ca10b93-1eeb-4111-ab5c-f9701ce44b49" />

   Al momento que se carguen las imagenes, se le recomienda al usuario remover las imagenes que no son el elemento seleccionado para este debe darle al boton "Gallery". Finalmente se le dara al boton de "Download"

## Motor de entrenamiento de imagenes

- Para este proyecto se hizo uso de la herramienta Roboflow, a continuacion se le dara el paso a paso a seguir para poder registrar las imagenes que se descargaron en el paso anterior. Con el siguiente link se podra entrar a la web de Roboflow, cree una cuenta para continuar. https://app.roboflow.com/

1. Iniciar sesion
<img width="1260" height="980" alt="image" src="https://github.com/user-attachments/assets/44e601b5-84db-4de4-a095-30e01941bc44" />
2. ir al apartado de "Projects¨ y comenzar a crear un nuevo proyecto
   
3. Se le pedira que ponga un nombre para el proyecto y se selecciona la opcion de "Object detection "  y la opcion "Traditional" <img width="1864" height="866" alt="image" src="https://github.com/user-attachments/assets/4a5d7994-199f-4b24-8a1b-689f5c7842c6" />
 y seguido de eso se le dara clic en " Create Public Project "

4. Se despliega este apartado <img width="1913" height="978" alt="image" src="https://github.com/user-attachments/assets/34010829-6c2c-4421-b8b7-6e0c4265a3a0" />. Paso seguido se le dara clic a la opcion " select folder "
   
5. Se desplegara el explorador de archivos donde el usuario tiene que encontrar la carpeta que le arrojo la extension <img width="930" height="580" alt="image" src="https://github.com/user-attachments/assets/b64d6c72-c5f7-4a00-bace-691d4fe7fe1c" /> se selecciona y abre la carpeta "mouse" ahi comenzara a subir las imagenes descargadas. Automaticamente comenzara a subirlas <img width="1919" height="970" alt="image" src="https://github.com/user-attachments/assets/6794b83d-c805-4a52-aeac-48a0210aa58b" /> . Luego apareceran las imagenes cargadas <img width="1585" height="977" alt="image" src="https://github.com/user-attachments/assets/c430ad4a-9656-4ef6-84c6-d13869223449" />

6.Se le dara a ¨Save and continue ¨ Despues de cargar las imagenes saldra este menu ¨<img width="1919" height="983" alt="image" src="https://github.com/user-attachments/assets/ef54b954-a97d-429e-8774-d05f5e18732e" /> El usuario le dara al boton de ¨Annotate Images¨ Despues se le tendra que dar a la opcion ¨Label myself¨ y se tendra que seleccionar el icono de mouse con brillo y seleccionar el elemento <img width="1919" height="991" alt="image" src="https://github.com/user-attachments/assets/4e6d55f4-d98d-4cb4-8b4f-9ea82fb06a56" />

7. Agregamos la etiqueta del elemento que tenemos <img width="306" height="307" alt="image" src="https://github.com/user-attachments/assets/4830193d-88ae-4201-92b5-ca3ec66ae21c" /> se le dara al boton de add y la etiqueta quedara agregada <img width="316" height="319" alt="image" src="https://github.com/user-attachments/assets/169670a5-4391-4047-948f-d16ad271ea74" />

8. Seleccionamos el objeto y saldra el siguiente menu <img width="1361" height="634" alt="image" src="https://github.com/user-attachments/assets/10c1636b-b08b-4455-aa9c-ebc38982b8a6" /> . Seguido se le dara al boton de save. Paso seguido crear la carpeta con el nombre del elemento y darle ¨Save¨
9. Finalmente se le dara clic a la flecha y continuar con todas las imagenes cargadas. <img width="1803" height="927" alt="image" src="https://github.com/user-attachments/assets/945ab301-e540-489d-94c8-c2933cf47936" />

# 1. Importación de Librerías

<img width="1529" height="855" alt="image" src="https://github.com/user-attachments/assets/d677452b-f273-46e6-a2a5-29a541027aec" />
-    YOLO: Permite cargar el modelo entrenado.
-    cv2: Maneja la cámara y procesamiento de video.
- time: Controla tiempos de espera.

## Carga del Modelo Entrenado
La linea de codigo (model = YOLO("runs/detect/train-2/weights/best.pt"))carga el modelo entrenado previamente.

El archivo best.pt contiene los pesos aprendidos durante el entrenamiento del modelo.

## Apertura de la Cámara

La linea de codigo (cap = cv2.VideoCapture(0, cv2.CAP_DSHOW)) inicializa la cámara web para capturar video en tiempo real

## Configuración de Resolución 
Las lineas (cap.set(cv2.CAP_PROP_FRAME_WIDTH, 640)
cap.set(cv2.CAP_PROP_FRAME_HEIGHT, 480))
define la resolución de captura del video.

## Captura Continua de Video

La linea (while True:) hace que el programa entra en un ciclo infinito para leer constantemente imágenes de la cámara.

## Detección de Objetos

La linea (results = model(frame)) hace que Cada fotograma capturado es enviado al modelo YOLOv8 para identificar objetos.

## Dibujar Resultados

La linea (annotated_frame = results[0].plot())
Hace que se dibujen automáticamente:

* Cajas delimitadoras
* Etiquetas
* Nivel de confianza

sobre los objetos detectados.

## Mostrar Video en Tiempo Real

La linea de codigo (cv2.imshow("Deteccion de Objetos", annotated_frame)) Muestra la ventana con las detecciones realizadas.

# Prueba de Cámara con Pygame

Este parte del código fue utilizado para verificar el correcto funcionamiento de la cámara antes de integrar YOLOv8.

<img width="619" height="806" alt="image" src="https://github.com/user-attachments/assets/6e5e968c-ea01-4d37-8a93-7903a8d44a8f" />

La linea (pygame.camera.init()) Activa el módulo de cámara de Pygame.

## Listado de Cámaras Disponibles
La linea (camaras =
pygame.camera.list_cameras()) Permite detectar cámaras conectadas al computador.


## Captura de Imágenes

La linea (image = cam.get_image()) Obtiene imágenes en tiempo real desde la cámara.

## Visualización en Pantalla 

La linea (screen.blit(image, (0,0))) Muestra el video capturado dentro de una ventana de Pygame.

# 3 Estructura del Proyecto

<img width="272" height="252" alt="image" src="https://github.com/user-attachments/assets/a080c338-a2a7-46e1-bf1c-6c279a360cdb" />

.venv = Entorno virtual del proyecto

dataset = Contiene imágenes para entrenamiento

runs = Guarda resultados y modelos entrenados

train = Datos del entrenamiento

deteccion.py = Código principal de detección

entrenamiento.py = Script de entrenamiento del modelo

test.py = Pruebas de funcionamiento

yolov8n.pt = Modelo base de YOLOv8

<img width="1388" height="636" alt="image" src="https://github.com/user-attachments/assets/21cf2e82-865c-47cc-9d62-2e7bb87ed820" />



<img width="1361" height="623" alt="image" src="https://github.com/user-attachments/assets/2e1de6e4-1a63-4c61-a995-0af2e45a7283" />


<img width="1338" height="478" alt="image" src="https://github.com/user-attachments/assets/b7468ba7-7698-4dcb-9fbf-6ea216afb9d1" />


<img width="1375" height="552" alt="image" src="https://github.com/user-attachments/assets/0d962323-d9de-4ead-853d-588c844c1cdf" />


<img width="1346" height="607" alt="image" src="https://github.com/user-attachments/assets/cc44f4e3-9db2-448c-b9a4-20fe5e544181" />


<img width="1369" height="572" alt="image" src="https://github.com/user-attachments/assets/9394ee10-e741-44b5-a089-3371058d911f" />


<img width="1377" height="206" alt="image" src="https://github.com/user-attachments/assets/43faee61-2a88-4bfc-978d-ebc9ef7ac3fa" />


