# sshd-hardening

1. Cambiar el puerto por defecto del Daemon de SSH

Port 10022

2. Numero de intentos de conexión fallida antes de cerrar la sesion establecida

MaxAuthTries 2

3. No permitir usuarios con contraseña en blanco

PermitEmptyPasswords no

4. Numero de seg los cuales puede permanacer un usuario sin intruducir la contraseña de Login

LoginGraceTime 20

