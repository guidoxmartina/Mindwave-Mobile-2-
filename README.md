# Mindwave-Mobile-2- OSC 2 TOUCHDESIGNER  
*tutorial para conectar Mindwave mobile 2 con Touchdesigner*



- Comprobar que los drivers de bluetooth estén actualizados desde el administrador de dispositivos

![image](https://user-images.githubusercontent.com/48781895/183589708-47ab1611-b2b4-4a26-a764-3fc83cc50013.png)


- Instalar  [Windows Setup Kit](https://github.com/guidoxmartina/Mindwave-Mobile-2-/blob/1dfc80b88b1585eadc679c6b979f9c9bac5b6eb6/Windows%20Setup%20Kit.zip)(este programa es el que te hacen bajar en el instructivo, pero no funciona, solo tiene que estar abierto ejecutándose en la pc aunque figure ''Status : disconnected')

![image (49)](https://user-images.githubusercontent.com/48781895/183589820-d006e0ec-ead7-4ac5-a2e3-ca8da9079080.png)


- Agregar el dispositivo bluetooth a la pc. Se recomienda primero conectar el que aparece con un icono de una pc, y luego agregar el de los auriculares (si pide una clave es 0000). Tienen que estar ambos emparejados, y si alguno figura como conectado mejor.

![image (50)](https://user-images.githubusercontent.com/48781895/183590470-91d2d121-613b-433a-891c-d74eee28df17.png)


- Controlar que en el administrador de dispositivos figuren 2 dispositivos bluetooth llamados "MindWave Mobile"

![image (51)](https://user-images.githubusercontent.com/48781895/183590677-d3598380-7605-4a40-a4c5-74d77783aac9.png)


- En dispositivos e impresoras debe figurar tambien el MindWave Mobile

![image (52)](https://user-images.githubusercontent.com/48781895/183590866-825d73be-b6ce-499e-99b2-b9ea3b5a1ef8.png)


- Hacer click derecho sobre el dispositivo y entrear a las propiedades. Dentro de este menu ir a Servicios y comprobar que la casilla SPP esta marcada. (Es importante prestar atención al puerto asignado al dispositivo, ya que es necesario mas adelante.
 En este caso es COM3.
 
 ![image (53)](https://user-images.githubusercontent.com/48781895/183590960-04b821c0-a329-4460-9225-2d912fa59299.png)

- Instalar [tutorial_windows_v1.2.3](https://github.com/guidoxmartina/Mindwave-Mobile-2-/blob/1dfc80b88b1585eadc679c6b979f9c9bac5b6eb6/tutorial_windows_v1.2.3.zip)
 
 - Al ejecutar cerrar la ventana emergente y presionar en "Click To Connect". En la ventana que se abre dejar el texto en AUTO y apretar Connect. Luego de unos segundos y de probar en varios puertos el programa debería encontrar el puerto en el que esta conectado el dispositivo automáticamente. Si aparece "error to connect"puede ser por que uno de los dos dispositivos que tienen que figurar como conectados (icono auriculares e icono pc) no esten conectados/emparejados
 
 ![image (54)](https://user-images.githubusercontent.com/48781895/183591075-95f5dfe9-645b-4b84-8979-794cc2598c22.png)
 
 - Si el dispositivo se conecta con exito cambiara el estado
![image](https://user-images.githubusercontent.com/48781895/183591675-01c1e05c-d21b-4d79-b597-c75bbb34dab1.png)
 
- Se debe colocar de forma tal que el clip de oreja quede del lado izquierdo -

![image](https://user-images.githubusercontent.com/48781895/183591928-7342cee2-531f-4ceb-8d4e-5f28b9a9f3ea.png)

- En la pestaña "Try" se puede probar un poco el dispositivo
- Desde esta pagina se pueden bajar aplicaciones  https://store.neurosky.com/collections/apps

- ?????Al terminar la conexión cerrar la aplicación ???????????????
HAY Q CERRARLA SIOSI?


# Señal-OSC
Sacado de https://github.com/trentbrooks/BrainWaveOSC

- Luego de conectar correctamente el dispositivo instalar [BrainWaveOSC_WIN_0.98](https://github.com/guidoxmartina/Mindwave-Mobile-2-/blob/1dfc80b88b1585eadc679c6b979f9c9bac5b6eb6/BrainWaveOSC_WIN_0.98.zip)

- En esta parte vamos a necesitar el numero/nombre de puerto ANTES MENCIONADO. Este se puede obtener entrando a las propiedades del dispositivo presionando click derecho sobre el icono de MindWave Mobile en "Dispositivos e impresoras". Especificamente en la pestaña "servicios". En este caso es ¨COM3¨
![image](https://user-images.githubusercontent.com/48781895/183592634-fd82ed95-eb92-45dd-beaa-31d818f69662.png)

- Editar con un block de notas el archivo "settings.xml" ubicado dentro de la carpeta "data" que se encuentra en la misma carpeta que la aplicación.
En la linea 5 entre <value>........<value> debemos escribir el nombre del puerto al que se esta conectando nuestro dispositivo
![image (55)](https://user-images.githubusercontent.com/48781895/183592737-5d043d61-539b-444b-851c-8e04a2cea9cc.png)

Cerrar y guardar los cambios del block de notas

- Luego de esto al ejecutar el programa debería abrirse con el fondo en verde e indicar que llega algo de señal
![image (56)](https://user-images.githubusercontent.com/48781895/183592825-f7408a60-f37b-4af0-931c-6978b6bf8cc8.png)

# TOUCHDESIGNER-OSC
Mediante el CHOP ¨OSC In¨ recibiremos los datos del BRAINWAVE OSC en touchdesigner

- Para esto debemos copiar a Touchdesigner el Network Port que figura en la interfaz y en el archivo "settings.xml" del BRAINWAVE OSC. En este caso es 7771
![image (57)](https://user-images.githubusercontent.com/48781895/183593018-d40d9b63-2d27-4a71-aad8-a5b480999550.png)

![image (58)](https://user-images.githubusercontent.com/48781895/183593043-8feb1330-1151-4034-8cbb-5ebba4376957.png)

Ejemplo [TOE Touchdesigner](https://github.com/guidoxmartina/Mindwave-Mobile-2-/blob/main/Neuro-Touchdesigner.toe)


## Fuentes
- https://www.youtube.com/watch?v=GZl89BtTno0 (los archivos de la descripcion estan desactualizados)
- https://github.com/trentbrooks/BrainWaveOSC
