# Redes Virtuales en Azure

En esta práctica vamos a crear una red virtual en Azure y dos máquinas virtuales, un Windows Server 2019 y un Windows 10 Pro, y probaremos y a conectar.

Los pasos para dar respueta a la siguiente necesidad:

![](img/img01.PNG)

## Paso 1

Crearemos nuestro grupo de recursos.

Para ello nos vamos al menú principal de Azure y seleccionaremos grupo de recursos y dentro de este pulsaremos create.

<img src="img/img17.PNG" style="zoom:200%;" />

![](img/img02.PNG)

Le daremos el nombre de RG-vnet3.

![](img/img12.PNG)



## Paso 2

Crearemos una máquina virtual con Windows Server 2019, dentro del grupo de recursos pulsaremos el boton create, y seleccionamos windows Server 2019 Datacenter y empezaremos la creación.

![](img/img03.PNG)

![](img/img04.PNG)

Lo primero seria elegir, la suscripción despues el nombre de la máquina en este caso vm19, la arquitectura x64.

El nombre de usuario en este caso azureuser y muy importante abrir los puertos HTTP y RDP.

Los discos los dejamos por defecto.

![](img/img05.PNG)



Ahora configuraremos la Red Virtual.

![](img/img06.PNG)

En este paso daremos en crear nueva, para crear una nueva Red Virtual.

![](img/img07.PNG)

Elegimos el nombre Vnet03, elegimos el rango de la red 10.0.0.0/20 y creamos la subred subnet 01, con el rango 10.0.0.0/24.

Pasaremos a la creacion de la IP Pública, en la pestaña de Networking, en el apartado de IP Pública seleccionaremos crear nueva.

![](img/img08.PNG)

Le pondremos el nombre ws2019ip, SKU en standard, Asignamiento Estático y ruta de preferencia Microsoft Network.

En la pestaña Tags asignaremos esta máquina al departamento de Marketing.

![](img/img22.PNG)

Pulsaremos Revisar y Crear.

Una vez pulsado eso nos saldrá la siguiente ventana.

![](img/img09.PNG)

![](img/img10.PNG)

Despues de esto pulsamos create y empezará el proceso.

![](img/img11.PNG)

Una vez acabado el proceso, nos aparecerá en el grupo de recursos.

## Paso3

Crearemos una Máquina Virtual con el SO Windows 10 Pro.

En el Grupo de Recursos pulsaremos el boton Create.

![](img/img18.PNG)

Seleccionamos Windows 10 y pulsamos el create, nos aparecerá la siguiente ventana.

![](img/img19.PNG)

Como en el anterior estbleceremos el nombre, la arquitectura y lo meteremos en el grupo de recursos previamente creado.

![](img/img20.PNG)

Creamos el usuario, y abrimos el puerto RDP, Ahora vamos a configurar la pestaña de Networking.

![](img/img21.PNG)

Configuraremos esta máquina para que este en la red virtual creada previamente, y en la misma subnet. Otra vez comprobaremos que el puerto RDP esta abierto.

Ahora configuraremos la IP Pública, crearemos una nueva IP Pública.

![](img/img13.PNG)

En la pestaña tags, también asignaremos esta máquina al departameto de Márketing.

![](img/img22.PNG)

Presionaremos Revisar+Crear y empezará el proceso de creación de la máquina una vez acabe aparecerá en el grupo de Recursos.

