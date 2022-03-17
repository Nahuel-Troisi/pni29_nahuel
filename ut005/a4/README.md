
<center>

# PACKET TRACER III


</center>

***Nahuel Ivan Troisi*** <br>
***1º de Ciclo Superior de Administración de Sistemas Informáticos en Red*** 

### ÍNDICE

+ [Introducción](#id1)
+ [Objetivos](#id2)
+ [Material empleado](#id3)
+ [Desarrollo](#id4)
+ [Conclusiones](#id5)


#### ***Introducción***. <a name="id1"></a>

Realizaremos una serie de prácticas con Packet Tracer.

#### ***Objetivos***. <a name="id2"></a>

Completar correctamente los ejercicios que nos manda el profesor.

#### ***Material empleado***. <a name="id3"></a>

MV de Kali o en su defecto, de Windows 10 con el programa de Packet Tracer instalado. 

#### ***Desarrollo***. <a name="id4"></a>

## Ejercicio 1. Inalámbrico. Red Abierta.

Paso 1. Insertar un dispositivo inalámbrico Linksys WRT300N (Punto de acceso). Por
defecto, este equipo viene con la configuración 192.168.0.1 y máscara de red
255.255.255.0. Debemos colocar la configuración con la IP 192.168.1.1 y máscara de
red 255.255.255.0. Además, debemos desactivar la asignación de direcciones
mediante DHCP en el dispositivo inalámbrico. <br>

Paso 2. Insertar tres PC’s inalámbricos, con las siguientes configuraciones: <br>

Paso 3. Comprobar la comunicación entre los diferentes PC’s, y su comunicación con
el punto de acceso. Observar esta comunicación en el modo simulación. ¿A qué te
recuerda este tipo de propagación de tramas? <br>

Paso 4. Cambia la configuración de los equipos: <br>


Paso 5. Comprobar la comunicación entre los diferentes PC’s, y su comunicación con
el punto de acceso. Como podemos comprobar, la configuración IP del punto de
acceso no impide una correcta comunicación entre los diferentes PC’s que se conecten
a su red. <br>


## Ejercicio 2. Inalámbricas: varios puntos de acceso.

Paso 1. Insertar dos dispositivos inalámbricos Linksys WRT300N (Punto de acceso).
Cambiar la configuración por defecto a 192.168.1.1 y máscara de red 255.255.255.0 y
192.168.2.1 y máscara de red 255.255.255.0. <br>

Paso 2. Cambiar el SSID de las redes: <br>

Paso 3. Insertar seis PC’s inalámbricos, con las siguientes configuraciones: <br>

Paso 4. Conectar entre sí ambos puntos de acceso por el puerto Ethernet 1. <br>

Paso 5. Comprobar las comunicaciones entre los seis PC’s, verificando que las
comunicaciones no dependen de la red inalámbrica a la que se conecten, sino que
configuran el punto de acceso al que se conectan. <br>

Paso 6. Cambiar el SSID del equipo PC05 de RED1 a red1. Comprobar que, para los
puntos de acceso y las tarjetas de red, ambas configuraciones son diferentes. No es lo
mismo SSID RED1 que SSID red1. <br>



## Ejercicio 3. Inalámbrico: Red cifrado WEP.

Paso 1. Insertar dos dispositivos inalámbricos Linksys WRT300N (Punto de acceso).
Cambiar su configuración a 192.168.1.1 y máscara de red 255.255.255.0 y 192.168.2.1
y máscara de red 255.255.255.0. <br>

Paso 2. Cambiar el SSID de las redes: <br>

Paso 3. Introducir clave WEP en el punto de acceso de la RED1: clave WEP
0123456789. <br>

Paso 4. Insertar tres PC’s con las siguientes configuraciones: <br>


## Ejercicio 4. Inalámbrico: DHCP.

Paso 1. Insertar dos dispositivos inalámbricos Linksys WRT300N (Punto de acceso).
Colocar la configuración a 192.168.1.1 y máscara de red 255.255.255.0 y 192.168.2.1 y
máscara de red 255.255.255.0. <br>

Paso 2. Cambiar el SSID de las redes: <br>

Paso 3. Comprobar la configuración DHCP de los puntos de acceso para comprobar
qué direcciones reparte cada uno de ellos. <br>

Paso 4. Insertar cuatro PC’s con la siguiente configuración: <br>

Paso 5. Cambiar el PC01 de RED1 a RED2. ¿Cambia su dirección IP? Para poder
realizar el cambio, sin apagar y encender el PC, podemos dirigirnos al Escritorio del
equipo, pulsar el botón Configur. IP y pasarla a estática y volver a colocarla en DHCP.
De esta forma se actualiza. No se recomienda en tener dos DHCP en la misma red LAN,
ya que no se puede asegurar cuál de ellos será el que asigne la dirección. Pero de esto
hablaremos más adelante.



#### ***Conclusiones***. <a name="id5"></a>

Esta última práctica ha resultado ser más fácil y rápida de realizar respecto a las anteriores y no me ha supuesto ningún problema. 
