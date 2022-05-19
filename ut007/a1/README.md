# CONFIGURACIÓN BÁSICA DE UN ROUTER

***Nahuel Ivan Troisi*** 
<br>
***1º de Ciclo Superior de Administración de Sistemas Informáticos en Red*** 


## 1.Establecer la topología e inicializar los dispositivos
	
a) Configurar los equipos. <br>
	
<img src="https://github.com/Nahuel-Troisi/pni29_nahuel/blob/main/ut007/a1/img/1.1%20(1).png">
<img src="https://github.com/Nahuel-Troisi/pni29_nahuel/blob/main/ut007/a1/img/1.1%20(2).png">

b) Configurar el router. <br>

<img src="https://github.com/Nahuel-Troisi/pni29_nahuel/blob/main/ut007/a1/img/1.1%20(3).png">

c) Configurar el switch. <br>	
	
<img src="https://github.com/Nahuel-Troisi/pni29_nahuel/blob/main/ut007/a1/img/1.1%20(4).png">

## 2.Configurar dispositivos y verificar la conectividad

a) Acceda al router mediante el puerto de consola y habilite el modo EXEC privilegiado. <br>
b) Ingrese al modo de configuración global. <br>
c) Asigne un nombre de dispositivo al router. <br>
d) Deshabilite la búsqueda DNS para evitar que el router intente traducir los comandos incorrectamente
   introducidos como si fueran nombres de host. <br>
e) Establezca el requisito de que todas las contraseñas tengan como mínimo 10 caracteres. <br>
f) Asigne "cisco12345" como la contraseña cifrada del modo EXEC privilegiado. <br>
g) Asigne ciscoconpass como la contraseña de consola, establezca un tiempo de espera, habilite el inicio
   de sesión y agregue el comando "logging synchronous". El comando "logging synchronous" sincroniza
   la depuración y el resultado del software IOS de Cisco, y evita que estos mensajes interrumpan la
   entrada del teclado. <br>
<img src="https://github.com/Nahuel-Troisi/pni29_nahuel/blob/main/ut007/a1/img/2-ag.png">
h) Asigne "ciscovtypass" como la contraseña de vty, establezca un tiempo de espera, habilite el inicio de
   sesión y agregue el comando "logging synchronous". <br>
<img src="https://github.com/Nahuel-Troisi/pni29_nahuel/blob/main/ut007/a1/img/2-h.png">
i) Cifre las contraseñas de texto no cifrado. <br>
j) Cree un aviso que advierta a todo aquel que acceda al dispositivo que el acceso no autorizado está
   prohibido. <br>
<img src="https://github.com/Nahuel-Troisi/pni29_nahuel/blob/main/ut007/a1/img/2-hj.png">
k) Configure una dirección IP y una descripción de interfaz. Active las dos interfaces en el router. <br>
l) Configure el reloj en el router, por ejemplo: <br>
   "R1# clock set 17:00:00 18 Feb 2013". <br>
m) Guarde la configuración en ejecución en el archivo de configuración de inicio.<br>
<img src="https://github.com/Nahuel-Troisi/pni29_nahuel/blob/main/ut007/a1/img/2-km.png">
n) Haga ping a la PC-B en un símbolo del sistema en la PC-A.<br>
<img src="https://github.com/Nahuel-Troisi/pni29_nahuel/blob/main/ut007/a1/img/2.3%20(a).png">
o) Acceda de forma remota al R1 desde la PC-A mediante el cliente de Telnet de Tera Term.
   Abra Tera Term e introduzca la dirección IP de la interfaz G0/1 del R1 en el campo Host: de la ventana
   Tera Term: New Connection (Tera Term: nueva conexión). Asegúrese de que el botón de opción Telnet
   esté seleccionado y después haga clic en OK (Aceptar) para conectarse al router. <br>
<img src="https://github.com/Nahuel-Troisi/pni29_nahuel/blob/main/ut007/a1/img/2.3%20(b).png">
<img src="https://github.com/Nahuel-Troisi/pni29_nahuel/blob/main/ut007/a1/img/2.3%20(b2).png">
p) Habilite las conexiones SSH y cree un usuario en la base de datos local del router. <br>
<img src="https://github.com/Nahuel-Troisi/pni29_nahuel/blob/main/ut007/a1/img/2.4.png">
q) Acceda remotamente al R1 desde la PC-A con el cliente SSH de Tera Term. <br>

## 3.Mostrar la información del router

a) Establecer una sesión SSH para el R1. <br>
b) Recuperar información importante del hardware y el software. <br>
<img src="https://github.com/Nahuel-Troisi/pni29_nahuel/blob/main/ut007/a1/img/3.1%20(1).png">
<img src="https://github.com/Nahuel-Troisi/pni29_nahuel/blob/main/ut007/a1/img/3.1%20(2).png">
<img src="https://github.com/Nahuel-Troisi/pni29_nahuel/blob/main/ut007/a1/img/3.2.png">
c) Mostrar la configuración de inicio. <br>
<img src="https://github.com/Nahuel-Troisi/pni29_nahuel/blob/main/ut007/a1/img/3.3%20(1).png">
<img src="https://github.com/Nahuel-Troisi/pni29_nahuel/blob/main/ut007/a1/img/3.3%20(2).png">
<img src="https://github.com/Nahuel-Troisi/pni29_nahuel/blob/main/ut007/a1/img/3.3%20(3).png">
<img src="https://github.com/Nahuel-Troisi/pni29_nahuel/blob/main/ut007/a1/img/3.3%20(4).png">
d) Mostrar la tabla de routing en el router. <br>
<img src="https://github.com/Nahuel-Troisi/pni29_nahuel/blob/main/ut007/a1/img/3.4.png">
e) Mostrar una lista de resumen de las interfaces del router. <br>
<img src="https://github.com/Nahuel-Troisi/pni29_nahuel/blob/main/ut007/a1/img/3.5.png">		

## 4.Configurar IPv6 y verificar la conectividad

a) Asigne una dirección de unidifusión global IPv6 a la interfaz G0/0; asigne la dirección link-local en la
   interfaz, además de la dirección de unidifusión; y habilite el routing IPv6. <br>
<img src="https://github.com/Nahuel-Troisi/pni29_nahuel/blob/main/ut007/a1/img/4.1%20(a).png">
b) Use el comando show ipv6 int brief para verificar la configuración de IPv6 en el R1.
   Si no se asignó una dirección IPv6 a la G0/1, ¿por qué se indica como [up/up]? <br>
<img src="https://github.com/Nahuel-Troisi/pni29_nahuel/blob/main/ut007/a1/img/4.1%20(b).png">
c) Emita el comando ipconfig en la PC-B para examinar la configuración de IPv6. <br>
   ¿Cuál es la dirección IPv6 asignada a la PC-B? <br>
   ¿Cuál es el gateway predeterminado asignado a la PC-B? <br>
<img src="https://github.com/Nahuel-Troisi/pni29_nahuel/blob/main/ut007/a1/img/4.1%20(c1).png">
   En la PC-B, haga ping a la dirección link-local del gateway predeterminado del R1. ¿Tuvo éxito? <br>
<img src="https://github.com/Nahuel-Troisi/pni29_nahuel/blob/main/ut007/a1/img/4.1%20(c2).png">
   En la PC-B, haga ping a la dirección IPv6 de unidifusión del R1 2001:db8:acad:a::1. ¿Tuvo éxito? <br>
<img src="https://github.com/Nahuel-Troisi/pni29_nahuel/blob/main/ut007/a1/img/4.1%20(c3).png">
d) Durante la investigación de un problema de conectividad de red, un técnico sospecha que no se habilitó una
  interfaz. ¿Qué comando show podría usar el técnico para resolver este problema? <br>
   Durante la investigación de un problema de conectividad de red, un técnico sospecha que se asignó una
   máscara de subred incorrecta a una interfaz. ¿Qué comando show podría usar el técnico para resolver este
   problema? <br>
   Después de configurar IPv6 en la LAN de la PC-B en la interfaz G0/0 del R1, si hiciera ping de la PC-A a la
   dirección IPv6 de la PC-B, ¿el ping sería correcto? ¿Por qué o por qué no? <br>

## 5.Inicialización y recarga de un router y un switch

a) Acceda al router mediante el puerto de consola y habilite el modo EXEC privilegiado. <br>
b) Escriba el comando erase startup-config para eliminar el archivo de configuración de inicio de la
   NVRAM. <br>
c) Emita el comando "reload" para eliminar una configuración antigua de la memoria. Cuando reciba el
   mensaje Proceed with reload (Continuar con la recarga), presione Enter para confirmar. (Si presiona
   cualquier otra tecla, se cancela la recarga). <br>
d) Una vez que se vuelve a cargar el router, se le solicita introducir el diálogo de configuración inicial.<br>
   Escriba "no" y presione "Enter". <br>
e) Se le solicita finalizar la instalación automática. Escriba "yes" (sí) y, luego, presione "Enter". <br>
<img src="https://github.com/Nahuel-Troisi/pni29_nahuel/blob/main/ut007/a1/img/Apendice_1.png">
<img src="https://github.com/Nahuel-Troisi/pni29_nahuel/blob/main/ut007/a1/img/Apendice_1.1.png">
<img src="https://github.com/Nahuel-Troisi/pni29_nahuel/blob/main/ut007/a1/img/Apendice_1.2.png">
f) Acceda al switch mediante el puerto de consola e ingrese al modo EXEC privilegiado. <br>
g) Utilice el comando show flash para determinar si se crearon VLAN en el switch. <br>
h) Si se encontró el archivo vlan.dat en la memoria flash, elimínelo. <br>
i) Utilice el comando "erase startup-config" para eliminar el archivo de configuración de inicio de la
   NVRAM. Se le solicitará que confirme la eliminación del archivo de configuración. Presione Enter para
   confirmar que desea borrar este archivo. (Al pulsar cualquier otra tecla, se cancela la operación). <br> 
j) Vuelva a cargar el switch para eliminar toda información de configuración antigua de la memoria. Se le
   solicitará que confirme la recarga del switch. Presione Enter para seguir con la recarga. (Si presiona
   cualquier otra tecla, se cancela la recarga). <br>
k) Una vez que se vuelve a cargar el switch, se le solicita introducir el diálogo de configuración inicial.
   Escriba "no" y presione "Enter". <br>
<img src="https://github.com/Nahuel-Troisi/pni29_nahuel/blob/main/ut007/a1/img/Apendice_2.png">
<img src="https://github.com/Nahuel-Troisi/pni29_nahuel/blob/main/ut007/a1/img/Apendice_2.1.png">
<img src="https://github.com/Nahuel-Troisi/pni29_nahuel/blob/main/ut007/a1/img/Apendice_2.2.png">
<img src="https://github.com/Nahuel-Troisi/pni29_nahuel/blob/main/ut007/a1/img/Apendice_2.3.png">
<img src="https://github.com/Nahuel-Troisi/pni29_nahuel/blob/main/ut007/a1/img/Apendice_2.4.png">
<img src="https://github.com/Nahuel-Troisi/pni29_nahuel/blob/main/ut007/a1/img/Apendice_2.5.png">
	




