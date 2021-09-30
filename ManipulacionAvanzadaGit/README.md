# Manipulacion avanzada de repositorios en Git

![logo-git](https://github.com/Regnierd/Git/blob/main/Instalaci%C3%B3nGit/img/image.axd.png)

## Índice

- <a href="#1">Ejercicio 1</a>
- <a href="#2">Ejercicio 2</a>
- <a href="#3">Ejercicio 3</a>
- <a href="#4">Ejercicio 4</a>
- <a href="#5">Ejercicio 5</a>
- <a href="#6">Ejercicio 6</a>
- <a href="#7">Ejercicio 7</a>
- <a href="#8">Ejercicio 8</a>
- <a href="#9">Ejercicio 9</a>

Para empezar tenemos que hacer uso del siguiente comando: <b>git clone -link completo de tu repositorio-</b>. Y como podemos ver en la imagen se nos creó la clonación de nuestro repositorio remoto en la máquina local.

![1](https://github.com/Regnierd/Git/blob/main/ManipulacionAvanzadaGit/img/1.png)

<a name="1"></a>

### Ejercicio 1
Para mostrar el historial de todos los cambios de mi repositorio usaremos: <b>git show</b>

![2](https://github.com/Regnierd/Git/blob/main/ManipulacionAvanzadaGit/img/2.png)

Dentro de nuestro repositorio creamos la carpeta capítulos y dentro creamos un fichero con el nombre capitulo1.txt con una frase en su contenido.

![3](https://github.com/Regnierd/Git/blob/main/ManipulacionAvanzadaGit/img/3.png)

Guardamos los cambios que hemos hecho en el repositorio con <b>git add ./ </b>. Luego hacemos un commit de mi guardado anterior con un mensaje en específico de nuestro cambio en el repositorio. El comando sería: <b>git commit -m “Añadido capitulo 1”</b>.

![4](https://github.com/Regnierd/Git/blob/main/ManipulacionAvanzadaGit/img/4.png)

Volvemos a mostrar el historial del cambio realizado con <b>git log</b>.

![5](https://github.com/Regnierd/Git/blob/main/ManipulacionAvanzadaGit/img/5.png)

<a name="2"></a>

### Ejercicio 2
En este ejercicio creamos un segundo fichero llamado capitulo2.txt con un texto. Después de guardar el fichero, añadimos los cambios que hemos hecho con <b>git add</b>. Volvemos a crear otro commit con su mensaje específico con el mismo comando anterior.

![6](https://github.com/Regnierd/Git/blob/main/ManipulacionAvanzadaGit/img/6.png)

A continuación, mostramos las diferencias de la última versión con las dos versiones anteriores con el siguiente comando: <b>git diff HEAD~2..HEAD</b>

![7](https://github.com/Regnierd/Git/blob/main/ManipulacionAvanzadaGit/img/7.png)

<a name="3"></a>

### Ejercicio 3
En el ejercicio 3 volvemos a crear un tercer fichero llamado capitulo3.txt con un texto. Y repetimos los pasos que realizamos en el ejercicio anterior. Guardamos los cambios y hacemos el commit con su mensaje específico de los cambios.

![8](https://github.com/Regnierd/Git/blob/main/ManipulacionAvanzadaGit/img/8.png)

Ahora mostraremos las diferencias entre la primera versión y la última versión de nuestro repositorio con el siguiente comando: <b>git diff -hash del commit que queremos-..HEAD</b>. Para obtener el hash como el de la foto hay que usar el comando <b>git log</b> y te mostrará todo el historial del repositorio junto con el hash.

![21](https://github.com/Regnierd/Git/blob/main/ManipulacionAvanzadaGit/img/21.PNG)

<a name="4"></a>

### Ejercicio 4
Ahora creamos el archivo indice.txt con un texto. Volvemos a repetir los mismos pasos: guardamos y hacemos un commit con su mensaje. Por último, podemos ver quién ha hecho los cambios del fichero creado ahora mismo con el siguiente comando: <b>git annotate indice.txt</b>

![9](https://github.com/Regnierd/Git/blob/main/ManipulacionAvanzadaGit/img/9.png)

<a name="5"></a>

### Ejercicio 5
ara poder crear una rama en nuestro repositorio tenemos que usar el siguiente comando: <b>git branch -nombre de la rama-</b>. Para ver todas las ramas de nuestro repositorio se usa el siguiente comando de git: <b>git branch -av</b>. 

![10](https://github.com/Regnierd/Git/blob/main/ManipulacionAvanzadaGit/img/10.png)

<a name="6"></a>

### Ejercicio 6
En el ejercicio 6 creamos el cuarto capítulo, llamado capitulo4.txt, con un texto. Volvemos hacer los pasos de guardado y el commit con el mensaje específico.
Podemos ver todo el historial del repositorio incluyendo todas las ramas con el siguiente comando: <b>git log --graph --all --oneline</b>

![11](https://github.com/Regnierd/Git/blob/main/ManipulacionAvanzadaGit/img/11.png)

<a name="7"></a>

### Ejercicio 7
Ahora nos cambiamos a la rama bibliografía con el comando: <b>git checkout bibliografia</b> y creamos el fichero bibliografia.txt. con el texto que se ve en la imagen. Guardamos y hacemos el commit con su mensaje y volvemos a mostrar toda la historia con sus ramas con: <b>git log --graph --all --oneline</b>

![12](https://github.com/Regnierd/Git/blob/main/ManipulacionAvanzadaGit/img/12.png)

<a name="8"></a>

### Ejercicio 8
A continuación fusionamos la rama bibliografía con la rama main, para ello tenemos que volver a cambiarnos a la rama de main con el comando: <b>git checkout main</b>. Ahora podemos hacer la fusión entre las dos ramas con el siguiente comando: <b>git merge bibliografia</b> y podemos ver el cambio que hemos hecho mostrando todo el historial y con sus ramas.

![13](https://github.com/Regnierd/Git/blob/main/ManipulacionAvanzadaGit/img/13.png)

Ahora procedemos a eliminar la rama bibliografía con el comando: <b>git branch -d bibliografia</b>.

![14](https://github.com/Regnierd/Git/blob/main/ManipulacionAvanzadaGit/img/14.png)

Mostramos todas las ramas de nuestro repositorio y vemos que solo queda la rama main con el comando <b>git branch</b>.

![15](https://github.com/Regnierd/Git/blob/main/ManipulacionAvanzadaGit/img/15.png)

<a name="9"></a>

### Ejercicio 9
En el último ejercicio volvemos a crear la rama bibliografía con el primer comando que se ve en la imagen y nos cambiamos a la rama creada. Creamos un fichero llamado bibliografia.txt y le agregamos un texto. Procedemos a guardar los cambios y hacemos el commit con el mensaje específico. Volvemos a la rama main y nos mostrará un mensaje diciéndonos que la rama está adelantada por 8 commits, ya que no la hemos subido al repositorio remoto.

![17](https://github.com/Regnierd/Git/blob/main/ManipulacionAvanzadaGit/img/17.png)

A continuación modificamos el fichero bibligrafia.txt que contenga el siguiente mensaje que aparece en la imagen. Guardamos y volvemos hacer otro commit con el su mensaje. Ahora probamos a fusionar las dos ramas con el comando <b>git merge bibliografia</b>, pero nos dará un conflicto, ya que en la rama bibliografía el fichero bibliografia.txt tiene un texto y en la rama main tiene otro texto, por ello tenemos que arreglar este conflicto para poder hacer la fusión. El conflicto se resuelve eligiendo con cuál versión me quedo, con la que está hecha en la rama bibliografía o la de la main.

![18](https://github.com/Regnierd/Git/blob/main/ManipulacionAvanzadaGit/img/18.png)

Una vez hecho la elección volvemos a guardar los cambios y hacemos el commit con su mensaje. Podemos ver que nos devuelve un mensaje diciendo que se ha resuelto el conflicto de bibliografía.

![19](https://github.com/Regnierd/Git/blob/main/ManipulacionAvanzadaGit/img/19.png)

Por último, volvemos a mostrar toda el historial y podemos apreciar los cambios de las ramas y la última línea vemos la fusión realizada con éxito.

![20](https://github.com/Regnierd/Git/blob/main/ManipulacionAvanzadaGit/img/20.png)