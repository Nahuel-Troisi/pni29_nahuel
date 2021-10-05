# ACTIVIDAD 1 PNI

### 1. Defina los tres modos de transmisión.
Existen tres tipos de transmisión:

- __Simplex__ : Los datos fluyen en una única dirección. Un claro ejemplo sería la radio o la televisión.  

- __Half-duplex__ : En este caso, los datos se transmiten de forma bidireccional, es decir, en ambos sentidos, pero no pueden ser procesados de forma simultanea. 

- __Full-duplex__ : Los datos se transmiten en ambos sentidos y de forma simultanea.  

### 2. Indique las ventajas de cada tipo de topología de red.

En primer lugar, la red de tipo __Bus__ posee como ventaja principal el hecho de compartir información de manera directa con todos los dispositivos que se conecten a la red.
Por otro lado, la red de tipo __Anillo__ permite a los dispositivos conectarse entre sí mediante una cadena. 
No obstante, la red de tipo __Estrella__ permite que los nodos de comuniquen entre sí.
En cuanto a la red de tipo __Estrella Extendida__ ofrece las mismas características que la red anterior además de acortar el cableado necesario para conectar los dispositivos. 
Aun así, la red de tipo __Jerárquica__ permite una conexión en forma de ramificación escalonada, de manera que se aislan los fallos por capas. 
Finalmente, la red de tipo __Malla__ permite a todos los dispositivos estar conetados entre sí aunque uno de los nodos falle. 


### 3. ¿Cuáles son los factores que determinan que un sistema de comunicación sea una LAN, MAN o WAN?
El factor diferencial de estos tres tipos de redes es principalmente el tamaño del  mismo, que se clasifica de la siguiente manera:

- __LAN__ : Pensada principalmente para uso doméstico, ya sea en una planta o edificio, cuya característica principal es la alta velocidad de transferencia y su fiabilidad.  
- __MAN__ : Es el tipo de red empleada en las áreas metropolitanas, pudiendo abarcar ciudades enteras. 
- __WAN__ : Permite la conexión de redes de área extensa, es decir, entre países y continentes. No obstante, suelen ser redes de muy baja velocidad de transferencia y alta tasa de errores. 


### 4. Enumere las cinco topologías básicas de red.
- Topología de Bus 
- Topología de Anillo
- Topología de Estrella
- Topología Jerárquica
- Topología en Malla


### 5. Indique una desventaja de cada tipo de topología de red.
En el caso de la __Topología de Bus__, posee un mantenimiento de la red muy costoso. En cuanto a la __Topología de Anillo__, si falla un canal, falla toda la red. Por otro lado, la __Topología de Estrella__ depende de las limitaciones del HUB o SWITCH a la hora de conectar muchos dispositivos a la red. En cuanto a la __Topología Jerárquica__, si el nodo principal falla, ocasiona un efecto dominó en toda la red. Finalmente, la __Topología en Malla__ requiere un capital muy grande para la creación de la misma.    


### 6. Para una red con n dispositivos, ¿cuál es el número de enlaces de cable necesarios para una malla, un anillo, un bus y una topología en estrella?
- En el caso de la __Topología en Malla__, se necesita __N(N-1)/2__ dispositivos por enlace. 
- En cuanto a la __Topología en Bus__, se necesita __N__  dispositivos por cada __N+1__  enlaces.
- Por otro lado, la __Topología de Anillo__ necesita __N__  dispositivos por cada __N__  enlaces.
- La __Topología en Estrella__ posee un concentrador, el cual necesita  __N__ puertos por cada __N__ dispositivos.  
### 7. Para cada tipo de topología de red, indique las implicaciones de que exista un fallo de un único cable.
En el caso de la __Topología de Bus__, un fallo en el enlace provocaría una interrupción en todas las transmisiones. Por otro lado, en la  __Topología de Anillo__, la ruptura de cualquier enlace provocaría la caida de toda la red. En cuanto a la __Topología de Estrella__, si falla un enlace, únicamente se vería afectado dicho enlace, cacaterística que comparte con la __Topología Jerárquica__. Finalmente, la __Topología en Malla__ redirigiría la red por otro enlace si alguno de estos falla. 



### 8. ¿Qué es una intranet? ¿Qué es Internet?
- Una __Intranet__ es un conjunto de redes interconectadas entre sí. Utilizada normalmente en empresas.
- __Internet__ es la red de ámbito mundial, cuyo acceso está permitido a cualquier usuario. Comúnmente conocido como World Wide Web (WWW).


### 9. ¿Qué topología necesita un controlador central o un concentrador?
Necesita una topología de tipo __Estrella__


### 10. La comunicación entre una computadora y un teclado implica una transmisión ...
De tipo __Simplex__

### 11. En una red con 25 computadoras, ¿qué topología necesitaría el cableado más extenso?
Una __Topología en Malla__


### 12. Una topología en árbol es una variación de una topología en ...
Topología en __Estrella__

### 13. Una conexión ...  proporciona un enlace dedicado entre dos dispositivos.
De tipo __Punto a Punto__


### 14.En la transmisión ... , la capacidad del canal es siempre compartida por los dos dispositivos que se comunican.
De tipo __Full-Duplex__


### 15. Una rotura de cable en una topología en ... detiene toda la transmisión.
El tipo __Bus__


### 16. Una red que contiene múltiples concentradores está configurada muy probablemente como una topología en ...
Forma de __Árbol o Jerárquica__



### 17. Defina el tipo de topología de las siguientes figuras:

!(~/pni29_nahuel/ut0001/a1/img0001.png)	

### 18. Relacione los conceptos siguientes con una topología de red (cada uno se puede aplicar a más de una topología):

###       a) Se pueden añadir nuevos dispositivos fácilmente.

###       b) El control se efectúa a través de un nodo central.

###       c) El tiempo de transmisión se gasta reenviando los datos a través de nodos intermedios.

### 19. Cuando alguien hace una llamada telefónica local a otra persona, ¿está usando una configuración de línea punto a punto o multipunto? Explique su respuesta.
En este caso, se está utilizando una configuración de línea __Punto a Punto__, ya que dos, y únicamente dos, dispositivos se conectan a través del enlace dedicado. 



### 20. ¿Qué modo de transmisión (símplex, semidúplex o full-dúplex) se puede comparar a los siguientes?

###     a ) Una conexión computadora a monitor.

###     b ) Una conversación educada entre tía Gertrudis y tía Rowena. 

###     c ) Una emisión por televisión.


