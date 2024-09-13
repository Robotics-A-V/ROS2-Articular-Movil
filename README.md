## Introducción a ROS2 

Este repositorio contiene una serie de instrucciones para abordar la programación de robots con ROS2.

# Contenido
* [0. Prerrequisitos ](#0-Prerrequisitos )
    * [0.1 Instalación de Ubuntu](#01-Instalación-de-Ubuntu)
    * [0.2 Ubuntu y ROS2](#02-Ubuntu-y-ROS2)
    * [0.3 Instalación de ROS2](#03-Instalación-de-ROS2)
    * [0.4 GitHub](#04-GitHub)
* [1. Introducción](#1-Introducción)
* 
# 0. Prerrequisitos
# 0.1 Instalación de Ubuntu

Para el funcionamiento de ROS2 es necesario instalar Ubuntu, para el actual repositorio se usará Ubuntu 22.4.04 LTS y ROS2 .

Imagen ISO (ubuntu-22.04.4-desktop-amd64.iso): [Descarga](https://releases.ubuntu.com/22.04/)

Opción Máquina Virtual:[Tutorial](./clases/0-Maquina-Virtual.md)

Opcion Partición del disco (Cambiar por la Iso 22.04.4): [Tutorial](https://www.youtube.com/watch?v=_d6oT7rEoGc)

Verificación de instalación de Python

Ejecuto en la terminal
```
python3 --version
```
# 0.2 Ubuntu y ROS2

El manejo de la terminal de ubuntu es escencial para poder realizar proyectos de robótica que involucren el uso de ROS2.
[Tutorial](./clases/1-Ubuntu.md)

# 0.3 Instalación de ROS2

Si deseas aprender sobre el uso de ROS Noetic visita el siguiente link [Ros-Noetic](https://github.com/Robotics-A-V/Curso-ROS-?tab=readme-ov-file#02-Instalaci%C3%B3n-de-ROS)

La version que se va realizar para el curso de ROS2 es Humble, el soporte de Humble es hasta el a;o 2027. 

Humble se puede instalar desde 2 formas, usando los paquetes deb o utilizando el codigo fuente:

| Característica             | **Paquetes Debian (deb)**             | **Desde Fuentes (source)**      |
|----------------------------|---------------------------------------|---------------------------------|
| **Facilidad de instalación**| Muy fácil (`apt install`)             | Requiere descargar y compilar   |
| **Velocidad de instalación**| Muy rápida                            | Más lenta, debido a la compilación |
| **Flexibilidad**            | Limitada a las versiones oficiales    | Alta, puedes personalizar y modificar el código |
| **Mantenimiento**           | Automático con actualizaciones de Ubuntu | Manual, debes recompilar al actualizar |
| **Complejidad**             | Baja                                  | Alta, requiere manejo de dependencias y compilación |
| **Recomendado para**        | Usuarios que buscan estabilidad y rapidez | Desarrolladores o usuarios avanzados |

para el presente curso se utilizara la opcion de paquetes debian

link oficial [ROS2-Humble](https://docs.ros.org/en/humble/Installation/Ubuntu-Install-Debs.html)

Pasos para la instalacion:

1. Set Locales
   
Los locales son un conjunto de parámetros que definen cómo un sistema operativo debe manejar ciertos aspectos regionales y culturales, como la representación de texto, formatos de fecha y hora, monedas, números, y otros elementos específicos de la localización geográfica o del idioma. Cada sistema operativo tiene una configuración de locales que asegura que el software y las interfaces funcionen correctamente en diferentes entornos culturales.

El objetivo de esta sección es asegurarse de que tu sistema esté configurado para soportar UTF-8 antes de instalar ROS 2. Los siguientes comandos generalmente se usan para configurar las locales en un entorno basado en Ubuntu:
```
locale  # check for UTF-8

sudo apt update && sudo apt install locales
sudo locale-gen en_US en_US.UTF-8
sudo update-locale LC_ALL=en_US.UTF-8 LANG=en_US.UTF-8
export LANG=en_US.UTF-8

locale  # verify settings
```
2. Fuentes de configuración

Tendrá que añadir el repositorio ROS 2 apt a su sistema.

Primero asegúdese de que el repositorio de Ubuntu Universe esté habilitado.
```
sudo apt install software-properties-common
sudo add-apt-repository universe
```
3. Configurar los repositorios de Ubuntu

ROS 2 depende de algunas herramientas adicionales. Primero, debes asegurarte de que tu máquina esté completamente actualizada y tenga las herramientas necesarias.

```
sudo apt update && sudo apt install curl -y
```
ahora es necesario agregar la clave GPG para ROS 2:
```
sudo curl -sSL https://raw.githubusercontent.com/ros/rosdistro/master/ros.key -o /usr/share/keyrings/ros-archive-keyring.gpg
```
y agregar el repositorio de ROS 2 Humble a tu lista de fuentes:
```
echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/ros-archive-keyring.gpg] http://packages.ros.org/ros2/ubuntu $(. /etc/os-release && echo $UBUNTU_CODENAME) main" | sudo tee /etc/apt/sources.list.d/ros2.list > /dev/null
```

4. Instalar ROS 2 Humble
Actualizar el indice de contenidos
```
sudo apt update
```
Actualizar el sistema
```
sudo apt upgrade
```
Instalacion de ROS HUMBLE
```
sudo apt install ros-humble-desktop
```
para poder utilizar las herramientas de construccion de paquetes es necesario instalar las herrmientas adicionales utilizando el siguietne comando 
```
sudo apt install ros-dev-tools
```
