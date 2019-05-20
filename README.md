# Windows Server 2016 - Empresa
## Organización de la empresa
La empresa está organizada en tres departamentos los cuales son: Almacén, ventas y marketing. Cada departamento tiene un equipo y dos empleados que solo podrán entrar al equipo que está en su departamento.

En la empresa solo hay una impresora para todos.

Los usuarios solo podrán entrar al sistema de 9:00 a 15:00 de lunes a viernes.

Todo el sistema está en la red 192.168.1.0/24.

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

Ahora lo que tenemos que hacer es configurar los usuario. Para ello pondremos que los usuarios solo puedan entrar al equipo del departamento al que pertenecen.

![accesoUsuarioEquipo.PNG](./accesoUsuarioEquipo.PNG)

Ahora vamos a limitar las horas en las que los usuario pueden iniciar sesión en el sistema.

![horarioUsuario.PNG](./horarioUsuario.PNG)

Por último tenemos que agregar la impresora y para ello tenemos que agregar el rol al servidor.

![impresora(1).PNG](./impresora(1).PNG)

Una vez instalado tenemos que configurarla y añadir la impresora.

![impresora(2).PNG](./impresora(2).PNG)

![impresora(3).PNG](./impresora(3).PNG)

## Instalación de DHCP
Lo siguiente que vamos a hacer es agregar un nuevo rol a nuestro servidor de DHCP. Esto lo hacemos de la misma forma en la que hemos añadido el Active Directory.

![dhcp(1).PNG](./dhcp(1).PNG)

Después de añadirlo necesitamos configurarlo para que de el rango de IPs que nosotros queramos. Para ello lo que tenemos que hacer es agregar un nuevo ámbito.

![dhcp(2).PNG](./dhcp(2).PNG)

Una vez configurado ya está listo para que reparta IPs a los equipos de la red.

## Comprobaciones
### Conexión
Lo que necesitamos hacer es cambiar el nombre del equipo a uno que tengamos en el servidor creado. Una vez tengamos eso tenemos que cambiar el grupo de trabajo por el dominio de nuestro servidor. Una vez hecho eso nos pedirá la contraseña del administrador del sistema del servidor y ya se tendra acceso con los usuarios utilizados después de reiniciar el equipo.

![comprobacionConexion(1).PNG](./comprobacionConexion(1).PNG)

Una vez que hemos establecido la conexión vamos a intentar conectarnos con un usuario fuera de las horas establecidas, para comprobar que no se conecta.

![comprobacionConexion(2).PNG](./comprobacionConexion(2).PNG)

![comprobacionConexion(3).PNG](./comprobacionConexion(3).PNG)

Como vemos en la hora el usuario no va a poder entrar. Ahora vamos a cambiarle el acceso por horario y comprobar que entra.

![comprobacionConexion(4).PNG](./comprobacionConexion(4).PNG)

![comprobacionConexion(5).PNG](./comprobacionConexion(5).PNG)

![comprobacionConexion(6).PNG](./comprobacionConexion(6).PNG)

![comprobacionConexion(7).PNG](./comprobacionConexion(7).PNG)

### DHCP
La comprobación la hacemos desde un cliente en la misma red física y cofigurandolo como dhcp y comprobar que tiene una IP dentro de nuestro rango.

![comprobacionDHCP.PNG](./comprobacionDHCP.PNG)
