
<center>

# COMANDOS DE RED


</center>

***Nahuel Ivan Troisi*** <br>
***2º de Ciclo Superior de Administración de Sistemas Informáticos en Red*** 

### ÍNDICE

+ [Introducción](#id1)
+ [Objetivos](#id2)
+ [Material empleado](#id3)
+ [Desarrollo](#id4)
+ [Conclusiones](#id5)


#### ***Introducción***. <a name="id1"></a>

Vamos a realizar una serie de comandos de red, tanto en Linux como Windows, donde aprenderemos las diferencias visuales y prácticas entre ambos sistemas operativos y los respectivos comandos necesarios para comunicarnos con el terminal. 

#### ***Objetivos***. <a name="id2"></a>

Aprender a usar los comandos de red correctamente, así como saber cual utilizar en cada situación. 

#### ***Material empleado***. <a name="id3"></a>

MV de Kali Linux y Windows 10, así como sus respectivos terminales. 

#### ***Desarrollo***. <a name="id4"></a>


### __<ins> WINDOWS (IPCONFIG) </ins>__


| Dirección IPV4              	| 192.18.99.66                	|
|-----------------------------	|-----------------------------	|
| Máscara                     	| 255.255.0.0                 	|
| Gateway                     	| 172.18.0.1                  	|
| MAC                         	| 08-00-27-BF-CB-3F           	|
| Fabricante                  	| Intel                       	|
| Dirección IPV6              	| fe80::fd6a:d7b3:2531:401e%5 	|
| Servidores DNS              	| 80.58.61.250                	|
| Tiemo de concesión de la IP 	| 1 día                       	|
| Nombre del adaptador de red 	| PRO/1000 MT                 	|

1. Liberar la configuración IP del adaptador con ipconfig /release y a continuación volver a usar el
comando ipconfig.
¿Cuál es la ip ahora?

~~~ 
Si hacemos uso de este comando estamos provocando la liberación de la IP, por lo que si consultamos de nuevo 
dicha IP, no tendremos respuesta.
~~~

2. Ejecutar el comando ipconfig /renew solicitando una renovación de dirección IP. A continuación
volver a ejecutar ipconfig. ¿Cuál es la nueva ip?

~~~
La IP obtenida es la misma de la que partimos, es decir, 192.168.1.157. 
~~~
3. Ejecutar el comando ipconfig /displaydns y comprobar la información que contiene la caché DNS
de tu equipo. Ejecuta ahora el comando ipconfig /flushdns y después muestra otra vez el
contenido de la caché DNS. ¿Qué información muestra ahora? ¿Qué ha ocurrido?

~~~
No nos muestra ninguna información, ya que hemos vaciado el caché DNS previamente. 
~~~
4. Usar el navegador para ir a la web http://www.iespuertodelacruz.es y luego ejecutar el comando
ipconfig /displaydns. Hacer una captura de pantalla donde se muestre que se ha cacheado la ip de
ese nombre de dominio y pegarla aquí debajo.

![](https://github.com/Nahuel-Troisi/pni29_nahuel/blob/main/ut005/a1/1.png)

5. Borra la caché DNS con el comando ipconfig /flushdns y muestra una captura de pantalla en que
se vea que ya no hay registros DNS en caché.

![](https://github.com/Nahuel-Troisi/pni29_nahuel/blob/main/ut005/a1/2.png)


### __<ins> LINUX (IFCONFIG)</ins>__


| Dirección IPV4              	| 192.18.99.66                	|
|-----------------------------	|-----------------------------	|
| Máscara                     	| 255.255.0.0                 	|
| Gateway                     	| 172.18.0.1                  	|
| MAC                         	| 08-00-27-BF-CB-3F           	|
| Fabricante                  	| Intel                       	|
| Dirección IPV6              	| fe80::fd6a:d7b3:2531:401e%5 	|
| Servidores DNS              	| 80.58.61.250                	|
| Tiemo de concesión de la IP 	| 1 día                       	|
| Nombre del adaptador de red 	| PRO/1000 MT                 	|

1. Desactiva tu tarjeta de red con el comando ifconfig eth0 down. A continuación, comprueba con un
ifconfig que la tarjeta ya no aparece, se ha desactivado. Haz una captura de pantalla donde se vea
que ya no está activada.

![](https://github.com/Nahuel-Troisi/pni29_nahuel/blob/main/ut005/a1/3.png)

2. Usa el comando ifconfig –a para ver que la tarjeta está desactivada, pero nadie la ha robado. Sigue
ahí.
Ahora activa la tarjeta con el comando ifconfig eth0 up y luego con el comando ifconfig
comprueba que ya está habilitada.
Usa el comando ifconfig eth0 192.168.99.99 netmask 255.255.255.0 y pega una captura de
pantalla que muestre que el adaptador de red se ha configurado correctamente.

![](https://github.com/Nahuel-Troisi/pni29_nahuel/blob/main/ut005/a1/4.png)
![](https://github.com/Nahuel-Troisi/pni29_nahuel/blob/main/ut005/a1/5.png)

3. Usa el comando ifconfig eth0 IP netmask Máscara (con la configuración inicial de red) y pega una
captura de pantalla que muestre que el adaptador de red se ha configurado correctamente.

![](https://github.com/Nahuel-Troisi/pni29_nahuel/blob/main/ut005/a1/6.png)
<br>
![](https://github.com/Nahuel-Troisi/pni29_nahuel/blob/main/ut005/a1/7.png)

### __<ins> COMANDO PING </ins>__

1. Ejecuta el comando ping –s 100 –c 2 ip_puertadeenlace para que se
envíen dos ecos de 100 bytes. Muestra una captura de pantalla con el resultado.

![](https://github.com/Nahuel-Troisi/pni29_nahuel/blob/main/ut005/a1/8.png)

2. Usa el comando ping –i 2 ip_puertadeenlace para hacer un ping
a nuestra puerta de enlace con un TTL igual a 2.
Luego haz un ping de las mismas características, pero a google ping –i 2 www.google.es. Pega una
captura de pantalla con el resultado y explica lo que ha pasado.

![](https://github.com/Nahuel-Troisi/pni29_nahuel/blob/main/ut005/a1/9.png)

3. El comando ping nos da información sobre el tiempo de latencia de una red. Haz un ping a nuestra
puerta de enlace y luego a otro a www.google.es. Busca información de lo que es el tiempo de
latencia y compara los tiempos de latencia en ambos casos.

![](https://github.com/Nahuel-Troisi/pni29_nahuel/blob/main/ut005/a1/10.png)

~~~ 
Como podemos comprobar, los tiempos de latencia son menores en el primer caso, ya que estamos transmitiendo datos a 
nuestro própio equipo, mientras que enviar paquetes a un servidor más lejano tomaría más tiempo. 
~~~

### __<ins> COMANDO ROUTE </ins>__

1. Usa el comando route para ver la puerta de enlace de tu equipo. ¿Cuál es tu puerta de enlace?

![](https://github.com/Nahuel-Troisi/pni29_nahuel/blob/main/ut005/a1/11.png)

2. Borra la puerta de enlace usando el comando Route del default gw ip_gateway. A continuación,
ejecuta el comando route para comprobar que ya no hay puerta de enlace. Intenta navegar por
internet y verás que tampoco puedes. Haz una captura de pantalla con la salida del comando
route y del resultado de ping 8.8.8.8 ¿Cómo interpretas el mensaje que te devuelve el ping?

![](https://github.com/Nahuel-Troisi/pni29_nahuel/blob/main/ut005/a1/12.png)

3. Vuelve a configurar la puerta de enlace usando el comando route add default gw ip_gateway y
comprueba que ya ha vuelto la puerta de enlace con el comando route.

![](https://github.com/Nahuel-Troisi/pni29_nahuel/blob/main/ut005/a1/13.png)

### __<ins> COMANDO NETSTAT </ins>__

1. Abre una página web cualquiera y luego ejecuta el comando netstat -t para que nos muestre las
conexiones que tenemos abiertas por tcp. Pon una captura de pantalla del resultado y explica lo
que es cada una de las columnas que aparecen.

2. Ahora espera unos segundos y vuelve a ejecutar netstat -tn. Comprobarás que algunas de las
conexiones se han cerrado o están esperando para cerrarse. Además con la opción -n verás los resultados en formato numérico. Pon una captura de pantalla y explica la diferencia entre Established, Time_wait y Close_Wait.

3. Ejecuta ahora la orden netstat -at para que muestre las tanto las conexiones tcp abiertas como los
puertos que están a la escucha. Copia una captura de pantalla donde se vean los puertos que
tienes escuchando, explica qué significan los asteriscos en la columna “Foreign address” e
investiga si tener esos puertos abiertos es normal o supone una amenaza.

4. Ejecuta el comando netstat -s para ver las estadísticas de red y haz una captura en la que se vean
cuantos paquetes tcp has recibido y cuantos de ellos han sido erroneos.

### __<ins> COMANDO ARP </ins>__

1. Borra toda la caché ARP con el comando arp -d *. A continuación haz un ping a la puerta de
enlace. Pon una captura de la tabla ARP en que se vea que solo está la puerta de enlace y su mac.

2. Ahora borra manualmente la entrada arp de la puerta de enlace con la orden arp -d
ip_puertadeenlace. Luego introduce manualmente una mac falsa para la puerta de enlace en la
tabla arp con el comando arp -s ip_puertadeenlace aa:bb:cc:dd:ee:ff Haz una captura de pantalla
en que se vea el resultado del comando arp -a y de hacer un ping a google. Explica por qué ahora
no hay internet.

3. Borra la entrada falsa de la tabla arp con el comando arp -d ip_puertadeenlace.

### __<ins> COMANDO NSLOOKUP </ins>__

1. Averigua el nombre del servidor DNS de www.iespuertodelacruz.es. A continuación, ejecutamos
el comando nslookup nombreServidorDNS y luego el comando nslookup nombreServidorDNS
8.8.8.8. Explica las causas de las diferencias que hay entre los resultados de las dos consultas.

![](https://github.com/Nahuel-Troisi/pni29_nahuel/blob/main/ut005/a1/14.png)

~~~
La diferencia principal es que en el servidor del instituto, el DNS tiene un nombre totalmente distinto, mientras
que en el del servidor de google, está correctamente identificado el propietario del mismo.
~~~


#### ***Conclusiones***. <a name="id5"></a>

Ha sido una práctica bastante sencilla, aunque un poco extensa a mi parecer. No obstante, sirve para aprender a usar los comandos de red a nivel básico, que es lo que estamos buscando. 
