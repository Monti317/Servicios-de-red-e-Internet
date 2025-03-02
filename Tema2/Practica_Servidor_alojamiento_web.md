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
