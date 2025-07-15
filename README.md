# Exploring GIT internals: Understanding Areas and Workflow
##### Working Area(wip / working in progress)
    Area donde se encuentran los archivos en la unidad de almacenamiento, donde se esta trabajando

##### Staging Area
    Esta area nos sirve para darle seguimiento a nuestros archivos, si trabajaramos unicamente en el working area cualquier modificacion GIT no lo tendria a la vista.

## git init
    Instruccion para crear un repositorio git

```
git init
```    
![Descripción de la imagen](/images/git_init.png)


Crea una carpeta con el nombre del proyecto y inicializa un proyecto git
```
git init <name project>
``` 

## git add
    Adding a file in a staging area
```
> git add hello.c
```
![Descripción de la imagen](/images/git_add.png)

## Regresar un archivo de staging area a working directory

```
git rm --cached <file> ...
```

![Descripción de la imagen](/images/git_rm_cached.png)

## Comando para ver archivos en el staging area
Este comando lista todos los archivos que están en el índice (staging area) y ya están siendo rastreados por Git.

```
git ls-files
```

## git log
Muestra la historia de los commits en el repositorio

```
git log
```
![Descripción de la imagen](/images/git_log.png)


## Configurar git
```
git config --global user.name "<username>"

git config --global user.email "<email>"
```

Lista las configuraciones globales de git
```
git config --global -l
```

Lista la ubicacion del archivo de configuracion de git
```
git config --list --show-origin
```


## tipos de git reset (hard - soft - mixed)
### git reset mixed
Actualiza tu Staging area al commit solicitado
1 - Se muestran los commits
2 - Se muestra el estatus del repositorio
3 - Se muestra el contenido original del archivo a modificar en este caso hello.py
4 - Se muestra el contendio de hello.py en la version o commit que lo queremos dejar
5 - Hacemos el git reset mixed esto hara que solo se vea modificado el archivo en el staging area y no en nuestro Working Directory(WIP)
6 - Mostramos como se ve el estatus de nuestro repositorio
7 - Comprobamos que nuestro archivo hello.py no a sufrido modificacion en el WIP
8 - Para dejar el archivo hello.py tal cual como en nuestro Staging Area ejecutamos el comando git checkout
9 - Comprobamos que ya ha sido modificado nuestro archivo hello.py tal cual como esta en el staging area
 
![Descripción de la imagen](/images/git_reset_mixed_001.png)



## git alias
Son shortcuts 
```
git config --global alias.<nombre-alias> "<comando>"
git config --global alias.mihistorial "git log --oneline"
```

## git cat-file -p <hash-commit>
Sirve para ver el contenido de un commit
```
git cat-file -p <hash-commit>
```
![Descripción de la imagen](/images/git_cat-file.png)


## markdown cheatsheet
[link markdown sheet](https://github.com/adam-p/markdown-here/wiki/markdown-cheatsheet)

## Donde se encuentra el archivo .ssh en windows o ubuntu
C:\Users\<nombre de usuario>\.ssh

/home/nombre_de_usuario/.ssh/
/home/v1k1ngg0d/.ssh
ls -al ~/.ssh

![private key and pucblic key](/images/git%20ssh%20file.png)


## Modificar el mensaje del ultimo commit
```
git commit --amend -m "<message>"
```

## reflog
Este comando te muestra TODO el historial de lo que has hecho en tu repositorio

## merge
Haremos merge de dev1 a master branch

![private key and pucblic key](/images/git_merge_1.png)

Hacemos el merge de dev1 en master y se muestra asi nuestro log

![private key and pucblic key](/images/git_merge_2.png)
Lo que muestra la imagen es que en ocasiones hay muchos commits sin sentido o se hace muy extenso el historial de la rama master de commits basura y sera dificil al momento de administrar la rama master una alternativa para evitar esto es hacer un "squash merge"

## git squash merge
![private key and pucblic key](/images/git_merge_squash.png)







## linux
### cat
Comando para editar un archivo

```
cat >> <filename>
```
Para salir das un  ENTER y en una nueva linea presionas CONTROL + D


### touch
Comando para crear archivos
```
touch <filename>.<extension>...
```

### history
Muestra todo el historial de los comandos que has ejecutado
```
history
```

### copiar el conteniddo de una carpeta en otra
```
cp -r <carpeta a copiar>/ <carpeta destino>/  
```

# avance
9 21:47


## temas a estudiar a profundidad 
- reflog(reachable commits and orphaned commits)



## notas
cd /mnt/c/Users/odina/Documents/odin/programacion/git/mastering-git-github-from-basics-to-advanced-workflows





