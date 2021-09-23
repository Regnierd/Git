# Instalación de Git en Local

![logo-git](https://github.com/Regnierd/Git/blob/main/Instalaci%C3%B3nGit/img/image.axd.png)

## Índice
- <a href="#1">Instalación de Git desde la fuente </a>
- <a href="#2">Configuración de Git </a>

<a name="1"></a>

### Instalación de Git desde la fuente
Antes de empezar con la instalación habrá que actualizar los paquetes del repositorio de Ubuntu. Para ello usaremos el siguiente comando: <b>sudo apt update</b>. Ponemos la contraseña de administrador para que empiece a actualizar.

![1](https://github.com/Regnierd/Git/blob/main/Instalaci%C3%B3nGit/img/1.png)

Una vez acabada la actualización, comprobamos que tenemos git instalado con el siguiente comando: <b>git --version</b> o <b>git -v</b>. En nuestro caso no lo tenemos instalado para hacer la práctica. 

![2](https://github.com/Regnierd/Git/blob/main/Instalaci%C3%B3nGit/img/2.png)

Antes de descargar Git e instalarlo necesitamos instalar el software necesario para que Git funcione correctamente. Instalaremos los paquetes necesarios desde los repositorios predeterminados.
Comando para la instalación: <b>sudo apt install libz-dev libssl-dev libcurl4-gnutls-dev libexpat1-dev gettext cmake gcc</b>

![3](https://github.com/Regnierd/Git/blob/main/Instalaci%C3%B3nGit/img/3.png)

Cuando acabe la instalación creamos una carpeta temporal en la ruta /home/javier/<b>tmp</b>, después de crearla nos colocamos dentro de dicho directorio para descargar Git en ella.

![4](https://github.com/Regnierd/Git/blob/main/Instalaci%C3%B3nGit/img/4.png)

Para poder descargar desde la web directamente necesitaremos <b>curl</b> instalado. Es tan fácil como el siguiente comando: <b>sudo apt install curl</b>. Comprobamos que se instaló con el comando <b>curl --version</b> o <b>curl -v</b>.

![5](https://github.com/Regnierd/Git/blob/main/Instalaci%C3%B3nGit/img/5.png)

Ahora procedemos a descarga desde la web de Git con el enlace https://mirrors.edge.kernel.org/pub/software/scm/git/ añadiendo la versión que queramos, en nuestro caso usaremos la más reciente, que sería la 2.29.3, el cual lo llamaremos <b>git.tar.gz</b>.
El comando sería tal que así: <b>curl -o git.tar.gz https://mirrors.edge.kernel.org/pub/software/scm/git/git-2.29.3.tar.gz</b>

![6](https://github.com/Regnierd/Git/blob/main/Instalaci%C3%B3nGit/img/6.png)

Descomprimimos el archivo git.tar.gz con el siguiente comando: <b>tar -zxf git.tar.gz</b>
y como vemos en la imagen veremos un directorio con el nombre <b>git-2.29.3</b>

![7](https://github.com/Regnierd/Git/blob/main/Instalaci%C3%B3nGit/img/7.png)

Entramos al nuevo directorio creado de Git. A partir de ahora podemos empezar a instalar el paquete con los dos siguientes comandos: <b>make prefix=/usr/local all</b>

![8](https://github.com/Regnierd/Git/blob/main/Instalaci%C3%B3nGit/img/8.png)

El segundo comando sería: <b>sudo make prefix=/usr/local install</b>

![9](https://github.com/Regnierd/Git/blob/main/Instalaci%C3%B3nGit/img/9.png)

Por último, necesitamos que se use la versión de Git recién instalada. Para ello usamos el siguiente comando: <b>exec bash</b>.

![10](https://github.com/Regnierd/Git/blob/main/Instalaci%C3%B3nGit/img/10.png)

### Configuración de Git

Una vez instalado correctamente Git, con la versión especificada, procedemos a configurarlo. Lo básico para configurar será nuestro nombre y nuestro correo electrónico, porque en las confirmaciones de que hagamos Git insertará nuestra información.
Para ello usaremos los dos siguientes comandos: 
- <b>git config --global user.name “Javier”</b>
- <b>git config --global user.email “javivi_lp_96@hotmail.es”</b>

![11](https://github.com/Regnierd/Git/blob/main/Instalaci%C3%B3nGit/img/11.png)

Para ver los cambios realizados usaremos el siguiente comando: <b>git config --list</b>

![12](https://github.com/Regnierd/Git/blob/main/Instalaci%C3%B3nGit/img/12.png)

Al haber cambiado estas dos opciones evitaremos mensajes de advertencia cuando hagamos una confirmación con Git. 
