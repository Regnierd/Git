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

Ahora para comprobar que todo funciona correctamente abriremos un navegador de nuestra máquina y en la url pondremos nuestra ip o localhost. Al poner localhost en en la url vemos como nos aparece este login. Introducimos el usuario root y la contraseña.

![7](https://github.com/Regnierd/Git/blob/main/InstalacionGitlab/img/7.PNG)

Si al poner el usuario y contraseña nos da error, tendremos que cambiar la contraseña de root usando el siguiente comando: <b>sudo gitlab-rails console</b>, al cual entraremos a una consola de ruby. Primero tenemos que encontrar al usuario root, para ello usaremos el siguiente comando: user = <b>User.where(id: 1).first</b>

![8](https://github.com/Regnierd/Git/blob/main/InstalacionGitlab/img/8.PNG)

Una vez encontrado el usuario procedemos a cambiar la contraseña. Para ello usaremos el comando: <b>user.password = ‘contraseña’</b> y <b>user.password = ‘misma_contraseña’</b>. La segunda es para confirmar la contraseña cambiada, tienen que ser iguales. Después de confirmar la contraseña tenemos que guardar los cambios del usuario con el comando <b>user.save! </b>

![9](https://github.com/Regnierd/Git/blob/main/InstalacionGitlab/img/9.PNG)

Salimos de la terminal de ruby y volvemos hacer el comando <b>sudo gitlab-ctl reconfigure</b>.

![6](https://github.com/Regnierd/Git/blob/main/InstalacionGitlab/img/6.PNG)

Volvemos al navegador y procedemos a poner el usuario (root) y la contraseña que hemos puesto anteriormente. Una vez ingresado entraremos al servidor de Gitlab y nos saldrá una pantalla tal que así.

![10](https://github.com/Regnierd/Git/blob/main/InstalacionGitlab/img/10.PNG)




