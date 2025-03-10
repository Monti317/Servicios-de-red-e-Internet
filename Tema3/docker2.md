# Docker Práctica 2

## Lleva a cabo la práctica descrita en el primer artículo

### 1. Ejecuta la imagen `hello-world`.
<br>
Para ejecutar la imagen "hellow-world" tendremos que introducir el siguiente comando
<br>

![Texto alternativo](imagenes1/Screenshot_1.png)
<br>
### 2. Muestra las imágenes Docker instaladas.
<br>
Para mostrar las imagenes de docker instaladas utilizaremos el comando
<br>

![Texto alternativo](imagenes1/Screenshot_2.png)
<br>
### 3. Muestra los contenedores Docker.
<br>
Para mostrar los contenedores de Docker utilizaremos el comando
<br>

![Texto alternativo](imagenes1/Screenshot_3.png)
<br>
## Lleva a cabo la práctica descrita en el segundo artículo

### 1. Edita el fichero Dockerfile.
<br>
Lo primero que tenemos que buscar es una aplicación para editar, el mismo Docker en su Github tiene una llamada "getting-started-app.git", por lo cuál es la que escogeremos
<br>

![Texto alternativo](imagenes1/Screenshot_4.png)
<br>
Y editaremos el archivo con los siguientes parámetros
<br>
![Texto alternativo](imagenes1/Screenshot_5.png)
<br>
### 2. Construye el contenedor.
Para construir el contenedor vamos a usar el comando "build"
<br>

![Texto alternativo](imagenes1/Screenshot_6.png)
<br>
### 3. Ejecutalo.
<br>
Usaremos el comando "run"
<br>

![Texto alternativo](imagenes1/Screenshot_7.png)
<br>
Como podemos ver ya esta funcionando correctamente
<br>
![Texto alternativo](imagenes1/Screenshot_8.png)
<br>
### 4. Crea una cuenta en hub.docker.com
<br>
Creamos la cuenta
<br>

![Texto alternativo](imagenes1/Screenshot_9.png)
<br>
Y creamos un repositorio
<br>
![Texto alternativo](imagenes1/Screenshot_10.png)
<br>
Rellenamos los datos del repositorio
<br>
![Texto alternativo](imagenes1/Screenshot_11.png)
<br>
### 5. Publícalo.
<br>
Antes tendremos que iniciar sesión con la cuenta que previamente creamos
<br>

![Texto alternativo](imagenes1/Screenshot_12.png)
<br>
Etiquetamos la imagen local con el siguiente comando
<br>
![Texto alternativo](imagenes1/Screenshot_13.png)
<br>
Creamos un nuevo commit del contenedor
<br>
![Texto alternativo](imagenes1/Screenshot_14.png)
<br>
Subimos la imagen al repositorio que hemos creado
<br>
![Texto alternativo](imagenes1/Screenshot_15.png)
<br>
Y como podemos ver la imagen ya aparece en nuestro repositorio
<br>

![Texto alternativo](imagenes1/Screenshot_16.png)
