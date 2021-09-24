# Manipulación de repositorios en Git 

![logo-git](https://github.com/Regnierd/Git/blob/main/Instalaci%C3%B3nGit/img/image.axd.png)

## Índice

- <a href="1">Configuracion</a>
- <a href="2">Creación de un repositorio</a>
- <a href="3">Comprobar el estado del repositorio</a>
- <a href="4">Realizando Commit's</a>
- <a href="5">Modificación de ficheros</a>
- <a href="6">Historial</a>

<a name="1"></a>

### Configuración 
Para manipular Git sin ningún problema hay que configurar el nombre de usuario, correo electrónico y el color de salida. Con los siguientes comandos:
- <b>git config --global user.name “Javier”
- git config --global user.email “correo electronico”
- git config --global color.ui auto
- git config --list (para mostrar la configuración por pantalla)</b>

![1](https://github.com/Regnierd/Git/blob/main/ManipulacionGit/img/1.PNG)

### Creación de un repositorio 
A continuación, creamos un repositorio en el directorio /home/javier/<b>dpl</b>. Para crear el repositorio necesitamos usar el siguiente comando: <b>git init</b> y podemos ver como se crea <b>.git</b> dentro de <b>/dpl.</b>

![2](https://github.com/Regnierd/Git/blob/main/ManipulacionGit/img/2.PNG)

### Comprobar el estado del repositorio
Para comprobar el estado del repositorio necesitamos usar el comando: <b>git status</b>. Que te muestra en qué rama estás y si hay commits por resolver. Ahora creamos un archivo <b>.txt</b> dentro del repositorio con algo escrito dentro.

![3](https://github.com/Regnierd/Git/blob/main/ManipulacionGit/img/3.PNG)

Ahora volvemos a usar <b>git status</b> y podemos apreciar que hay un archivo sin seguimiento. Para que deje de estar en seguimiento usamos: <b>git add nombre-fichero</b>

![4](https://github.com/Regnierd/Git/blob/main/ManipulacionGit/img/4.PNG)

### Realizando Commit's
Para que deje de decirnos que hay un archivo sin seguimiento necesitamos usar el siguiente comando: <b>git commit -m “nombre-del-commit”</b>, una vez lanzado vemos como 1 fichero ha cambiado y hay 2 inserciones. Hacemos otra vez <b>git status</b> y vemos que ya no nos aparece que hay un fichero sin seguimiento.

![5](https://github.com/Regnierd/Git/blob/main/ManipulacionGit/img/5.PNG)

### Modificación de ficheros
Cambiamos el fichero que creamos antes para ver los cambios comparado con la versión guardada anteriormente.

![6](https://github.com/Regnierd/Git/blob/main/ManipulacionGit/img/6.PNG)

Para ello usamos: <b>git diff</b> y vemos que lo que está en rojo es lo que había antes y lo que está en verde es lo que hemos cambiado de nuevo.

![7](https://github.com/Regnierd/Git/blob/main/ManipulacionGit/img/7.PNG)

Agregamos los cambios nuevamente con <b>git add nombre-fichero</b> y luego hacemos un commit con los cambios que hemos hecho.

![8](https://github.com/Regnierd/Git/blob/main/ManipulacionGit/img/8.PNG)

### Historial
Podemos cambiar los nombres de los commit con el siguiente comando: <b>git commit --amend -m “nombre-nuevo-del-commit”</b>

![9](https://github.com/Regnierd/Git/blob/main/ManipulacionGit/img/9.PNG)
