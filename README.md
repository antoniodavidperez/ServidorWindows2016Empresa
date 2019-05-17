# Windows Server 2016
## Instalación de Active Directory
Los primero que tenemos que hacer es instalar el rol de Active Directory a nuestro servidor.
![named.conf.local.PNG](./named.conf.local.PNG)

Configurar los servidores DNS a los que va a acudir nuestro servidor en el caso de que nos conozca la IP del nombre por el que le están preguntando.
![named.conf.options.PNG](./named.conf.options.PNG)

Crear las zonas directas de cada sitio donde se relacionan las IP con los nombres.
![rd.gato.com.PNG](./rd.gato.com.PNG)
![rd.mosquito.com.PNG](./rd.mosquito.com.PNG)
![rd.escherichiacoli.es.PNG](./rd.escherichiacoli.es.PNG)
![rd.chip555.org.PNG](./rd.chip555.org.PNG)

Crear la zona inversa donde se relacionan los nombres con las IP.
![ri.10.PNG](./ri.10.PNG)

## Creación del servidor Apache
Crear los host virtuales, para ello hay que crear primero la estructura de carpetas y luego configurar los archivos.
![gato.com.conf.PNG](./gato.com.conf.PNG)
![mosquito.com.conf.PNG](./mosquito.com.conf.PNG)

Los dos sitios que vemos a continuación además de la configuración tienen también la de los usuarios. Para ello primero hay que crear un directorio y un archivo donde añadimos los usuarios del sitio.
![escherichiacoli.es-passwords.PNG](./escherichiacoli.es-passwords.PNG)
![escherichiacoli.es.conf.PNG](./escherichiacoli.es.conf.PNG)
![chip555.org-passwords.PNG](./chip555.org-passwords.PNG)
![chip555.org.conf.PNG](./chip555.org.conf.PNG)

## Comprobación desde el lado del cliente
Comprobación de los host por el terminar de un cliente.
![comprobacionHost.PNG](./comprobacionHost.PNG)

Comprobación de los host en el navegador del cliente.
![navegadorGato.PNG](./navegadorGato.PNG)
![navegadorMosquito.PNG](./navegadorMosquito.PNG)
![navegadorEscherichiacoli1.PNG](./navegadorEscherichiacoli1.PNG)
![navegadorEscherichiacoli2.PNG](./navegadorEscherichiacoli2.PNG)
![navegadorChip5551.PNG](./navegadorChip5551.PNG)
![navegadorChip5552.PNG](./navegadorChip5552.PNG)
