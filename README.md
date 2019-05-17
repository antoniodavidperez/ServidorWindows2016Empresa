# Windows Server 2016 - Empresa
## Cambio de la IP y nombre del servidor
Antes de hacer nada en el servidor tenemos que hacer unas configuraciones básicas. Lo primero que haremos es cambiar el nombre del equipo a uno distintivo. También hay que cambiar la IP del servidor a una estática para que el servidor siempre esté accesible y no haya problemas de acceso desde los clientes.
![cambioIPServer.PNG](./cambioIPServer.PNG)

## Instalación de Active Directory
Para que nuestro equipo empiece a funcionar como servidor necesitamos un servicio. Los servicioes se agregan desde el enlace de roles. Desde ahí siguiendo los pasos instalaremos el rol de Active Directory.
![instalacionActiveDirectory(1).PNG](./instalacionActiveDirectory(1).PNG)
Una vez lo tenemos seleccionado solo tenemos que darle a siguiente hasta que nos de la opción de instalar.
![instalacionActiveDirectory(2).PNG](./instalacionActiveDirectory(2).PNG)
![instalacionActiveDirectory(3).PNG](./instalacionActiveDirectory(3).PNG)
Una vez se haya instalado nos aparecerá un mensaje en el que nos dirá que el rol ya ha sido instalado, pero eso no es todo, Ahora tendremos que configurarlo promoviendolo como controlador de dominio.
Lo primero que tenemos que configurar es la implementación que en nuestro caso escogeremos un nuebo bosque y además le daremos un nuevo nombre de dominio a nuestro servidor.
![instalacionActiveDirectory(4).PNG](./instalacionActiveDirectory(4).PNG)
En las siguientes ventanas solo tendremos que elegir contraseña y comenzará la instalación.
![instalacionActiveDirectory(5).PNG](./instalacionActiveDirectory(5).PNG)
![instalacionActiveDirectory(6).PNG](./instalacionActiveDirectory(6).PNG)

## Creación de la unidad organizativa de la empresa
Nuestra empresa tiene tres departamentos en los que hay un equipo y dos empleados en cada uno. Lo primero que tenemos que hacer es crear la unidad organizativa, para ello hacemos clic en herramientas y nos vamos a la gestión de Active Directory. Desde hay hacemos clic derecho sobre servidor(local) y seleccionamos crear una nueva unidad organizativa a la que le daremos el nombre deseado.
![unidadOrganizaiva(1).PNG](./unidadOrganizaiva(1).PNG)
Una vez la tenemos creada accedemos a ella con un doble clic y dentro de ella creamos carpetas para organizar los departamentos. Creamos una carpeta para Marketing, Almacen y Ventas. Dentro de esas carpetas meteremos los usuarios de cada departamento y su correspondiente equipo.
![unidadOrganizaiva(2).PNG](./unidadOrganizaiva(2).PNG)
![unidadOrganizaiva(3).PNG](./unidadOrganizaiva(3).PNG)
![unidadOrganizaiva(4).PNG](./unidadOrganizaiva(4).PNG)
![unidadOrganizaiva(5).PNG](./unidadOrganizaiva(5).PNG)
![unidadOrganizaiva(6).PNG](./unidadOrganizaiva(6).PNG)
![unidadOrganizaiva(7).PNG](./unidadOrganizaiva(7).PNG)

