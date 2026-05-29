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






 




