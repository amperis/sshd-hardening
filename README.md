# sshd-hardening

Editar /etc/ssh/sshd_config

1. Cambiar el puerto por defecto del Daemon de SSH

Port 10022

2. Numero de intentos de conexión fallida antes de cerrar la sesion establecida a un usuario

MaxAuthTries 2

3. No permitir usuarios con contraseña en blanco

PermitEmptyPasswords no

4. Numero de seg los cuales puede permanacer un usuario sin intruducir la contraseña de Login

LoginGraceTime 20

5. Numero maximo de conexion simultaneas pendiente de autenticar para un usuario

MaxStartups 2

6. Establecer banner de incio 

Banner /etc/ssh/ssh-banner-txt

Ejemplo de banner:

==========================================================
All connections are monitored and recorded
Disconnect IMMEDIATELY if you are not an authorized user!
==========================================================

7. Tiempo en seg de cierre de sesion automatico tras inactividad del usuario

ClientAliveInterval 300
ClientAliveCountMax 0

8. Deshabilitar el uso de .rhost

IgnoreRhosts yes

9. Deshabilitar el forwarding de entorno X a través de SSH

X11forwarding no

