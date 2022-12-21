# Redes Virtuales en Azure

En esta práctica vamos a crear una red virtual en Azure y dos máquinas virtuales, un Windows Server 2019 y un Windows 10 Pro, y probaremos y a conectar.

Los pasos para dar respueta a la siguiente necesidad:

![](img/img01.PNG)

## Paso 1

Crearemos nuestro grupo de recursos.

Para ello nos vamos al menú principal de Azure y seleccionaremos grupo de recursos y dentro de este pulsaremos create.

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

Pulsaremos Revisar y Crear.

Una vez pulsado eso nos saldrá la siguiente ventana.

![](img/img09.PNG)

![](img/img10.PNG)

Despues de esto pulsamos create y empezará el proceso.

![](img/img11.PNG)

Una vez acabado el proceso, nos aparecerá en el grupo de recursos.

