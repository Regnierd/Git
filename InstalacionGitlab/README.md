# Instalación de Gitlab en Linux

![logo-git](https://github.com/Regnierd/Git/blob/main/Instalaci%C3%B3nGit/img/image.axd.png)

## Índice

- <a href="#1">1. Instalación en local de Gitlab</a>
- <a href="#2">2. Acceso</a>

Para esta práctica necesitaremos una máquina con Ubuntu 20.04 instalado. 

<a name="1"></a>

### 1. Instalación en local de Gitlab

Para esta práctica necesitamos actualizar los repositorios y el sistema operativo para tener una mayor seguridad. Con el comando: <b>sudo apt update && sudo apt upgrade.</b>

![1](https://github.com/Regnierd/Git/blob/main/InstalacionGitlab/img/1.png)

A continuación instalaremos unos paquetes que necesitaremos más adelante. Como el vim o el curl. Con el comando: <b>sudo apt install -y vim curl ca-certificates apt-transport-https</b>

![2](https://github.com/Regnierd/Git/blob/main/InstalacionGitlab/img/2.png)

Podemos optar a tener un script de shell que nos proporciona el equipo de Gitlab para configurar el repositorio APT, como unas dependencias necesarias. Ejecutaremos el siguiente comando:  <b>curl -s https://packages.gitlab.com/install/repositories/gitlab/gitlab-ce/script.deb.sh | sudo bash</b>

![3](https://github.com/Regnierd/Git/blob/main/InstalacionGitlab/img/3.png)

Y ahora podemos proceder a instalar el gitlab con el comando <b>sudo apt install gitlab-ce.</b>

![4](https://github.com/Regnierd/Git/blob/main/InstalacionGitlab/img/4.png)

Como vemos ha acabado la instalación de Gitlab.

![5](https://github.com/Regnierd/Git/blob/main/InstalacionGitlab/img/5.PNG)

Por último, usaremos el siguiente comando para terminar la configuración:
<b>sudo gitlab-ctl reconfigure</b>. Esto puede tardar unos minutos.

![6](https://github.com/Regnierd/Git/blob/main/InstalacionGitlab/img/6.PNG)

<a name="2"></a>

### 1. Acceso




