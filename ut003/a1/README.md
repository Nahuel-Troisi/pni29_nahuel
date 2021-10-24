# ACTIVIDAD 1 PNI

### 1.¿Qué niveles OSI son los niveles de soporte de red?
Los niveles OSI de soporte de __red__ corresponden a:
- Capa Física
- Capa de Enlace de Datos
- Capa de Red
### 2.¿Qué niveles OSI son los niveles de soporte de usuario?
Los niveles OSI de soporte de __usuario__ pertenecen a:
- Capa de Sesión 
- Capa de Presentación 
- Capa de Aplicación 
### 3.¿Cómo están OSI e ISO relacionadas entre sí? 
El acrómino __ISO__ pertenece a las siglas __Organización Internacional de Estandarización__, cuya función es publicar los estándares
de comunicación a nivel internacional, mientras que la __OSI__ , comunmente conocido como el modelo de __Interconexión de Sistemas Abiertos__, es 
la base del modelo ISO, no obstante, su cometido es organizar la comunicación entre equipos de distinta procedencia. 
### 4.Enumere los niveles del modelo OSI. 
El modelo __OSI__ se divide en siete capas:
- Capa de Aplicación
- Capa de Presentación
- Capa de Sesión
- Capa de Transporte
- Capa de Red
- Capa de Enlace de Datos
- Capa Física
### 5.¿Cómo pasa la información de un nivel OSI al siguiente?
Por parte del __emisor__, la información circula en órden descendente, por lo que se mueve desde los niveles superiores a los
inferiores, mientras que el __receptor__ funciona de manera contraria, es decir, la información se transmite desde los niveles inferiores a los
superiores de manera ascendente. 
### 6.¿Qué son las cabeceras y cola y cómo se añaden y se quitan?
Las cabeceras son datos que se añaden en cada uno de los niveles por los protocolos correspondientes con la finalidad de proporcionar 
sus respectivos servicios. Dichas cabeceras se añaden según descienden en el caso del emisor, mientras que se eliminan en el caso del receptor a 
medida que ascienden. 
### 7.¿Cuáles son las responsabilidades del nivel físico?
El __nivel físico__ es el responsable de caracterizar su medio: cables, conectores, adaptación al medio, pines, 
funciones, niveles de tensión, etc. Se encarga de transferir los bits al medio de transmisión.
### 8.¿Cuáles son las responsabilidades del nivel de enlace?
El __nivel de enlace__ es el responsable de convertir el medio de transmisión en un medio seguro. Por ello sus funciones son la detección y 
corrección de errores, función que realiza entre nodos consecutivos. También se encarga del direccionamiento físico y de la 
encapsulación de los paquetes en tramas.
### 9.¿Cuáles son las responsabilidades del nivel de red? 
Las responsabilidades principales del __nivel de red__ son el encaminamiento o enrutamiento de los paquetes a través de la red 
interconectada de routers y el direccionamiento a nivel lógico.

### 10.¿Cuáles son las responsabilidades del nivel de transporte? 
El __nivel de transporte__ es el nivel que actúa de intermediario entre los niveles superiores e inferiores.
Sus funciones principales son la división de los datos en segmentos, realizar el control de flujo (cantidad de datos que son enviados por el emisor 
según la capacidad de procesamiento del receptor), control de congestión (cantidad de datos circulando por la red en un determinado momento), 
comunicación extremo a extremo y control de errores entre extremos.

### 11.El nivel de transporte crea una conexión entre el origen y el destino. ¿Cuáles son los tres eventos involucrados en la conexión?

### 12.¿Cuál es la diferencia entre una dirección de punto en servicio, una dirección lógica y una dirección fisica? 

### 13.¿Cuáles son las responsabilidades del nivel de sesión? 

### 14.Cuáles son las responsabilidades del nivel de presentación? 

### 15.¿Cuál es el objetivo de la traducción en el nivel de presentación? 
El objetivo es que las aplicaciones puedan trabajar de forma independiente al tipo de codificación utilizada.
### 16. Indique alguno de los servicios proporcionados por el nivel de aplicación. 
Podemos citar varios servicios, como por ejemplo:
- Servicios de terminal remoto (Telnet)
- Servicios de correo 
- Servicios de transferencia de ficheros (FTP)
- Servicios web
- Servicios DNS
- Servicios DHCP
### 17. ¿Cómo se relacionan los niveles de la familia del protocolo TCP/IP con los niveles del modelo OSI?
<center>
![](./img0004.png)
</center>
### 18. El nivel____________ decide la localización de los puntos de sincronización.
- a) de transporte
- __b) de sesión__
- c) de presentación
- d) de aplicación
### 19.En el nivel _______________, la unidad de datos se denomina trama.
- a) físico
- __b) de enlace de datos__
- c) de red
- d) de transporte
### 20.Los servicios de correo y de directorio están disponibles a los usuarios de la red a través del nivel:
- a) de enlace de datos
- b) de sesión
- c) de transporte
- __d) de aplicación__
### 21.A medida que los paquetes de datos se mueven  de los niveles inferiores a los superiores las cabeceras:
- a) añadidas
- __b) eliminadas__
- c) recolocadas
- d) modificadas
