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
