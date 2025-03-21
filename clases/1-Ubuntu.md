# Ubuntu

🐧 Introducción a Ubuntu y Linux

Ubuntu es una distribución del sistema operativo GNU/Linux basada en Debian. Es ampliamente utilizada por su estabilidad, seguridad, facilidad de uso y una comunidad activa. Ubuntu es ideal tanto para usuarios nuevos como para desarrolladores y administradores de sistemas.

🧱 Arquitectura de un sistema Linux

Un sistema Linux está compuesto por:

Kernel: El núcleo del sistema operativo. Administra el hardware y los recursos.

Shell: Interfaz de línea de comandos para ejecutar instrucciones (bash, zsh).

Sistema de archivos: Organización jerárquica donde todo es un archivo.

Servicios/Daemons: Procesos que corren en segundo plano.

Usuarios y Grupos: Controlan el acceso y la seguridad del sistema.

🧩 Distribuciones populares de Linux

Distribución

Basada en

Enfoque principal

Ubuntu

Debian

General, escritorio y servidores

Debian

Independiente

Estabilidad, servidores

Fedora

Red Hat

Tecnologías recientes, desarrollo

Arch Linux

Independiente

Usuarios avanzados

Linux Mint

Ubuntu

Escritorio amigable

Kali Linux

Debian

Seguridad y auditorías

CentOS / Rocky

Red Hat

Empresas, servidores

📂 Directorios principales del sistema

Directorio

Descripción

/

Directorio raíz del sistema

/home

Directorios personales de los usuarios

/etc

Archivos de configuración del sistema

/usr

Programas y bibliotecas del sistema

/opt

Software adicional instalado manualmente

/var

Archivos variables: logs, bases de datos, etc.

/tmp

Archivos temporales

/dev

Archivos que representan dispositivos

/proc y /sys

Información sobre el sistema y el kernel

/boot

Archivos necesarios para el arranque

🛠️ Usos comunes de Ubuntu

Desarrollo de software (Python, C++, ROS, Web)

Automatización y scripting con Bash

Simulación robótica (Gazebo, RViz, ROS 2)

Entornos virtualizados (KVM, VirtualBox)

Servidores web y de base de datos (Apache, MySQL)

Educación, ciencia y centros de investigación



Para manejar de una forma más eficiente las distintas configuraciones de ROS2 es necesario conocer conceptos básicas de ubuntu, a continuación se detallan una serie de comandos e información que serán importantes para la continuación del curso.

La siguiente bibliogradía aborda el uso básico de linux 

[Linux Essentials](https://learning.lpi.org/es/learning-materials/010-160/)

[Web Development Essentials](https://learning.lpi.org/es/learning-materials/030-100/)




Entendiendo los comandos básicos de ubuntu.

En general los comandos en ubuntu siguen la siguiente extructura:
```
comando (opciones) (argumentos)
```

## Comandos básicos de Linux
Aquí algunos comandos fundamentales que debes dominar:
1. Dominio de la consola
* echo: Escribe un mensaje para sí mismo.

2. Gestion de arhivos y directorios
* ls: Lista archivos y directorios.
```
ls -l # muestra una lista detallada con permisos, propietarios, tamaño, etc.
```
* cd: Cambia de directorio.
```
cd /home/ # te lleva al directorio Home.
```
* mkdir: Crea un nuevo directorio.
```
mkdir nuevo_directorio.
```

* rm: Elimina archivos o directorios.
```
rm archivo.txt # elimina el archivo archivo.txt.
```
```
rm -r carpeta # elimina una carpeta y su contenido.
```
* cp: Copia archivos o directorios.
```
cp archivo1.txt archivo2.txt # copia el archivo archivo1.txt en archivo2.txt.
```
* mv: Mueve o renombra archivos y directorios.
```
mv archivo.txt /ruta/destino # mueve un archivo a una nueva ubicación.
```
2. Permisos y gestión de usuarios:

* chmod: Cambia los permisos de archivos y directorios.
```
chmod 755 archivo.sh # otorga permisos de lectura, escritura y ejecución al propietario, y solo lectura y ejecución al resto.
```
* chown: Cambia el propietario de archivos o carpetas.
```
chown usuario # grupo archivo.txt.
```

* sudo: Ejecuta comandos como superusuario (administrador).
```
sudo apt update # actualiza los paquetes del sistema con permisos de administrador.
```
3. Gestión de procesos:

* ps: Muestra los procesos activos.
```
ps aux # lista todos los procesos.
```
* top: Muestra los procesos en ejecución y su uso de recursos.

* kill: Termina un proceso específico.
```
kill 1234 # termina el proceso con el PID 1234.
```
4. Instalación de paquetes y software:

* apt: Usado para gestionar paquetes en distribuciones basadas en Debian (como Ubuntu).
```
sudo apt install ros-humble-desktop # instala la versión Humble de ROS2.
```

* snap: Sistema para instalar paquetes universales.
```
sudo snap install nombre_paquete.
```
5. SSH (Secure Shell):
¿Qué es SSH?: SSH permite acceso remoto seguro a otra máquina, útil cuando trabajas con robots o servidores de manera remota.
estructura:  ssh usuario@ip_del_servidor # Conecta a un servidor remoto.
```
ssh usuario@192.168.1.100  # conecta a una máquina con esa IP.
```
* Transferir archivos vía SSH (SCP):
```
scp archivo.txt usuario@192.168.1.100:/ruta/destino  # Copia archivos a una máquina remota.
```
6. Gestión de red:
* ifconfig: Muestra la configuración de red.

* ping: Prueba la conexión a otra máquina.
```
ping google.com # verifica si hay conexión con Google.
```
* netstat: Muestra las conexiones de red activas.

*Firewall:
Configurar el firewall es esencial para habilitar o restringir puertos específicos, sobre todo al usar ROS o ROS2 en redes.

UFW (Uncomplicated Firewall): Firewall básico en Ubuntu.
```
sudo ufw status #Ver el estado del firewall.
```
```
sudo ufw enable #Habilitar el firewall.
```
```
sudo ufw allow 22 #Permitir conexiones SSH (puerto 22).
```
```
sudo ufw allow 11311 #Permitir conexiones en el puerto que usa ROS.
```
