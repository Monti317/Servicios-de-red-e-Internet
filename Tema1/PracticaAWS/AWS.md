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
Iniciados los servicios tendremos que crear la base de datos, para esto primero tendremos que entrar en mysql con el comando:
```
sudo mysql -u root -p
```
![](Images/Screenshot_8.png)
<br>
Creamos la BD con el comando:
```
create database defaultsite_db;
```
![](Images/Screenshot_9.png)
<br>
Una vez creada la base de datos tendremos que darle permisos totales a nuestro usuario root:
```
GRANT SELECT, INSERT, UPDATE, DELETE ON defaultsite_db.* TO 'defaultsite_admin'@'localhost' IDENTIFIED BY 'usuario';
```
```
GRANT SELECT, INSERT, UPDATE, DELETE ON defaultsite_db.* TO 'defaultsite_admin'@'localhost.localdomain' IDENTIFIED BY 'password';
```
```
flush privileges;
```

![](Images/Screenshot_10.png)

Ya configurados los permisos para el root, vamos a entrar en la base de datos recién creada:
```
use defaultsite_db;
```
![](Images/Screenshot_11.png)

