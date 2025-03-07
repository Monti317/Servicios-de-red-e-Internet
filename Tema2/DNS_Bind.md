# Instalación del servidor DNS Bind
<br>
Lo primero que vamos a hacer es actualizar nuestra máquina con los siguientes comandos:
<br>

![Texto alternativo](imagenes2/Screenshot_1.png)
<br>
![Texto alternativo](imagenes2/Screenshot_2.png)
<br>
Una vez el sistema está actualizado vamos a comenzar con la instalación del servicio Bind
<br>
![Texto alternativo](imagenes2/Screenshot_3.png)
<br>
Ya instalado pasaremos a la carpeta de configuración de bind que se encuentra en la ruta "/etc/bind/namedd.conf.options"
<br>
![Texto alternativo](imagenes2/Screenshot_4.png)
<br>
Dentro del archivo vamos a introducir los siguientes parámetros
<br>
![Texto alternativo](imagenes2/Screenshot_5.png)
<br>
Para validar la configuración vamos a poner el siguiente comando
<br>
![Texto alternativo](imagenes2/Screenshot_6.png)
<br>
Y para aplicar los cambios vamos a reiniciar el servidor BIND
<br>
![Texto alternativo](imagenes2/Screenshot_7.png)
<br>
Para que no tengamos problemas con el cortafuegos, vamos a habilitar Bind9
<br>
![Texto alternativo](imagenes2/Screenshot_8.png)
<br>
Y estableceremos como servidor DNS la ip de nuestra máquina, para esto vamos a editar el archivo "/etc/resolv.conf"
<br>
![Texto alternativo](imagenes2/Screenshot_9.png)
<br>
Ya dentro del archivo ponemos nuestra ip
<br>
![Texto alternativo](imagenes2/Screenshot_10.png)
<br>
Vamos a probar que tenemos conexión haciendo un ping a google
<br>
![Texto alternativo](imagenes2/Screenshot_11.png)
