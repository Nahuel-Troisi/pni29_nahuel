
<center>

# PACKET TRACER I


</center>

***Nahuel Ivan Troisi*** <br>
***1º de Ciclo Superior de Administración de Sistemas Informáticos en Red.*** 

+ [Introducción](#id1)
+ [Objetivos](#id2)
+ [Material empleado](#id3)
+ [Desarrollo](#id4)
+ [Conclusiones](#id5)


#### ***Introducción***. <a name="id1"></a>

Vamos a realizar una serie de prácticas con el programa de Packet Tracer.

#### ***Objetivos***. <a name="id2"></a>

Completar todas las actividades que nos pide el profesor.

#### ***Material empleado***. <a name="id3"></a>

Programa de Packet Tracer y una MV de Kali Linux. 

#### ***Desarrollo***. <a name="id4"></a>



## Ejercicio 2. Tipos de cables en uniones entre equipos. <br><br>



Paso 1. Unión de un PC con otro. Utilizar el cable adecuando de par trenzado hasta
que se produzca comunicación (luces en verde en ambos extremos). <br><br>



Paso 2. Unión de un PC con un switch (utilizaremos un 2950‐24 para todas las
experiencias). Utilizar el cable adecuando de par trenzado hasta que se produzca
comunicación (luces en verde en ambos extremos). <br><br>



Paso 3. Unión de un switch con otro. Utilizar el cable adecuando de par trenzado
hasta que se produzca comunicación (luces en verde en ambos extremos). <br><br>



Paso 4. Unión de un PC con un router (utilizaremos el 1841 en todas las
experiencias). Utilizar el cable adecuando de par trenzado hasta que se produzca
comunicación (luces en verde en ambos extremos). <br><br>



Paso 5. Unión de un switch con un router. Utilizar el cable adecuando de par
trenzado hasta que se produzca comunicación (luces en verde en ambos extremos). <br><br>



Paso 6. Unión de un switch con un hub (utilizaremos el HUB‐PT). Utilizar el cable
adecuando de par trenzado hasta que se produzca comunicación (luces en verde en
ambos extremos). <br><br>

<img src="https://github.com/Nahuel-Troisi/pni29_nahuel/blob/02f20556fc510ea236f8091ef6d3d749acab20ba/ut005/a2/ejercicio%202.png">



## Ejercicio 3. Diferencias entre Hub y Switch. <br><br>



Paso1. Añadimos un Generic Hub‐PT, que nos presenta un pequeño hub con 6
puertos Fast Ethernet. <br><br>

Paso 2. Añadimos 3 ordenadores con las siguientes configuraciones: <br><br>

|       |               | Máscara de red  |
|-------|---------------|-----------------|
| PC 01 | 192.168.5.101 | 255.255.255.0   |
| PC 02 | 192.168.5.102 | 255.255.255.0   |
| PC 03 | 192.168.5.103 | 255.255.255.0   |

<br>

Paso 3. Conectar los 3 equipos con el hub utilizando el cableado adecuado. <br><br>

Paso 4. Comprobar la conectividad entre los equipos realizando un ping entre ellos. <br><br>

<img src="https://github.com/Nahuel-Troisi/pni29_nahuel/blob/main/ut005/a2/ejercicio%203.4.png"> <br>

Paso 5. Una vez comprobada la conectividad, pasar del modo Tiempo Real al modo
Simulación y volver a realizar un ping entre equipos. Se debe reiniciar la configuración
para poder apreciar los paquetes ICMP entre los equipos. Para realizar correctamente
esta experiencia, y no tener más información que la necesaria, aplicar un filtro de
eventos que sólo nos presente los paquetes ARP e ICMP (que son los necesarios para
comprobar el funcionamiento del ping). Comprobar también tablas ARP aprendidas,
ejecutando el comando arp -a en uno de los equipos. <br><br>

<img src="https://github.com/Nahuel-Troisi/pni29_nahuel/blob/main/ut005/a2/ejercicio%203.5.png"> <br>

Paso 6. Realizar las mismas pruebas cambiando el Generic Hub‐PT por un switch 2950‐
24. Grabar el proyecto con un nuevo nombre. Comprobar la diferencia entre ambas
experiencias. <br><br>

<img src="https://github.com/Nahuel-Troisi/pni29_nahuel/blob/main/ut005/a2/ejercicio%203.6.png"> <br>


## Ejercicio 4. Configuración manual de un switch. <br><br>

Paso 1. Insertar un Switch‐PT‐Empty, que nos presenta un switch vacío, en el que se nos presenta un equipo al que se le pueden añadir 10 elementos de conectividad de
red, aunque sólo disponemos de 5 tipos de puertos a poderle añadir. <br><br>

Paso 2. Añadir cada uno de los 5 puertos posibles a añadir en dicho switch. Estos puertos los encontramos en la pantalla de
configuración del switch, en la pestaña de físico (recordar que, para añadir nuevos elementos de conexión hay que tener el switch apagado). <br><br>

Paso 3. Añadir 5 ordenadores para poderlos conectar a esos 5 tipos de puertos
diferentes. Para ello debemos cambiar los puertos que vienen por defecto en los
ordenadores. <br><br>

Paso 4. Realizar la conexión de los 5 equipos con el switch y comprobar la
conectividad entre ellos utilizando la siguiente configuración para los ordenadores: <br>

| Nombre | Dirección IP | Máscara de red  |
|--------|--------------|-----------------|
| PC 01  | 192.168.2.11 | 255.255.255.0   |
| PC 02  | 192.168.2.12 | 255.255.255.0   |
| PC 03  | 192.168.2.13 | 255.255.255.0   |
| PC 04  | 192.168.2.14 | 255.255.255.0   |
| PC 05  | 192.168.2.15 | 255.255.255.0   |

<br>

<img src="https://github.com/Nahuel-Troisi/pni29_nahuel/blob/main/ut005/a2/ejercicio%204.1.1.png"> <br>


## Ejercicio 5. Unión entre switchs de comunicaciones. <br><br>

Paso 1. Colocar 4 switchs 2950‐24, cambiando sus nombres a SW01, SW02, SW03 y SW04. <br><br>

Paso 2. Realizar las siguientes conexiones entre switchs: <br>

| Switch Origen | Puerto Origen | Switch Destino | Puerto Destino |
|---------------|---------------|----------------|----------------|
| SW 01         | 2             | SW 02          | 1              |
| SW 01         | 3             | SW 03          | 1              |
| SW 02         | 4             | SW 04          | 2              |

<br>

Paso 3. Insertar los siguientes equipos con sus correspondientes configuraciones: <br>

| Nombre | IP         | Máscara     | Switch | Puerto |
|--------|------------|-------------|--------|--------|
| PC 01  | 10.0.1.101 | 255.255.0.0 | SW 01  | 11     |
| PC 02  | 10.0.1.102 | 255.255.0.0 | SW 02  | 12     |
| PC 03  | 10.0.1.103 | 255.255.0.0 | SW 03  | 13     |
| PC 04  | 10.0.1.104 | 255.255.0.0 | SW 04  | 14     |

<br>

Paso 4. Comprobar la conectividad de los 4 equipos. <br><br>

<img src="https://github.com/Nahuel-Troisi/pni29_nahuel/blob/main/ut005/a2/ejercicio%204.4.png"> <br>

Paso 5. Introducir una nueva conexión entre switchs entre el SW01 puerto 4 y el
SW04 puerto 1. Esto crea un circuito entre los equipos. Comprobar qué sucede con la
comunicación entre equipos. <br><br>

<img src="https://github.com/Nahuel-Troisi/pni29_nahuel/blob/main/ut005/a2/ejercicio%204.5.png"> <br>

Paso 6. Eliminar la última conexión realizada. Añadir un Generic Hub‐PT y
denominarlo HUB05. Utilizando el puerto 1 de este hub, unirlo al SW04 puerto 1.
Insertar un nuevo equipo con la configuración PC05, 10.0.5.105, 255.255.0.0, al puerto
del hub número 5. Comprobar la conectividad de los 4 equipos anteriores con éste. <br><br>

<img src="https://github.com/Nahuel-Troisi/pni29_nahuel/blob/main/ut005/a2/ejercicio%204.6.png"> <br>


#### ***Conclusiones***. <a name="id5"></a>

La práctica en general ha sido bastante sencilla, aunque ha habido algunos inconvenientes, ya que mi equipo de clase no permite la instalación del Packet Tracer y he tenido que usar una MV para poder realizar la práctica. 
