# Exploring GIT internals: Understanding Areas and Workflow
##### Working Area(wip / working in progress)
    Area donde se encuentran los archivos en la unidad de almacenamiento, donde se esta trabajando

##### Staging Area
    Esta area nos sirve para darle seguimiento a nuestros archivos, si trabajaramos unicamente en el working area cualquier modificacion GIT no lo tendria a la vista.

## git init
    Instruccion para crear un repositorio git

```
> git init
```    
![Descripción de la imagen](/images/git_init.png)

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



## Como puedo remover un archivo del area de commit?





## linux
### cat
Comando para editar un archivo

```
cat >> <filename>
```
Para salir das un  ENTER y en una nueva linea presionas CONTROL + D



##notas
cd /mnt/c/Users/odina/Documents/odin/programacion/git/mastering-git-github-from-basics-to-advanced-workflows





