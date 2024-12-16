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

Ya configurados los permisos para el root, vamos a entrar en la base de datos recién creada para crear los usuarios:
```
use defaultsite_db;
```
![](Images/Screenshot_11.png)
```
create table mysql_auth ( username varchar(191) not null, passwd varchar(191), groups varchar(191), primary key (username) );
```
![](Images/Screenshot_12.png)
<br> 
Encriptaremos la contraseña:
```
htpasswd -bns siteuser siteuser
```
![](Images/Screenshot_13.png)
<br>
Una vez nos da el hash tendremos que ponerlo en la tabla que creamos anteriormente de los usuarios, para esto tendremos que volver a entrar en la base de datos:
```
use defaultsite_db;
```
E introduciremos el siguiente comando:
```
INSERT INTO `mysql_auth` (`username`, `passwd`, `groups`) VALUES('siteuser', '{SHA}tk7HEH6Wo7SKT6+3FHCgiGnJ6dA=', 'sitegroup');
```
![](Images/Screenshot_14.png)
<br>
Activaremos los módulos dbd, authn_dbd, socache_shmcb, authn_socache:
```
sudo a2enmod dbd
```

```
sudo a2enmod authn_dbd
```

```
sudo a2enmod socache_shmcb
```

```
sudo a2enmod authn_socache
```
![](Images/Screenshot_15.png)
<br>
Una vez todos habilitados reiniciaremos apache:
```
systemctl restart apache2
```
![](Images/Screenshot_16.png)
<br>
Creamos el directorio protegido.
```
sudo mkdir /var/www/html/protegido
```
```
sudo chown -R www-data:www-data /var/www/html/protegido
```
![](Images/Screenshot_17.png)
<br>
Tendremos que cambiar la configuración de nuestro dominio:
```
sudo nano /etc/apache2/sites-available/000-default.conf
```
![](Images/Screenshot_18.png)
<br>
Tendremos que introducir las siguientes lineas:
<br>
![](Images/Screenshot_19.png)
<br>
Una vez hemos hecho estas modificaciones reiniciaremos apache
<br>
Y como podemos ver una vez ponemos el usuario y la contraseña estamos dentro:
<br>
![](Images/Screenshot_20.png)
