# Ubuntu

Para manejar de una forma más eficiente las distintas configuraciones de ROS2 es necesario conocer conceptos básicas de ubuntu, a continuación se detallan una serie de comandos e información que serán importantes para la continuación del curso.
La siguiente bibliogradía aborda el uso básico de linux 
[Linux Essentials](https://learning.lpi.org/es/learning-materials/010-160/)
[Web Development Essentials](https://learning.lpi.org/es/learning-materials/030-100/)

Entendiendo los comandos básicos de ubuntu.

1. Comandos básicos de Linux
Aquí algunos comandos fundamentales que debes dominar:

Gestión de archivos y directorios:
* ls: Lista archivos y directorios.
Ejemplo: ls -l muestra una lista detallada con permisos, propietarios, tamaño, etc.
cd: Cambia de directorio.
Ejemplo: cd /home/usuario te lleva al directorio del usuario.
mkdir: Crea un nuevo directorio.
Ejemplo: mkdir nuevo_directorio.
rm: Elimina archivos o directorios.
Ejemplo: rm archivo.txt elimina el archivo archivo.txt. rm -r carpeta elimina una carpeta y su contenido.
cp: Copia archivos o directorios.
Ejemplo: cp archivo1.txt archivo2.txt copia el archivo archivo1.txt en archivo2.txt.
mv: Mueve o renombra archivos y directorios.
Ejemplo: mv archivo.txt /ruta/destino mueve un archivo a una nueva ubicación.
Permisos y gestión de usuarios:
chmod: Cambia los permisos de archivos y directorios.
Ejemplo: chmod 755 archivo.sh otorga permisos de lectura, escritura y ejecución al propietario, y solo lectura y ejecución al resto.
chown: Cambia el propietario de archivos o carpetas.
Ejemplo: chown usuario:grupo archivo.txt.
sudo: Ejecuta comandos como superusuario (administrador).
Ejemplo: sudo apt update actualiza los paquetes del sistema con permisos de administrador.
Gestión de procesos:
ps: Muestra los procesos activos.
Ejemplo: ps aux lista todos los procesos.
top: Muestra los procesos en ejecución y su uso de recursos.
kill: Termina un proceso específico.
Ejemplo: kill 1234 termina el proceso con el PID 1234.
Instalación de paquetes y software:
apt: Usado para gestionar paquetes en distribuciones basadas en Debian (como Ubuntu).
Ejemplo: sudo apt install ros-humble-desktop instala la versión Humble de ROS2.
snap: Sistema para instalar paquetes universales.
Ejemplo: sudo snap install nombre_paquete.
SSH (Secure Shell):
¿Qué es SSH?: SSH permite acceso remoto seguro a otra máquina, útil cuando trabajas con robots o servidores de manera remota.
ssh usuario@ip_del_servidor: Conecta a un servidor remoto.
Ejemplo: ssh usuario@192.168.1.100 conecta a una máquina con esa IP.
Transferir archivos vía SSH (SCP):
scp archivo.txt usuario@192.168.1.100:/ruta/destino: Copia archivos a una máquina remota.
Gestión de red:
ifconfig: Muestra la configuración de red.
ping: Prueba la conexión a otra máquina.
Ejemplo: ping google.com verifica si hay conexión con Google.
netstat: Muestra las conexiones de red activas.
Firewall:
Configurar el firewall es esencial para habilitar o restringir puertos específicos, sobre todo al usar ROS o ROS2 en redes.

UFW (Uncomplicated Firewall): Firewall básico en Ubuntu.
sudo ufw status: Ver el estado del firewall.
sudo ufw enable: Habilitar el firewall.
sudo ufw allow 22: Permitir conexiones SSH (puerto 22).
sudo ufw allow 11311: Permitir conexiones en el puerto que usa ROS.
