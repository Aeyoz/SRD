# Instalación de un servidor SMTP en Windows Server 2016.

## Parte 1: Servicio SMTP

Faltaron los puntos:

    * Enviar varios correos desde / hacia las diferentes cuentas y comprobar envío (real o ficticio) y carpetas mailroot. Las carpetas existentes en mailroot alojan mensajes en cola (Queue), mensajes para destinatarios desconocidos (Badmail) y mensajes entregados (Drop)
* Nueva configuración de servicio SMTP a través del administrador de aplicaciones (IIS) 6.0. Establecer autenticación básica de Windows. Probar diferentes configuraciones de dominio predeterminado, cifrado TLS, etc.
  * En el cliente Windows:
    * Configurar las cuentas según los parámetros especificados en el servidor. Enviar varios correos desde / hacia las diferentes cuentas y comprobar envío y carpetas mailroot. En este caso sólo tendrán acceso al servidor SMTP cuentas del dominio y correspondientes a usuarios de AD.

### Instalación de los roles del servidor.

![](./mail/001.png)

![](./mail/002.png)

![](./mail/003.png)

![](./mail/004.png)

![](./mail/005.png)

![](./mail/006.png)

![](./mail/007.png)

![](./mail/008.png)

![](./mail/009.png)

![](./mail/010.png)

![](./mail/011.png)

![](./mail/012.png)

![](./mail/013.png)

![](./mail/014.png)

![](./mail/015.png)

![](./mail/016.png)

![](./mail/017.png)

![](./mail/018.png)

![](./mail/019.png)

![](./mail/020.png)

![](./mail/021.png)

![](./mail/022.png)

![](./mail/023.png)

![](./mail/024.png)

![](./mail/025.png)

![](./mail/026.png)

![](./mail/027.png)

![](./mail/028.png)

![](./mail/029.png)

![](./mail/030.png)

![](./mail/031.png)

![](./mail/032.png)

![](./mail/033.png)

## Parte 2: Cliente Htmail

Faltaron los puntos:

* Configura en el cliente Windows un cliente de correo como thunderbird o Live Mail (en los ordenadores clientes) para acceder al servidor de correo instalado en Windows 2016.
* Realiza prueba de envío y recepción de correos entre los diferentes usuarios, comprobando, además de envío y recepción correctas, el efecto de las opciones configuradas en las cuentas.
* Crea una lista de distribución empleados asociada al dominio y añade a los dos usuarios de miempresa.com a ella.
Realiza prueba de envío y recepción de correos por medio de la lista de distribución.

Debido a que no se encontró una solución para el error de identificacion de registro tipo mx.


![](./hmail/001.png)

![](./hmail/002.png)

![](./hmail/003.png)

![](./hmail/004.png)

![](./hmail/005.png)

![](./hmail/006.png)

![](./hmail/007.png)

![](./hmail/008.png)

![](./hmail/009.png)

![](./hmail/010.png)

![](./hmail/011.png)

![](./hmail/012.png)

![](./hmail/013.png)

![](./hmail/014.png)

![](./hmail/015.png)

![](./hmail/016.png)

![](./hmail/017.png)

![](./hmail/018.png)

![](./hmail/019.png)

![](./hmail/020.png)

![](./hmail/021.png)

![](./hmail/022.png)

![](./hmail/023.png)

![](./hmail/024.png)

![](./hmail/025.png)
