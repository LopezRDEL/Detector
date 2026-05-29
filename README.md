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
   
3. Se le pedira que ponga un nombre para el proyecto y se selecciona la opcion de "Object detection " <img width="1219" height="891" alt="image" src="https://github.com/user-attachments/assets/91a657d4-6d4f-4d63-ae5d-2c84f71c2db3" />

4. Se despliega la siguiente pestaña y se le dara clic en ¨Start ¨<img width="1242" height="972" alt="image" src="https://github.com/user-attachments/assets/57cfc18b-a4a8-4b00-b234-584fcde65685" /> y seguido de eso se le dara clic en "Use Traditional Model Builder Instead "
5. 


