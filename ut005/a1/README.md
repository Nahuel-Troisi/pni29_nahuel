
<center>

# TÍTULO DE LA PRÁCTICA


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

Aquí explicamos brevemente la parte teórica que tiene que ver con la práctica que se va a realizar

#### ***Objetivos***. <a name="id2"></a>

Aquí explicamos los objetivos que se pretenden alcanzar al realizar la práctica.

#### ***Material empleado***. <a name="id3"></a>

Enumeramos el material empleado tanto hardware como software y las conficuraciones que hacemos (configuraciones de red por ejemplo) 

#### ***Desarrollo***. <a name="id4"></a>



__<ins> WINDOWS </ins>__


| Dirección IPV4              	| 172.18.99.72                	|
|-----------------------------	|-----------------------------	|
| Máscara                     	| 255.255.0.0                 	|
| Gateway                     	| 172.18.0.1                  	|
| MAC                         	| 08-00-27-BF-CB-3F           	|
| Fabricante                  	| Intel                       	|
| Dirección IPV6              	| fe80::fd6a:d7b3:2531:401e%5 	|
| Servidores DNS              	| 80.58.61.250                	|
| Tiemo de concesión de la IP 	| 1 día                       	|
| Nombre del adaptador de red 	| PRO/1000 MT                 	|

1. Liberar la configuración IP del adaptador con ***ipconfig /release*** y a continuación volver a usar el
comando **ipconfig***.
¿Cuál es la ip ahora?

2. Ejecutar el comando ***ipconfig /renew*** solicitando una renovación de dirección IP. A continuación
volver a ejecutar ***ipconfig***. ¿Cuál es la nueva ip?

3. Ejecutar el comando ***ipconfig /displaydns*** y comprobar la información que contiene la caché DNS
de tu equipo. Ejecuta ahora el comando ***ipconfig /flushdns*** y después muestra otra vez el
contenido de la caché DNS. ¿Qué información muestra ahora? ¿Qué ha ocurrido?

4. Usar el navegador para ir a la web ***http://www.iespuertodelacruz.es*** y luego ejecutar el comando
***ipconfig /displaydns***. Hacer una captura de pantalla donde se muestre que se ha cacheado la ip de
ese nombre de dominio y pegarla aquí debajo.

5. Borra la caché DNS con el comando ***ipconfig /flushdns*** y muestra una captura de pantalla en que
se vea que ya no hay registros DNS en caché.


__<ins> LINUX </ins>__

#### ***Conclusiones***. <a name="id5"></a>

En esta parte debemos exponer las conclusiones que sacamos del desarrollo de la prácica.
