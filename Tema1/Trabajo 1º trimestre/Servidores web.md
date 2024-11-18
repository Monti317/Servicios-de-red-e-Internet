## 1. Instalación del servidor web apache.
Usaremos dos dominios mediante el archivo hosts: `centro.intranet` y `departamentos.centro.intranet`
<br>
El primero servirá el contenido mediante wordpress y el segundo una aplicación en python.
<br>
Comenzaremos con la instalación de Apache, pero primero lo que vamos a hacer es actualizar nuestro ubuntu con los siguientes comandos:
<br>
![Update1](images/Screenshot_1.png)
<br>
Una vez descargadas las actualizaciones vamos a instalarlas con el siguiente comando:
<br>
![Update2](images/Screenshot_2.png)
<br>
Ya tenemos nuestro sistema operativo actualizado vamos a comenzar con  la instalación de Apache.
<br>
Para la instalación de apache vamos a poner el siguiente comando:
<br>
```sudo apt install apache2```
<br>
![Instalacion Apache](images/Screenshot_3.png)
<br>
Ya instalado vamos a comprobar que todo este correctamente, para esto vamos a poner el siguiente comando:
<br>
```service apache2 status```
<br>
![Comprobamos Instalacion Apache](images/Screenshot_4.png)
