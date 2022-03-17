
<center>

# PACKET TRACER II


</center>

***Nahuel Ivan Troisi*** <br>
***1º de Ciclo Superior de Administración de Sistemas Informáticos en Red.*** 

### ÍNDICE

+ [Introducción](#id1)
+ [Objetivos](#id2)
+ [Material empleado](#id3)
+ [Desarrollo](#id4)
+ [Conclusiones](#id5)


#### ***Introducción***. <a name="id1"></a>

Realizaremos una serie de prácticas en Packet Tracer. 

#### ***Objetivos***. <a name="id2"></a>

Realizar correctamente los ejercicios que se piden.

#### ***Material empleado***. <a name="id3"></a>

MV de Kali Linux o en su defecto, de Windows 10 con el programa de Packet Tracer. 

#### ***Desarrollo***. <a name="id4"></a>

## Ejercicio 5. Direccionamiento IP. <br><br>

Paso 1. Insertar tres switchs 2950‐24 con los nombres SW01, SW02 y SW03, con la
siguiente configuración: <br>

|       |   | Switch Destino | Puerto Destino |
|-------|---|----------------|----------------|
| SW 01 | 2 | SW 02          | 1              |
| SW 01 | 3 | SW 03          | 1              |

<br>

Paso 2. Insertar los 15 equipos con la siguiente configuración: <br>

| Nombre | IP            | Máscara         | Switch | Puerto |
|--------|---------------|-----------------|--------|--------|
| PC 01  | 192.168.1.101 | 255.255.255.0   | SW 01  | 11     |
| PC 02  | 192.168.1.121 | 255.255.255.248 | SW 02  | 11     |
| PC 03  | 192.168.1.140 | 255.255.255.192 | SW 03  | 11     |
| PC 04  | 192.168.1.160 | 255.255.255.128 | SW 01  | 12     |
| PC 05  | 192.168.1.1   | 255.255.255.0   | SW 02  | 12     |
| PC 06  | 192.168.1.11  | 255.255.255.224 | SW 03  | 12     |
| PC 07  | 192.168.1.111 | 255.255.255.128 | SW 01  | 13     |
| PC 08  | 192.168.1.200 | 255.255.255.240 | SW 02  | 13     |
| PC 09  | 192.168.1.201 | 255.255.255.0   | SW 03  | 13     |
| PC 10  | 192.168.1.248 | 255.255.255.128 | SW 01  | 14     |
| PC 11  | 192.168.1.144 | 255.255.255.192 | SW 02  | 14     |
| PC 12  | 192.168.1.211 | 255.255.255.240 | SW 03  | 14     |
| PC 13  | 192.168.1.25  | 255.255.255.128 | SW 01  | 15     |
| PC 14  | 192.168.1.33  | 255.255.255.224 | SW 02  | 15     |
| PC 15  | 192.168.1.222 | 255.255.255.0   | SW 03  | 15     |

<img src="https://github.com/Nahuel-Troisi/pni29_nahuel/blob/main/ut005/a3/5.2.png"><br>

Paso 3. Calcular, de forma manual, qué equipos se comunican entre ellos.
Comprobar estos cálculos con los aportados por las comunicaciones del ejemplo. <br><br>

~~~
Comprobamos la conexión entre equipos uno a uno y llegamos a la siguiente conclusión:
~~~

<img src="https://github.com/Nahuel-Troisi/pni29_nahuel/blob/main/ut005/a3/5.3.png"><br>

Paso 4. Comprobar las direcciones MAC que
ha aprendido cada uno de los switchs. Para ello,
entramos en el modo consola de cada uno de
los switchs.  
Dentro de ese modo consola, debemos entrar
en el modo privilegiado del sistema. Esto se
consigue tecleando el comando enable.
Después, al cambiar el prompt de petición a
tener un #, colocaremos el comando show
mac‐address‐table. <br>

<img src="https://github.com/Nahuel-Troisi/pni29_nahuel/blob/main/ut005/a3/5.4.1.png"><br>
<img src="https://github.com/Nahuel-Troisi/pni29_nahuel/blob/main/ut005/a3/5.4.2.png"><br>
<img src="https://github.com/Nahuel-Troisi/pni29_nahuel/blob/main/ut005/a3/5.4.3.png"><br>


Verificamos que los resultados eran los
requeridos.
Señalar que, si no hay comunicación entre los equipos durante un tiempo, esta tabla se
vacía.
Comprobar también que en los equipos podemos verificar las relaciones direcciones IP
y MAC de los equipos con los que nos hemos comunicado mediante el comando
arp –a.
Sobre la máquina virtual (no sobre el simulador) realizamos un ping a la dirección
www.google.es. Este ping debe ser correcto. Comprobar y explicar qué elementos
aparecen al realizar el comando arp –a después de esta comunicación. <br><br>

<img src="https://github.com/Nahuel-Troisi/pni29_nahuel/blob/main/ut005/a3/5.4.4.png"><br>
<img src="https://github.com/Nahuel-Troisi/pni29_nahuel/blob/main/ut005/a3/5.4.5.png"><br>

~~~
Al hacer ping a una nueva IP, esta se registra en la tabla ARP y se añade a la misma,
por eso vemos que hay datos que han cambiado. 
~~~

Paso 5. Cambiar la configuración de tal forma que los equipos se comuniquen en
grupos de 5 equipos (primer grupo PC01 al PC05, segundo grupo PC06 al PC10, tercer
grupo PC11 al PC15). <br><br>

~~~
Para poder realizar este ejercicio, lo que debemos hacer es dividir
los 5 grupos con 5 máscaras de red distintas y para mayor comodidad,
cambiar las IP de los PC para que sean más fáciles de reconocer. 
~~~

## Ejercicio 6. Seguridad y configuraciones de un switch. <br><br>

Paso 1. Establecer la conexión con el switch utilizando la opción de enlace por Consola y Terminal. <br><br>

Paso 2. Establecer el nombre del equipo. Este es uno de los primeros pasos que se
suele realizar al configurar un switch. En nuestro caso, le pondremos el nombre
Mi_primer_switch. Esta acción la realizamos desde el modo comando de la siguiente
forma: <br>
Switch> enable (entra en el modo privilegiado de configuración) <br>
Switch# configure terminal (entra en el modo de configuración que es el que permite
el cambio de los parámetros del switch) <br>
Switch(config)# hostname Mi_primer_switch (cambia el nombre) <br>
Mi_primer_switch (config)# (vemos como ya ha cambiado el nombre) <br><br>

<img src="https://github.com/Nahuel-Troisi/pni29_nahuel/blob/main/ut005/a3/6.2.png"> <br>

Paso 3. Desactivar avisos de consola. Es una acción muy habitual, ya que, con cada
modificación del estado de alguno de los parámetros del switch, se presenta un
mensaje por consola. Por ejemplo, cuando apagamos o encendemos un equipo, se
presentan mensajes del estado de ese puerto en el que estaba conectado el equipo.
Debemos comprobar que esto es así, y, usando los comandos siguientes,
comprobaremos que ya no se presentan dichas alertas. <br>
Switch> enable <br>
Switch# configure terminal <br>
Switch(config)# no logging console (para la aparición de mensajes por consola) <br><br>

Paso 4. Contraseñas de acceso. Si nuestro switch es una parte importante de nuestra
configuración de red, es lógico que protejamos su acceso mediante el uso de
contraseñas. <br>
En primer lugar, podemos establecer una contraseña para acceder al modo
privilegiado. Esto lo hacemos con los siguientes comandos: <br>
Switch> enable <br>
Switch# configure terminal <br>
Switch(config)# enable secret ciscoenable (activa y fija la contraseña del modo
privilegiado a ciscoenable) <br>
Y después activamos la contraseña para la entrada mediante consola:
Switch(config)# line console 0 (se puede colocar una contraseña diferente para
cada tipo de acceso; nosotros estamos entrando por consola; ver que cambia el
prompt del sistema) <br>
Switch(config)# password cisco (coloca como contraseña la palabra cisco) <br>
Switch(config‐line)# login (activa la solicitud de contraseña por consola) <br>
Debemos comprobar que esto funciona, por lo que nos desconectaremos de la consola
y volveremos a entrar. <br>
Para desactivar la contraseña del modo consola, llegando a config‐line tecleamos no
login. Para desactivar la contraseña del modo privilegiado, llegando a config tecleamos
no enable secret. <br>
La mayoría de los desactivados en IOS CISCO se hacen colocando el comando no por
delante del comando que lo activó. <br><br> 

<img src="https://github.com/Nahuel-Troisi/pni29_nahuel/blob/main/ut005/a3/6.4.png"> <br>


Paso 5. Configurar dirección IP, máscara y puerta de enlace del switch.
La dirección IP del propio switch la configuramos para su acceso a través de la VLAN1.
Por eso, muchos fabricantes, llaman a esta VLAN1 la de gestión, ya que el
equipamiento de red configura por ahí su acceso remoto por IP. <br>
En modo comando, lo hacemos así: <br>
Switch> enable <br>
Switch# configure terminal <br>
Switch(config)# interface vlan 1 (entramos en la configuración de la vlan 1) <br>
Switch(config‐if)#ip address 192.168.1.254 255.255.255.0 (colocamos la IP y la
máscara) <br>
Switch(config‐if)# no shutdown (este comando activa el interface que acabamos
de configurar) <br>
Switch(config)# exit (salimos a la configuración general) <br>
Switch(config)# ip default‐gateway 192.168.1.1 (configuramos la puerta de enlace
predeterminada para todas las comunicaciones de gestión del switch; hay que
colocarlo si queremos acceder a él a través de un router, o para que se conecte a
Internet para descargar actualizaciones, etc.) <br>
Podemos comprobar que la IP funciona realizando un ping desde un equipo que esté
enganchado al switch. <br><br>

<img src="https://github.com/Nahuel-Troisi/pni29_nahuel/blob/main/ut005/a3/6.5.png"> <br>

Paso 6. Guardar la configuración.
Con todos los pasos anteriores, hemos modificado la configuración de nuestro switch,
pero existe un problema: no hemos guardado la configuración.
Para verificar que esto es así, procedemos a recargar la configuración, que sería como
apagar y volver a encender el switch. <br>
Switch> enable <br>
Switch# reload <br>
Al iniciar, comprobamos que los cambios en el switch no están (nombre del switch,
direcciones IP, etc.). <br>
Volvemos a colocar el nombre al switch, y ahora grabaremos los cambios. Para realizar
esta acción, debemos saber que un equipo CISCO posee dos ficheros de configuración:
running‐config: almacena la configuración que está en ejecución en este momento. Es
sobre la que hemos realizado los cambios hasta ahora. Este fichero, al iniciar el
sistema, se sobre escribe con otro fichero: startup‐config. <br>
startup‐config: como su nombre indica, es el fichero de configuración que se carga en
el sistema al iniciar el mismo, y realiza una copia de si mismo sobre el fichero running‐
config. <br>
Con esta configuración, si en algún momento uno de los parámetros de configuración
que tocamos provoca un comportamiento inadecuado, podemos solucionarlo
volviendo a una configuración estable con solo reiniciar el switch. <br>
Para grabar la configuración, sólo debemos realizar una copia del fichero running‐
config sobre el fichero startup‐config. La forma de hacerlo no puede ser más clara: <br>
Switch> enable  <br>
Switch# copy running‐config startup‐config <br>
Ahora, realizamos un cambio en el nombre del switch (Paso 2), copiamos la
configuración y reiniciamos el switch. De esta forma comprobamos que nuestro equipo
ha mantenido el cambio de nombre. <br>
También volveremos a realizar el paso 5 de colocar la IP, ya que la necesitamos en el
paso siguiente, y grabaremos la configuración. Podemos comprobar que la IP funciona
realizando un ping desde un equipo que esté enganchado al switch. <br><br>

<img src="https://github.com/Nahuel-Troisi/pni29_nahuel/blob/main/ut005/a3/6.6.png"> <br>

Paso 7. Acceso mediante Telnet.
Además de tener configurada una dirección IP para nuestro switch, éste posee 5
conexiones para telnet desde el exterior que pueden ser activadas. Lógicamente, al ser
conexiones externas, se debe establecer una contraseña para dicha conexión. Estas
acciones se realizan mediante lo comandos: <br>
Switch> enable <br>
Switch# configure terminal <br>
Switch# enable password cisco (debe tener contraseña el acceso al switch hasta
por consola) <br>
Switch(config)# line vty 0 4 (accedemos a la configuración de los 5 interfaces telnet) <br>
Switch(config‐line)# password cisco (colocamos la contraseña cisco para
accede mediante telnet) <br>
Switch(config‐line)# login (activamos la petición de contraseña)  <br>
Ahora, procederemos a acceder desde un ordenador conectado a ese switch mediante
la opción de Escritorio, entrando en el modo comando, e invocando el comando
Telnet <br><br>

<img src="https://github.com/Nahuel-Troisi/pni29_nahuel/blob/main/ut005/a3/6.7.png"> <br>


## Ejercicio 7. Configuración de puertos. <br><br>

Paso 1. Auto‐negociación o fijado de velocidad.
Esta configuración la haremos utilizando el switch 2950T que posee dos puertos
Gigabit. En el PC que utilicemos vamos a colocar, en lugar de la tarjeta estándar que
viene, una tarjeta de par trenzado Gigabit. De esta forma tendremos una unión entre
el switch y el PC a Gigabit.
Veamos cual es la situación normal del puerto: <br>
Switch# show interfaces GigabitEthernet1/1  <br>

<img src="https://github.com/Nahuel-Troisi/pni29_nahuel/blob/main/ut005/a3/7.1.png"> <br>

De esta forma comprobamos la velocidad del puerto. <br>
Si queremos cambiarla, utilizamos los comandos: <br>
Switch# configure terminal <br>
Switch(config)#interface gigabitEthernet1/1 <br>
Switch(config‐if)#speed 10 <br>

<img src="https://github.com/Nahuel-Troisi/pni29_nahuel/blob/main/ut005/a3/7.1.1.png"> <br>

Y comprobamos que, ahora, la velocidad de nuestro puerto a cambia a 10 Mbps. <br>
Switch# show interfaces GigabitEthernet1/1 <br>

<img src="https://github.com/Nahuel-Troisi/pni29_nahuel/blob/main/ut005/a3/7.1.2.png"> <br>

Podemos hacer lo mismo colocando la velocidad a 100: <br>
Switch(config)#interface gigabitEthernet1/1 <br>
Switch(config‐if)#speed 100 <br>
O volviendo a colocar la velocidad en automático: <br>
Switch(config)#interface gigabitEthernet1/1 <br>
Switch(config‐if)#speed auto <br><br>


Paso 2. Desactivar un puerto.
Hay momentos en que podremos necesitar el desactivar un puerto, ya sea porque la
tarjeta de red del equipo no funciona correctamente, o por haber detectado que quien
hace uso de ese puerto no está autorizado.
Por este motivo, podemos desactivar un puerto.
Partiendo de la configuración anterior, podemos desactivar cualquier puerto del
switch. Esta acción la conseguimos con los comandos: <br>
Switch>enable  <br>
Switch#configure terminal <br>
Switch(config)#interface gigabitEthernet1/1 <br>
Switch(config‐if)#shutdown <br>
Comprobar el funcionamiento de este comando mediante el añadido de varios equipos 
al switch a diferentes puertos <br><br>

<img src="https://github.com/Nahuel-Troisi/pni29_nahuel/blob/main/ut005/a3/7.2.png"> <br>

<img src="https://github.com/Nahuel-Troisi/pni29_nahuel/blob/main/ut005/a3/7.2.1.png"> <br>


#### ***Conclusiones***. <a name="id5"></a>

Se nota que en nivel de dificultad va en aumento, ya que algunos apartados han llevado más tiempo del esperado, aun con todo, en líneas generales estoy
contento con la práctica. 
