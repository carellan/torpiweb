TorPi - Panel de Control
=========
TorPi Panel de Control es una aplicación web que proporciona información del estado de la Raspberry Pi y la posibilidad de reiniciar, apagar el dispositivo y cambiar el estado del servicio TOR. 

Para poder ejectuarlo correctamente se necesitan los siguientes programas.

Instalar Apache y PHP
```
apt -y install apache2 php php-common
```
Una vez instado hay que realizar el git clone en la siguiente ruta
```
cd /var/www/html/

git clone https://github.com/carellan/torpiweb.git
```
Seguidamente, ya podemos acceder a nuestro servidor web indicando al final de este /torpiweb

Se ha dotado de un password para proteger el acceso.

**Preview:**

![alt tag](https://i.ibb.co/RBjFnLV/login-torpiweb.png)

![alt tag](https://i.ibb.co/ZHR19fY/torpi-control-panel.png)


Installation
--------------

You need to have a Webserver up and running on your Raspberry Pi. lighttpd, Apache2 have been testet, but i think others will do just fine. You need to have PHP enabled and be able to execute *shell_exec()* commmands.

For the reboot and shutdown buttons to work, you need to adjust your /etc/sudoers file by using
```sh
sudo visudo
```
and adding this line
```sh
www-data ALL=NOPASSWD:/sbin/shutdown
```
**WARNING:**
*After adding this line, the User www-data is able to restart and shutdown your Pi. Which means, anybody who might get access to your Pi over http could do so also. You need to secure it yourself. If your Pi is running in your local network, and there is nobody around who might shut down your Pi on purpose, this solution works fine without extra securing it.*

License
----

nada - do whatever you want. This was made quick and dirty, what means that this solution might work for me, but not for you. You may fork, rename, distribute, or do whatever you want, as long as you don't blame me for things getting broken or not working the way the should.

[JustGage]:http://justgage.com/
[Raphaël]:http://raphaeljs.com/
Carlos
HOLA
HI
