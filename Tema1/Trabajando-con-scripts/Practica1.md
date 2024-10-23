1. **Crea un script que añada un puerto de escucha en el fichero de configuración de Apache. El puerto se recibirá como parámetro en la llamada y se comprobará que no esté ya presente en el fichero de configuración.**
<br>
¿Qué acciones realiza este script?
<br>
-Verificación de parámetros<br>
-Verificación del puerto<br>
-Copia de seguridad y adición del puerto<br>

![Texto alternativo](images/Screenshot_1.png)

2. **Crea un script que añada un nombre de dominio y una ip al fichero hosts. Debemos comprobar que no existe dicho dominio en el fichero hosts**
<br>
¿Qué acciones realiza este script?
<br>
-Verificación de parámetros: Comprueba que se hayan pasado exactamente dos parámetros (una IP y un dominio). Si no es así, muestra un mensaje de error.
<br>
-Comprobación de existencia: Verifica si la IP y el dominio ya existen en el archivo /etc/hosts. Si ya existen, muestra un mensaje de error.
<br>
-Copia de seguridad y adición: Si no existen, realiza una copia de seguridad del archivo /etc/hosts y añade la nueva entrada (IP y dominio) al final del archivo, indicando que se ha añadido correctamente.
<br>

![Texto alternativo](images/Captura2.png)

3. **Crea un script que nos permita crear una página web con un título, una cabecera y un mensaje**
<br>
¿Qué acciones realiza este script?
<br>
-Cambio de directorio: Se mueve al directorio /var/www/monti.com y muestra la ruta actual.
<br>
-Entrada del usuario: Solicita al usuario que ingrese el nombre del archivo HTML.
<br>
-Verificación de existencia: Comprueba si el archivo ya existe. Si existe, pregunta al usuario si desea sobreescribirlo.
<br>
Si el usuario elige no sobreescribir, la operación se cancela.
<br>
-Recopilación de datos: Solicita al usuario que ingrese el título de la página, la cabecera y el mensaje.

![Texto alternativo](images/Captura3.png)
