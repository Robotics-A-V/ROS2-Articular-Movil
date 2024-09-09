# Instalacion de Ubuntu 22.04 con VirtualBox

1.  [Descargar VirtualBox](https://www.oracle.com/virtualization/technologies/vm/downloads/virtualbox-downloads.html)

![Seleccion](../images/0-VB0.jpeg)

3. Configuracion de VirtualBOX

Selecciono la opción "nueva"

![Seleccion](../images/0-VB1.jpeg)


Coloco un nombre para la máquina virtual 

![Seleccion](../images/0-VB2.jpeg)

Cargo la imagen ISO

![Seleccion](../images/0-VB3.jpeg)

![Seleccion](../images/0-VB4.jpeg)

Agrego un Usuario y contraseña para la máquina virtual

![Seleccion](../images/0-VB5.jpeg)

Congifuro la memoria ram y el número de nucleos (se recomienda utilizar el 50% de la memoria RAM Física)

![Seleccion](../images/0-VB6.jpeg)

Para un uso básico se recomienda un total de 30 GB de memoria

![Seleccion](../images/0-VB7.jpeg)

Finalizo la configuración 

![Seleccion](../images/0-VB8.jpeg)

Arrancar Máquina virtual - Al iniciar la máquina de forma automática comenzará la instalación

![Seleccion](../images/0-VB9.jpeg)

Finalmente ingresar en la consola y ejecutar los comandos:
```
sudo apt update
```
```
sudo apt upgrade
```

***Posibles Errores*** -

1. Al momento de ejecutar la máquina virtual
NOT IN A HYPERVISOR PARTITION (HVP =0 ) [solucion](https://www.youtube.com/watch?v=XkLHhqOZmmY&t=5s)

2. No se abre el terminal
[solucion](https://www.youtube.com/watch?v=ncUctr7Ygrk)

3. [usuario] is not in the sudoers file

para este ejemplo el usuario de ubuntu se llama ubuntuROS por lo tanto en la terminal se deberá colocar el comando:
```
sudo usermod -aG sudo ubuntuROS
```
reiniciar el equipo y verificar que pueda actualizar el sistema:

```
sudo apt update
```
```
sudo apt upgrade
```
