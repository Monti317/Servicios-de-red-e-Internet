# Práctica 1- Servidor alojamiento web

## Creación de la VPC
<br>
Lo primero que vamos a hacer es entrar al laboratorio AWS
<br>

![Texto alternativo](imagenes/Screenshot_1.png)
<br>
Una vez dentro de AWS nos iremos al buscador y buscaremos el servicio "VPC"
<br>

![Texto alternativo](imagenes/Screenshot_2.png)
<br>
Ya dentro del servicio VPC lo crearemos
<br>
![Texto alternativo](imagenes/Screenshot_3.png)
<br>
Ya creado empezaremos a con su configuración
<br>
![Texto alternativo](imagenes/Screenshot_4.png)
<br>
Configuraremos las ips para que tengamos 2 subredes públicas y 2 privadas
<br>
![Texto alternativo](imagenes/Screenshot_5.png)
<br>
El resto lo dejaremos por defecto y crearemos la VPC
<br>
![Texto alternativo](imagenes/Screenshot_6.png)
<br>
Y como podemos ver ya se empezaría a crear el VPC
<br>
![Texto alternativo](imagenes/Screenshot_7.png)
<br>
Ya la tenemos creada:
<br>
![Texto alternativo](imagenes/Screenshot_8.png)
<br>
## Creamos la instancia con EC2 
<br>
Lo primero que vamos a hacer es buscar en los servicios EC2
<br>

![Texto alternativo](imagenes/Screenshot_9.png)
<br>
Una vez ya dentro de EC2 lanzaremos la instancia
<br>
![Texto alternativo](imagenes/Screenshot_10.png)
<br>
Empezaremos configurando el sistema operativo
<br>

![Texto alternativo](imagenes/Screenshot_11.png)
<br>
Tambíen seleccionaremos el tipo de instancia y el par de claves
<br>
![Texto alternativo](imagenes/Screenshot_13.png)
<br> 
La configuración de red
<br>
![Texto alternativo](imagenes/Screenshot_12.png)
<br>
Y por último configuraremos el firewall con las reglas de entrada tanto ssh como http
<br>
![Texto alternativo](imagenes/Screenshot_14.png)
<br>
Ya todo configurado lanzaremos la instancia
<br>
![Texto alternativo](imagenes/Screenshot_15.png)
<br>
Como podemos ver el lanzamiento no tuvo ningun fallo
<br>
![Texto alternativo](imagenes/Screenshot_16.png)
<br>
Y ya tendremos nuestra instancia creada
<br>
![Texto alternativo](imagenes/Screenshot_17.png)
<br>
## Instalación de Apache
<br>
Antes de instalar apache o php deberemos actualizar nuestra maquina con los comandos:
<br>

![Texto alternativo](imagenes/Screenshot_18.png)
<br>
![Texto alternativo](imagenes/Screenshot_19.png)
<br>
Una vez ya hemos actualizado nuestra máquina deberemos instalar apache2 con el comando:
<br>
![Texto alternativo](imagenes/Screenshot_20.png)
<br>
Ya instalado vamos a iniciarlo y lo activaremos
<br>
![Texto alternativo](imagenes/Screenshot_21.png)
<br>
![Texto alternativo](imagenes/Screenshot_22.png)
<br>
Para comprobar que funciona correctamente deberemos copiar la ip publica de nuestra máquina, la cual nos aparecerá debajo de la consola
<br>
![Texto alternativo](imagenes/Screenshot_23.png)
<br> 
Y la pegaremos en el navegador y nos deberería salir la página de apache
<br>
![Texto alternativo](imagenes/Screenshot_24.png)
<br>
Ya instalado apache2, vamos a comenzar con la instalación de PHP
<br>
## Instalación de PHP
<br>
Lo primero que vamos a hacer es añadir un repositorio a nuestra máquina con el comando:
<br>

![Texto alternativo](imagenes/Screenshot_25.png)
<br>
Ya añadido el repositorio instalaremos PHP
<br>
![Texto alternativo](imagenes/Screenshot_26.png)
<br>
E instalaremos Mysql
<br>
![Texto alternativo](imagenes/Screenshot_27.png)
<br>
Ya instalados vamos a reiniciar apache2
<br>
![Texto alternativo](imagenes/Screenshot_28.png)
<br>
Para comprobar que se ha instalado correctamente verificaremos la versión de PHP con el comando:
<br>
![Texto alternativo](imagenes/Screenshot_29.png)
<br>
Como podemos ver nos da la versión lo que significa que lo tenemos instalado correctamente.
<br>
## Creamos la base de datos
<br>
Como ya hemos hecho previamente con los demás servicios, buscaremos el servicio RDS en el buscador de AWS
<br>

![Texto alternativo](imagenes/Screenshot_30.png)
<br>
Una vez dentro de RDS podremos ver la opción de "Crear Base de datos"
<br>
![Texto alternativo](imagenes/Screenshot_31.png)
<br>
Empezaremos con la configuración de la base de datos eligiendo el motor MYSQL
<br>
![Texto alternativo](imagenes/Screenshot_32.png)
<br>
Deberemos elegir en el apartado de "Plantillas" la capa gratuita
<br>
![Texto alternativo](imagenes/Screenshot_33.png)
<br>
Nos pedirá que le asignemos un nombre y un usuario y contraseña con el que acceder a la base de datos en mi caso "admin" "12345678"
<br>
![Texto alternativo](imagenes/Screenshot_34.png)
<br>
Dejaremos la siguiente configuración por defecto
<br>
![Texto alternativo](imagenes/Screenshot_35.png)
<br>
En el apartado de conectividad tendremos que asignar la VPC que creamos anteriormente
<br>
![Texto alternativo](imagenes/Screenshot_36.png)
<br>
En el apartado de seguridad del VPC le asignaremos un nombre, en mi caso "SeguridadDB"
<br>
![Texto alternativo](imagenes/Screenshot_37.png)
<br>
El apartado "Supervisión" lo dejaremos por defecto
<br>
![Texto alternativo](imagenes/Screenshot_38.png)
<br>
Lo único que nos queda es asignarle un nombre a nuestra base de datos
<br>
![Texto alternativo](imagenes/Screenshot_39.png)
<br>
Y crearemos la base de datos
<br>
Como podemos ver la base de datos ya esta creada
<br>
![Texto alternativo](imagenes/Screenshot_40.png)
<br>
Una vez creada tendremos que configurarla en un EC2, para esto tendremos que irnos a nuestra base de datos y entrar en el apartado "Acciones"
<br>
![Texto alternativo](imagenes/Screenshot_41.png)
<br>
Seleccionamos la EC2 que creamos anteriormente y continuamos
<br>
![Texto alternativo](imagenes/Screenshot_42.png)
<br>
Nos pondrán los cambios que se han llevado a cabo, le damos a "Configurar"
<br>
![Texto alternativo](imagenes/Screenshot_43.png)
<br>
Y como podemos ver nos pone que la conexión se ha establecido con exito
<br>
![Texto alternativo](imagenes/Screenshot_44.png)
<br>
## Creación del EFS
<br>
Para crear el sistema de ficheros vamos a hacer como con los servicios anteriores, buscaremos el servicio EFS en el buscador de AWS
<br>

![Texto alternativo](imagenes/Screenshot_45.png)
<br>
Una vez dentro seleccionaremos el apartado "Crear un sistema de archivos"
<br>
![Texto alternativo](imagenes/Screenshot_46.png)
<br>
Para crear el sistema de archivos, le daremos un nombre y le asignaremos la VPC que creamos anteriormente.
<br>
![Texto alternativo](imagenes/Screenshot_47.png)
<br>
Como podemos ver se ha creado correctamente
<br>
![Texto alternativo](imagenes/Screenshot_48.png)
<br>
Una vez creado nos tendremos que ir a la configuración de la VPC en mi caso "wordpress" para añadir una regla de entrada
<br>
Seleccionamos el VPC al que le queremos añadir la regla
<br>
![Texto alternativo](imagenes/Screenshot_49.png)
<br>
Nos vamos al apartado "Reglas de entrada" y le damos a "Editar reglas de entrada"
<br>
![Texto alternativo](imagenes/Screenshot_50.png)
<br>
Estableceremos una regla para el protocolo NFS que solo se pueda conectar a través de nuestra VPC
<br>
![Texto alternativo](imagenes/Screenshot_51.png)
<br>
Ahora nos vamos a EFS, al apartado de "Red"
<br>
![Texto alternativo](imagenes/Screenshot_53.png)
<br>
Y cambiamos la VPC que viene por defecto, por la que creamos nosotros
<br>
![Texto alternativo](imagenes/Screenshot_52.png)
<br>
Una vez hecho los cambios, tendremos que asociarla con la máquina donde va a estar wordpress
<br>
![Texto alternativo](imagenes/Screenshot_54.png)
<br>
La asociaremos mediante ip, nos dará un codigo el cuál deberemos introducir en la máquina para asociarla
<br>
![Texto alternativo](imagenes/Screenshot_55.png)
<br>
Pero antes de introducir ese comando deberemos instalar en nuestra máquina "NFS" con el comando:
<br>
![Texto alternativo](imagenes/Screenshot_56.png)
<br>
Ya instalado deberemos ejecutar el comando que nos daba EFS
<br>
![Texto alternativo](imagenes/Screenshot_57.png)
<br>
Y como podemos ver ya tenemos el directorio "EFS"
<br>
![Texto alternativo](imagenes/Screenshot_58.png)
<br>

## Instalación de Wordpress
<br>
Empezaremos descargando Wordpress con el comando
<br>

![Texto alternativo](imagenes/Screenshot_59.png)
<br>
Una vez descargado debemos descomprimirlo
<br>
![Texto alternativo](imagenes/Screenshot_60.png)
<br>
Como podemos ver ya tenemos wordpress instalado en el directorio "/var/www/html"
<br>
![Texto alternativo](imagenes/Screenshot_61.png)
<br>
Ya instalado wordpress necesitaremos un cliente MYSQL para crear la base de datos de wordpress
<br>
Instalaremos el cliente con el comando
<br>
![Texto alternativo](imagenes/Screenshot_62.png)
<br>
Ya con el cliente instalado tendremos que entrar en MYSQL 
<br>
![Texto alternativo](imagenes/Screenshot_63.png)
<br>
Y crearemos la base de datos para wordpress
<br>
![Texto alternativo](imagenes/Screenshot_64.png)
<br>
Una vez creada la base de datos entraremos en wordpress desde nuestro navegador para empezar a configurarlo, para entrar deberemos poner la ip de nuestra máquina en mi caso 54.211.14.162 seguida de la palabra wordpress.
<br>
Quedaría tal que así : "54.211.14.162/wordpress/"
<br>
![Texto alternativo](imagenes/Screenshot_65.png)
<br>
Y empezaremos con la configuración de wordpress, nos pedirán parametros básicos como el nombre de la base de datos, el usuario y contraseña del root...
<br>
![Texto alternativo](imagenes/Screenshot_66.png)
<br>

