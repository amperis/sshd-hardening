# sshd-hardening

Editar /etc/ssh/sshd_config

- Cambiar el puerto por defecto del Daemon de SSH
```
Port 10022
```
- Numero de intentos de conexión fallida antes de cerrar la sesion establecida a un usuario
```
MaxAuthTries 2
```
- No permitir usuarios con contraseña en blanco
```
PermitEmptyPasswords no
```
- No permitir autentificacion con root
```
PermitRootLogin no 
```
Algun usuario tendrá que poder hacer sudo
```
sysadmin ALL=(ALL) NOPASSWD:ALL
```
- Numero de seg los cuales puede permanacer un usuario sin intruducir la contraseña de Login
```
LoginGraceTime 20
```
- Numero maximo de conexion simultaneas pendiente de autenticar para un usuario
```
MaxStartups 2
```
- Establecer banner de incio 
```
Banner /etc/ssh/ssh-banner-txt
```
Ejemplo de banner:
```
All connections are monitored and recorded
Disconnect IMMEDIATELY if you are not an authorized user!
```
- Tiempo en seg de cierre de sesion automatico tras inactividad del usuario
```
ClientAliveInterval 300
ClientAliveCountMax 0
```
- Deshabilitar el uso de .rhost
```
IgnoreRhosts yes
```
- Deshabilitar el forwarding de entorno X a través de SSH
```
X11forwarding no
```
- Permitir hacer login solo a usuarios concretos
```
AllowUsers sysadmin operador
```

Otros permisos si proceden dependiente del sistema

- Limitar la interfaz donde escuchará el daemon
```
Listen 192.168.1.100
````
- Denegar la uthentificacion basada en contraseña y realizar en base a certificados
```
AuthenticationMethods publickey
PubkeyAuthentication yes
```
