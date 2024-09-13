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
3. 
