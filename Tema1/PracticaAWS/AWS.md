## 1. Activar la autenticación con MySql
<br>
Para empezar actualizaremos nuestro servidor de Ubuntu con los siguientes comandos:

```
sudo apt update
```
![](Images/Screenshot_1.png)

```
sudo apt upgrade
```
![](Images/Screenshot_2.png)
<br>
Una vez que ya tenemos nuestro Ubuntu Server actualizado empezaremos con la instalación de apache:
```
sudo apt-get install apache2
```
![](Images/Screenshot_3.png)
<br>
Ya instalado apache nos tocará instalar PHP y MySQL:
```
sudo apt-get install apache2 php7.0 libapruti11-dbd-mysql -y
```
![](Images/Screenshot_4.png)
<br>
También instalaremos MariaDB:
```
sudo apt-get install mariadb-server mariadb-client -y
```
![](Images/Screenshot_5.png)
<br>
Ya todo esto instalado tendremos que activar los servicios, tanto de apache como de mysql:
```
sudo systemctl enable apache2
```
![](Images/Screenshot_6.png)
```
sudo systemctl enable mysql
```
![](Images/Screenshot_7.png)
<br>
