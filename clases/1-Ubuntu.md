# 🐧 Introducción a Ubuntu y Linux

##  ¿Qué es Ubuntu?

**Ubuntu** es una distribución del sistema operativo **GNU/Linux** basada en **Debian**. Es una de las distribuciones más populares por su facilidad de uso, estabilidad y fuerte comunidad. Se utiliza ampliamente en servidores, entornos de desarrollo, sistemas embebidos, ciencia y escritorios personales.

---

##  Arquitectura básica de un sistema Linux

Un sistema Linux se compone de:

- **Kernel**: Núcleo del sistema que controla el hardware y gestiona los recursos.
- **Shell**: Interfaz de línea de comandos para interactuar con el sistema (ej. `bash`).
- **Sistema de archivos jerárquico**: Organización estructurada de todos los archivos y directorios.
- **Servicios (Daemons)**: Procesos que corren en segundo plano (ej. `systemd`, `cron`).
- **Usuarios y grupos**: Gestión de accesos y permisos de seguridad.

---

##  Principales distribuciones de Linux

| Distribución       | Basada en    | Enfoque principal                     |
|--------------------|--------------|----------------------------------------|
| **Ubuntu**         | Debian       | Escritorio, desarrollo, servidores     |
| **Debian**         | Independiente| Estabilidad, servidores                |
| **Fedora**         | Red Hat      | Últimas tecnologías, desarrolladores   |
| **CentOS / Rocky** | Red Hat      | Servidores empresariales               |
| **Arch Linux**     | Independiente| Control total, usuarios avanzados      |
| **Linux Mint**     | Ubuntu       | Escritorio amigable para principiantes |
| **Kali Linux**     | Debian       | Seguridad, pentesting                  |

---

##  Estructura de directorios en Linux

| Directorio     | Propósito                                                   |
|----------------|-------------------------------------------------------------|
| `/`            | Directorio raíz, contiene todo el sistema                   |
| `/home`        | Archivos personales de los usuarios                         |
| `/etc`         | Archivos de configuración del sistema                       |
| `/bin`, `/sbin`| Comandos esenciales del sistema                             |
| `/usr`         | Programas instalados y librerías compartidas                |
| `/opt`         | Programas de terceros instalados manualmente                |
| `/var`         | Datos variables (logs, correos, spool, etc.)                |
| `/boot`        | Archivos necesarios para el arranque del sistema            |
| `/dev`         | Archivos de dispositivos                                    |
| `/proc`, `/sys`| Información del sistema y del kernel                        |
| `/tmp`         | Archivos temporales                                         |

---

## Usos comunes de Ubuntu

- Desarrollo de software (Python, C++, ROS 2, Web)
- Educación y simulación (Gazebo, MATLAB, R)
- Administración de sistemas y redes (SSH, Docker, servidores web)
- Automatización de tareas con Bash scripting
- Virtualización y contenedores (QEMU, VirtualBox, LXD)
- Entornos gráficos personalizados y ligeros

---

La siguiente bibliogradía aborda más a detalle el uso básico de linux 

[Linux Essentials](https://learning.lpi.org/es/learning-materials/010-160/)

[Web Development Essentials](https://learning.lpi.org/es/learning-materials/030-100/)

A continuación se detallan una serie de comandos e información que serán importantes para la continuación del curso.

En general los comandos en ubuntu siguen la siguiente extructura:
```
comando (opciones) (argumentos)
```
y el uso de la consola se puede facilitat usando los siguientes atajos:

```
<backspace>, <Ctrl-h> Borrar un caracter hacia la izquierda.
<Ctrl-c> Terminar la ejecución de un comando y regresar a shell.
<Ctrl-u> Borra toda la línea.
<Ctrl-a> Ir al inicio de la línea.
<Ctrl-e> Ir al final de la línea.
<tab> Completa el comando o el nombre del archivo.
<Flecha arriba> Anterior comando.
<Flecha abajo> Siguiente comando.
<Shift page-up> Presenta la salida del comando anterior.
<Ctrl-r> Busca un comando dentro del history
```

## Comandos básicos de Linux
Aquí algunos comandos fundamentales que debes dominar:
1. Comandos generales
```
history # Guarda los últimos 1000 comandos ejecutados.
```
se puede ejercutar el comando del listado usando !
```
!n
```
utilizando el comando | grep podemos realizar una busqueda de palabras claves en el historial de comandos
```
history | grep palabra_clave
```
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
