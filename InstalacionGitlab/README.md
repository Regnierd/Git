# Instalación de Gitlab en Linux

![logo-git](https://github.com/Regnierd/Git/blob/main/Instalaci%C3%B3nGit/img/image.axd.png)

## Índice

- <a href="#1">1. Instalación en local de Gitlab</a>
- <a href="#2">2. Acceso</a>

Para esta práctica necesitaremos una máquina con Ubuntu 20.04 instalado. 

<a name="1"></a>

### 1. Instalación en local de Gitlab

Para esta práctica necesitamos actualizar los repositorios y el sistema operativo para tener una mayor seguridad. Con el comando: <b>sudo apt update && sudo apt upgrade.</b>

![1]()

A continuación instalaremos unos paquetes que necesitaremos más adelante. Como el vim o el curl. Con el comando: <b>sudo apt install -y vim curl ca-certificates apt-transport-https</b>

![2]()

Podemos optar a tener un script de shell que nos proporciona el equipo de Gitlab para configurar el repositorio APT, como unas dependencias necesarias. Ejecutaremos el siguiente comando:  <b>curl -s https://packages.gitlab.com/install/repositories/gitlab/gitlab-ce/script.deb.sh | sudo bash</b>

![3]()

Y ahora podemos proceder a instalar el gitlab con el comando <b>sudo apt install gitlab-ce.</b>

![4]()

Como vemos ha acabado la instalación de Gitlab.

![5]()

Por último, usaremos el siguiente comando para terminar la configuración:
<b>sudo gitlab-ctl reconfigure</b>. Esto puede tardar unos minutos.

![6]()

<a name="2"></a>

### 1. Acceso


