# EJERCICIO-1

<center>

![](img/ejercicio1.png)

</center>

1. Cambia el nombre del switch a **S1**.

~~~
Switch>enable
Switch#configure terminal 
Switch(config)#hostname S1
S1(config)#
~~~

2. Creamos las VLAN y le asignamos un nombre a cada siguiendo el criterio:

+ vlan 10 -> **proyecto10**

~~~
S1(config)#vlan 10
S1(config-vlan)#name proyecto10
S1(config-vlan)#exit
~~~

+ vlan 20 -> **proyecto20**

~~~
S1(config)#vlan 20
S1(config-vlan)#name proyecto20
S1(config-vlan)#exit
~~~

+ vlan 30 -> **proyecto30**

~~~
S1(config)#vlan 30
S1(config-vlan)#name proyecto30
S1(config-vlan)#exit
~~~

+ Muestra las redes VLAN 
~~~
S1#show vlan brief

VLAN Name                             Status    Ports
---- -------------------------------- --------- -------------------------------
1    default                          active    Fa0/1, Fa0/2, Fa0/3, Fa0/4
                                                Fa0/5, Fa0/6, Fa0/7, Fa0/8
                                                Fa0/9, Fa0/10, Fa0/11, Fa0/12
                                                Fa0/13, Fa0/14, Fa0/15, Fa0/16
                                                Fa0/17, Fa0/18, Fa0/19, Fa0/20
                                                Fa0/21, Fa0/22, Fa0/23, Fa0/24
                                                Gig0/1, Gig0/2
10   proyecto10                       active    
20   proyecto20                       active    
30   proyecto30                       active    
1002 fddi-default                     active    
1003 token-ring-default               active    
1004 fddinet-default                  active    
1005 trnet-default                    active    
S1#
~~~

3. Asignamos las máquinas a cada una de las vlan creadas siguiendo el criterio siguiente:

+ PC1, PC5 y PC8 forman el equipo de trabajo para el desarrollo del **proyecto10**

#### PC1
~~~
S1#enable
S1#configure terminal 
S1(config)#interface Fa0/1
S1(config-if)#switchport mode access 
S1(config-if)#switchport access vlan 10
~~~

#### PC5
~~~
S1#enable
S1#configure terminal
S1(config)#interface Fa0/5
S1(config-if)#switchport mode access
S1(config-if)#switchport access vlan 10
~~~

#### PC8
~~~
S1#enable
S1#configure terminal
S1(config)#interface Fa0/8
S1(config-if)#switchport mode access
S1(config-if)#switchport access vlan 10
~~~
+ PC2 y PC6 forman el grupo de trabajo para el desarrollo del **proyecto20**

#### PC2
~~~
S1#enable
S1#configure terminal
S1(config)#interface Fa0/2
S1(config-if)#switchport mode access
S1(config-if)#switchport access vlan 20
~~~

#### PC6
~~~
S1#enable
S1#configure terminal
S1(config)#interface Fa0/6
S1(config-if)#switchport mode access
S1(config-if)#switchport access vlan 20
~~~
+ PC3, PC4 y PC7 forman el grupo de trabajo para el desarrollo del **proyecto30**

#### PC3
~~~
S1#enable
S1#configure terminal
S1(config)#interface Fa0/3
S1(config-if)#switchport mode access
S1(config-if)#switchport access vlan 30
~~~

#### PC4
~~~
S1#enable
S1#configure terminal
S1(config)#interface Fa0/4
S1(config-if)#switchport mode access
S1(config-if)#switchport access vlan 30
~~~

#### PC7
~~~
S1#enable
S1#configure terminal
S1(config)#interface Fa0/7
S1(config-if)#switchport mode access
S1(config-if)#switchport access vlan 30
~~~
4. Mostramos un resumen de las redes vlan creadas:

~~~
S1#show vlan brief

VLAN Name                             Status    Ports
---- -------------------------------- --------- -------------------------------
1    default                          active    Fa0/9, Fa0/10, Fa0/11, Fa0/12
                                                Fa0/13, Fa0/14, Fa0/15, Fa0/16
                                                Fa0/17, Fa0/18, Fa0/19, Fa0/20
                                                Fa0/21, Fa0/22, Fa0/23, Fa0/24
                                                Gig0/1, Gig0/2
10   proyecto10                       active    Fa0/1, Fa0/5, Fa0/8
20   proyecto20                       active    Fa0/2, Fa0/6
30   proyecto30                       active    Fa0/3, Fa0/4, Fa0/7
1002 fddi-default                     active    
1003 token-ring-default               active    
1004 fddinet-default                  active    
1005 trnet-default                    active    
S1#
~~~


5.Guardamos la configuración del switch

~~~
S1#copy running-config startup-config 
Destination filename [startup-config]? 
Building configuration...
[OK]
S1#
~~~



6. Configuramos las direcciones `ip`de cada uno de los equipos siguiendo el siguiente criterio:

+ Vlan 10 -> proyecto10 -> 10.0.10.0/24
+ Vlan 20 -> proyecto20 -> 10.0.20.0/24
+ Vlan 30 -> proyecto30 -> 10.0.30.0/24

Una vez hecho esto comprobar que sólo hay comunicación entre los distintos equipos que forman parte de la misma red vlan.



# EJERCICIO-2

Partiendo del ejercicio de un switch ya resuelto, añadir un switch S2 conectado a S1. Este switch tendrá:

+ En el puerto 9 el equipo PC9 del **proyecto10**.
+ En el puerto 10 el equipo PC10 del **proyecto20**.
+ En el puerto 11 el equipo PC11 del **proyecto30**.
+ El troncal estará en el primer puerto gigabitethernet de los dos switches

>***NOTA-1***: Conectamos los equipos al switch y les asignamos a cada uno de ellos las "ip" correspondientes **PERO NO CONFIGURAMOS NINGUNA VLAN EN EL SEGUNDO SWTICH**, ya que vamos a hacer uso del protocolo **VTP** para que el primer switch se comporte como **servidor** y el segundo como **cliente**

>***NOTA-2***: No conectar los dos switches entre sí hasta no configurar el **VTP**


<center>

![](img/ejercicio2.png)

</center>


1. Configura el switch S1 como **servidor** dentro del protocolo **VTP**

~~~
S1>enable
S1#configure terminal 
S1(config)#vtp domain prueba_nahuel
S1(config)#vtp password 1234
S1(config)#vtp mode server 
~~~

2. Muestra el estado del protocolo **VTP** en el switch S1

~~~
S1#show vtp status
VTP Version                     : 2
Configuration Revision          : 0
Maximum VLANs supported locally : 255
Number of existing VLANs        : 8
VTP Operating Mode              : Server
VTP Domain Name                 : prueba_nahuel
VTP Pruning Mode                : Disabled
VTP V2 Mode                     : Disabled
VTP Traps Generation            : Disabled
MD5 digest                      : 0x24 0x25 0x7D 0x29 0xAD 0xFB 0x35 0xA6 
Configuration last modified by 0.0.0.0 at 3-1-93 00:11:57
Local updater ID is 0.0.0.0 (no valid interface found)
S1#
~~~

3. Conficura el puerto `Gig0/1` en modo **troncal**

~~~
S1#enable
S1#configure terminal 
S1(config)#interface Gig0/1
S1(config-if)#switchport mode trunk 
~~~

4. Configura el switch S2 como **cliente** dentro del protocolo **VTP**

~~~
S2#enable
S2#configure terminal
S2(config)#vtp domain prueba_nahuel 
S2(config)#vtp password 1234
S2(config)#vtp mode client
S2(config)#
~~~

5. Muestra el estado del protocolo **VTP** en el switch S2

~~~
S2#show vtp status
VTP Version                     : 2
Configuration Revision          : 0
Maximum VLANs supported locally : 255
Number of existing VLANs        : 5
VTP Operating Mode              : Client
VTP Domain Name                 : prueba_nahuel
VTP Pruning Mode                : Disabled
VTP V2 Mode                     : Disabled
VTP Traps Generation            : Disabled
MD5 digest                      : 0x37 0xDA 0x64 0x83 0xFB 0x44 0x09 0x0E 
Configuration last modified by 0.0.0.0 at 0-0-00 00:00:00
S2#
~~~


6. Configura el puerto `Gig0/1`del switch S2 en modo **troncal**

~~~
S2#enable
S2#configure terminal
S2(config)#interface Gig0/1
S2(config-if)#switchport mode trunk
~~~

7. Muestra un resumen de las redes vlan del switch S2 (no debe haber ninguna vlan salvo la que se crea por defecto)

~~~
S2#show vlan  brief

VLAN Name                             Status    Ports
---- -------------------------------- --------- -------------------------------
1    default                          active    Fa0/1, Fa0/2, Fa0/3, Fa0/4
                                                Fa0/5, Fa0/6, Fa0/7, Fa0/8
                                                Fa0/9, Fa0/10, Fa0/11, Fa0/12
                                                Fa0/13, Fa0/14, Fa0/15, Fa0/16
                                                Fa0/17, Fa0/18, Fa0/19, Fa0/20
                                                Fa0/21, Fa0/22, Fa0/23, Fa0/24
                                                Gig0/1, Gig0/2
1002 fddi-default                     active    
1003 token-ring-default               active    
1004 fddinet-default                  active    
1005 trnet-default                    active    
S2#
~~~

8.Conecta los puertos `Gig0/1` de ambos switches.

9. Muestra un resumen de las redes vlan del switch S2. ¿Qué diferencia hay ?

~~~
S2#show vlan  brief

VLAN Name                             Status    Ports
---- -------------------------------- --------- -------------------------------
1    default                          active    Fa0/1, Fa0/2, Fa0/3, Fa0/4
                                                Fa0/5, Fa0/6, Fa0/7, Fa0/8
                                                Fa0/9, Fa0/10, Fa0/11, Fa0/12
                                                Fa0/13, Fa0/14, Fa0/15, Fa0/16
                                                Fa0/17, Fa0/18, Fa0/19, Fa0/20
                                                Fa0/21, Fa0/22, Fa0/23, Fa0/24
                                                Gig0/2
10   proyecto10                       active    
20   proyecto20                       active    
30   proyecto30                       active    
1002 fddi-default                     active    
1003 token-ring-default               active    
1004 fddinet-default                  active    
1005 trnet-default                    active    
S2#
~~~

~~~
La diferencia del S2 respecto al S1 es que no hemos tenido que configurar previamente las VLAN ya que se han 
transferido de un switch a otro mediante el protocolo VTP. 
~~~

10. Configurar las interfaces del switch S2 en cada vlan:
+ En el puerto 9 el equipo PC9 del **proyecto10**.
+ En el puerto 10 el equipo PC10 del **proyecto20**.
+ En el puerto 11 el equipo PC11 del **proyecto30**.

~~~
S2#enable
S2#configure terminal
S2(config)#interface Fa0/9
S2(config-if)#switchport mode access
S2(config-if)#switchport access vlan 10
~~~
~~~
S2#enable
S2#configure terminal
S2(config)#interface Fa0/10
S2(config-if)#switchport mode access
S2(config-if)#switchport access vlan 20
~~~
~~~
S2#enable
S2#configure terminal
S2(config)#interface Fa0/11
S2(config-if)#switchport mode access
S2(config-if)#switchport access vlan 30
~~~

11. Mostramos un resumen de las vlan del switch S2: 

~~~
S2#show vlan brief

VLAN Name                             Status    Ports
---- -------------------------------- --------- -------------------------------
1    default                          active    Fa0/1, Fa0/2, Fa0/3, Fa0/4
                                                Fa0/5, Fa0/6, Fa0/7, Fa0/8
                                                Fa0/12, Fa0/13, Fa0/14, Fa0/15
                                                Fa0/16, Fa0/17, Fa0/18, Fa0/19
                                                Fa0/20, Fa0/21, Fa0/22, Fa0/23
                                                Fa0/24, Gig0/2
10   proyecto10                       active    Fa0/9
20   proyecto20                       active    Fa0/10
30   proyecto30                       active    Fa0/11
1002 fddi-default                     active    
1003 token-ring-default               active    
1004 fddinet-default                  active    
1005 trnet-default                    active    
S2#
~~~

# EJERCICIO-3

<center>

![](img/ejercicio3.png)

</center>

Conectar un **router 1841** al switch 2 por el puerto `Fa0/1` del router.

1. Configuramos  el router para hacer enrutamiento entre VLANs (Router On A Stick). Para ello creamos sub-interfaces para cada vlan en el puerto `Fa0/1` del router:

+ Configuramos la interfaz `fa0/1` eliminando el direccionamiento:

~~~
Router#enable
Router#configure terminal 
Router(config)#interface Fa0/1
Router(config-if)#no shutdown 
Router(config-if)#no ip address 
~~~ 

+ Sub-interfaz para la vlan 10

~~~
Router#enable
Router#configure terminal 
Router(config)#interface Fa0/1.10
Router(config-subif)#encapsulation dot1Q 10
Router(config-subif)#ip address 10.0.10.100 255.255.255.0 
~~~

+ Sub-interfaz para la vlan 20

~~~
Router#enable
Router#configure terminal
Router(config)#interface Fa0/1.20
Router(config-subif)#encapsulation dot1Q 20
Router(config-subif)#ip address 10.0.20.100 255.255.255.0
~~~

+ Sub-interfaz para la vlan 30

~~~
Router#enable
Router#configure terminal
Router(config)#interface Fa0/1.30
Router(config-subif)#encapsulation dot1Q 30
Router(config-subif)#ip address 10.0.30.100 255.255.255.0
~~~

2. Configuramos la interfaz `Fa0/0` con un servidor para hacer pruebas de conectividad. Utiliza las `ips` de la red `192.168.1.0/2` para esta nueva red.

~~~
Router#enable
Router#configure terminal
Router(config)#interface Fa0/0
Router(config-if)#ip address 192.168.1.1 255.255.255.0 
Router(config-if)#no shutdown
~~~

3. Muestra la tabla de enrutamiento del router.

~~~
Router#show ip route
Codes: C - connected, S - static, I - IGRP, R - RIP, M - mobile, B - BGP
       D - EIGRP, EX - EIGRP external, O - OSPF, IA - OSPF inter area
       N1 - OSPF NSSA external type 1, N2 - OSPF NSSA external type 2
       E1 - OSPF external type 1, E2 - OSPF external type 2, E - EGP
       i - IS-IS, L1 - IS-IS level-1, L2 - IS-IS level-2, ia - IS-IS inter area
       * - candidate default, U - per-user static route, o - ODR
       P - periodic downloaded static route

Gateway of last resort is not set

     10.0.0.0/24 is subnetted, 3 subnets
C       10.0.10.0 is directly connected, FastEthernet0/1.10
C       10.0.20.0 is directly connected, FastEthernet0/1.20
C       10.0.30.0 is directly connected, FastEthernet0/1.30
C    192.168.1.0/24 is directly connected, FastEthernet0/0

Router#
~~~

4. Guarda la configuración del router.

~~~
Router>enable
Router#copy running-config startup-config 
Destination filename [startup-config]? 
Building configuration...
[OK]
Router#
~~~

