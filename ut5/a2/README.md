
<center>

# Instalación de cliente de Correo en Linux


</center>

***Nombre: Ayoze Hernández Díaz***
***Curso: 2º de Ciclo Superior de Administración de Sistemas Informáticos en Red.***

### ÍNDICE

+ [Introducción](#id1)
+ [Objetivos](#id2)
+ [Material empleado](#id3)
+ [Desarrollo](#id4)
+ [Conclusiones](#id5)



#### ***Instalación de postfix***. <a name="id1"></a>

Instalamos el postfix con el comando **sudo apt-get install postfix**.

![](./img/1.postfix/001.png)

Elegimos la opcion de sitio de Internet.

![](./img/1.postfix/002.png)

Definimos el nombre del sistema que vamos a usar para el servidor de correo.

![](./img/1.postfix/003.png)

Iniciamos el servicio de postfix con **sudo /etc/init.d/postfix start** (no aparece sudo en la imagen porque ya somos root).

![](./img/1.postfix/004.png)

Usamos el comando **netstat -utap** para ver las conexiones activas

![](./img/1.postfix/006.png)

Definimos un usuario angel y le añadimos contraseña.

![](./img/1.postfix/009.png)

Usamos **telnet localhost 25** para conectarnos dentro de la propia máquina para conectarnos al servicio de correo.

![](./img/1.postfix/007.png)


Ahora usamos:
* helo localhost para usar usuarios del sistema para enviar un correo.
* mail from: ayoze para especificar el usuario
* rcpt to: angel para especificar a que usuario se va a enviar.
* data para ver el correo y enviarlo.

![](./img/1.postfix/008.png)

Iniciamos sesión como angel y miramos el archivo de texto que se ha creado en **/var/spool/mail/angel**.

![](./img/1.postfix/010.png)

#### ***Instalación de Evolution***. <a name="id2"></a>

Instalamos el cliente de correo evolution con **sudo apt install evolution** en el cliente.

![](./img/1.postfix/011.png)

Dentro del fichero **/etc/hosts** añadimos 2 registros asociados a la ip  del servidoren el cliente siendo estos:

* **smtp.w34u.com**
* **pop.w34u.com**

![](./img/1.postfix/012.png)

Abrimos el evolution para empezar a configurarlo (la mayoría de capturas van por defecto).

![](./img/2.evolution/013.png)

![](./img/2.evolution/014.png)

Definimos un usuario con cuenta de correo en el servidor.

![](./img/2.evolution/015.png)

Definimos el servidor para el servicio **pop**.

![](./img/2.evolution/016.png)

![](./img/2.evolution/017.png)

Definimos el servidor para el servicio **smtp**.

![](./img/2.evolution/018.png)

Intentamos enviar un correo de prueba.

![](./img/2.evolution/025.png)

Pero vemos que se nos queda colgado enviando el mensaje. (Probe a añadir usuarios desde el propio).

![](./img/2.evolution/026.png)

#### ***Instalación de Squirrelmail***. <a name="id3"></a>

Aunque este componente sea del último apartado se debe de instalar en este porque lo requiere.

![](./img/3.squirrelmail/027.png)

Instalamos el squirrelmail con **apt install squirrelmail**.

![](./img/3.squirrelmail/014.png)

Vemos con tree lo que hay en la carpeta de **/etc/squirrelmail**.

![](./img/3.squirrelmail/015.png)

Copiamos el fichero de configuración de apache dentro de /etc/squirrelmail a /etc/apache2/sites-available.

![](./img/3.squirrelmail/016.png)

Vemos el estado del servicio y luego lo reiniciamos.

![](./img/3.squirrelmail/017.png)



![](./img/3.squirrelmail/018.png)

Hacemos un enlace simbólico en **/etc/apache2/sites-enable**

![](./img/3.squirrelmail/019.png)

Habilitamos el sitio con **a2ensite squirrel.conf**.

![](./img/3.squirrelmail/020.png)

Comprobamos el estado del apache2.

![](./img/3.squirrelmail/021.png)

Entramos **localhost/squirrelmail**

![](./img/3.squirrelmail/022.png)

Cuando entramos con uno de los usuarios mostrados a continuación:

* Roberto
* Fernando

Devuelve el siguiente error.

![](./img/3.squirrelmail/028.png)

Busque información sobre como arreglar el error y decia de añadir a los usuarios al grupo mail, cosa que no funcionó. Puedo acceder a diferentes INBOX, pero no al que interesa.

INBOXES ACCESIBLES

* Borradores
* Enviados
* Papelera

![](./img/3.squirrelmail/026.png)

![](./img/3.squirrelmail/028.png)
