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

