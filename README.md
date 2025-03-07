# git
Sistema de control de versiones

Existen dos sistemas de versiones:
* centralizado
* distribuido

## Sistema de versiones centralizado
Todos los desarrolladores se conectan a una misma maquina para almacenar el codigo, una de las desventajas es que si el servidor deja de funcionar nadie va  apoder realizar cambios.

Un ejemplo seria subversion

## Sistema de versiones distribuido
Todos los desarrolladores cuentan con el historial del proyecto y si quieren sincronizar sus cambios lo pueden hacer sin necesidad de un servidor, y si el servidor deja de funcionar los desarrolladores pueden seguir trabajando.

## Configuracion de GIT
* Sistema
* Global
* Local

Nombre de usuario
Correo
Editor

Para abrir el archivo de configuracion de GIT usar la siguiente instrucción:
```
git config --global -e
```

## Navegar en los menus de ayuda de GIT
Letra J -> bajar
letra K -> subir
letra Q -> salir

## Eliminando archivos en git
* Con comando del shell o terminal
´´´
> rm <archivo>
> git add
> git commit -m "<mensaje>"
´´´

* Con instruccion de git (te ahorras el git add)
´´´
> rm <archivo>
> git commit -m "<mensaje>"
´´´

## moviendo archivos
En este caso se usa para renombrar el archivo
git mv <archivo1> <archivo2>
git commit -m "<mensaje>"

o la otra puede ser usando el shell pero aqui debes de mandar a staging el archivo eliminado y el archivo creado

mv <archivo1> <archivo2>
git add <archivo1>
git add <archivo2>
git commit -m "<mensaje>"

## sacando archivos de staging
git restore --staged <filename..>
git restore --staged .          --> saca todo de staging

## viendo nuestros cambios
Te muestra los cambios que existen entre lo que ya le hiciste commit y el area de staging
git diff --cached                 

Te muestra los cambios que existen entre tu directorio y el area de staging
git diff

## difftool
Como configurar difftool con VsCode ver video 26

>git difftool                           --> checa diferencias entre staging y directorio
>git difftool --staged                  --> checa diferencias entre repo y staging





## Videos para repasar
Video 24. Ignorando archivos ya agregados
Video 25
video 26



## configuring name git
git config --global user.name                           informa el nombre de usuario de git
git config --global user.name "odin"                    setea tu nombre de ususario en git

## configuring email git
git config --global user.email                          informa el email que git tiene configurado
git config --global user.email odin@gmail.com           setea el email para git

## the very basic of git: adding and commiting
git status                                              da información del repositorio y su contenido
git init                                                crea un repositorio git nuevo

## terminal instructions
touch [fileName.extension] [fileName2.extension]        crea un archivo o varios archivos
start .                                                 abre el explorador en la ubicación donde ejecutaste el comando
open .                                                  [linux-mac] abre el explorador en la ubicación donde ejecutaste el comando
pwd                                                     imprime tu ubicación actual
mkdir [folderName]                                      crea una carpeta
rm   [fileName]                                         elimina un archivo
rm -rf                                                  elimina un folder

## staging changes with git add
working directory -> git add -> staging area -> git commit -> repository
git add [file1]  [file2]                                Agrega archivos al Staging Area 

## git commit command
git commit

## the git log command
git log

## atomic commits
Un commit debe abarcar una caracteristica, mantener tu commit en algo simple, no debes poner todo lo que hiciste en un solo commit

## commit message
debe ser imperativo el mensaje
* make xyz do frotz

## a closer look at the git log command
git log --abbrev-commit             te muestra los commits con el hash abreviado
git log --oneline                   te muestra los commits abreviados

## fixing mistakes with amend
Imagina que hiciste un commit y te diste cuenta que no incluiste un archivo o talvez el mensaje del commit tiene un error,
para solucionar esto esta la instruiccion amend y solo sirve para el ultimo commit

## ignoring files
le podemos decir a git que archivos y carpetas ignorar en un repositorio,para esto se debe de crear un archivo llamado .gitignore
* .DS_Store will ignore files named .DS_Store
* folderName/ will ignore an entire directory
* *.log will ignore any files with the .log extension

## head
es un puntero que te ubica en localizacion actual y branch

## viewing all branches with git branch
git branch                                              muestra todos los branches de tu repositorio

## creating & switching branches
git branch <branch-name>                                crea un nuevo branch

## more practicing with branching
git commit -a -m "<commit-message>"                     Añade todos los archivos a la area de stage y cre commit

## another way of switching
 git checkout <branch-name>                             te cambia a otro repositorio, pero tiene mas fucniones aparte de cambiar de repo

## switching branches with unstaged changes?
si haces un cambio en un branch con un archivo que git le da seguimiento y no haces commit y despues switcheas a otro branch, git no te dejara hacer switch a ese repositorio porque 
tienes cambios sin hacerles commit , si hay un archivo qu enunca le dio seguimiento GIT este si dejara hacer el switch pero se llevara el archivo que no tiene seguimiento.

Error que se muestra al hacer lo anteriormente dicho:
error: Your local changes to the following files would be overwritten by checkout:
        playlist.txt
Please commit your changes or stash them before you switch branches.
Aborting

# deleting & renaming branches
Se debe estar colocado en un branch diferente para poder borrar el branch deseado
git branch -d <branch-name>                             borra un branch
git brnach -D <branch-name>                             forza git a borrar un branch
git branch -m <new-branch-name>                         renombra tu branch, debes estar en el branch a modificar

# how git stores HEAD & branches
Head es simplemente un puntero que refiere a la ubicación actual de un repositorio y apunta al ultimo commit del branch en el que te encuentras

## git stash
git stash is useful command that helps you save changes that you are not yet ready to commit. You can stash changes and then come back to them later.

Running git stash will take all uncommitted changes( stages and unstaged) and stash them, reverting the changes in your working copy.

Use git stash pop to remove the most recently stashed changes in your stash and re-apply them to your working copy

# git restore
Este comando se usa para deshacer cambios igual que git checkout HEAD pero git checkout hace muchas
cosas y no es un comando que haga algo en especifico y en ocasiones es confuso

# unstaging files with restore
If you have accidentally added a file to your staging area with add and you don't wish to include in the next commit, you can use "git restore" to remove 
it from staging.

Use the --staged option like this:
git restore --staged <file>


# git reset
Suppose you've just made a couple of commits on the master branch, but you actually meant to make them on a separate branch instead. To undo those commits, you can use git reset.

git reset <commit-hash> will reset the repo back to a specific commit.The commits are gone.

Lo primero que pasa es que solo te eliminara los commits pero los cambios que hiciste seguiran ahi, en el curso lo que hacen es crear una nueva rama hacerle commit y regresar a la rama y se restablecen los cambios.

# reset --hard
If you want to undo both the commits and the actual changes in your files, you can use --hard option.

for example, git reset --hard HEAD~1 will delete the last commit and associated changes.

# git revert

git revert is similar to git reset in that they both undo changes, but they accomplish it in different ways.

git reset actually moves the branch pointer backwards, eliminating commits

git revert instead CREATES a new commit which reverses/undos the changes from a comit. because it results in a new commit, you will be promoted to enter a commit message, 

Se sugiere usar git revert cuando estas colaborando con varios compañeros ya que no elimina commits.

# GITHUB the basics
## cloning
get a local copy of an existing repository

> git clone <url>

## what does "git push -u" mean
-u es como un link de coneccion de nuestro branch local con el branch remoto de github

git push -u <remote> <local-branch> = git push --set-upstream <remote> <local-branch>

## fetching and pulling
### remote branches
git branch -r

Cuando tu clonas un repo solo estas conectado con el repositorio remoto master
WORKSPACE                       REMOTE
master          ----->          origin/master
                                origin/puppies


## git fetch
fetching nos permite bajar cambios de un repositorio remoto, PERO, esos cambios no estaran integrados automaticamente dentro de nuestros archivos de trabajo

te permite ver que han estado trabajando otras personas, sin hacer merge de esos cambios en tu repositorio local

obten la ultimo del repo pero no estropes mi directorio de trabajo

git checkout fetch_HEAD
git switch -c nueva-rama


## git pull
git pull = git fetch + git mere


## github gists
Son una simple forma de compartir utiles fragmentos de codigo con otros


# Rebasing(Este tema no me quedo claro)
There are two main ways to use the GIT REBASE command:
- as an alternative to merging
- as a cleanup tool:
        sometimes we want to rewrite,delete,rename, or even reorder commits

# REFLOGS
Historial detallado de todas las acciones realizadas en un repositorio

# GIT ALIAS
Global Git Config
ubicacion:
~/.config/git/config

Ubicacion del archivo gitconfig:
> nano ~/.gitconfig 

Ejemplo: Se agregara el siguiente comando como alias
´´´
git log --oneline --graph
´´´
agregar esta instruccion:
´´´
git config --global alias.gl "log --oneline --graph"
´´´

## Encontrando el autor de una linea (git blame)
Te muestra linea por linea quien lo modifico

´´´
git blame <filename>
´´´

´´´
4d9b8c88 (Nicolas Schurmann 2023-10-02 11:56:26 +1300  1) FUNCIONALIDADES
´´´

Muestra linea por linea quien modifico el archivo, con la diferencia de que muestra el correo en lugar del nombre
´´´
git blame -e <filename>
´´´

´´´
4d9b8c88 (<nicolas@holamundo.io> 2023-10-02 11:56:26 +1300  1) FUNCIONALIDADES
´´´

Muestra solo las lineas que le especificas quien modifico el archivo, con la diferencia de que muestra el correo en lugar del nombre

´´´
git blame -e -L 4,8 <filename>
´´´

´´´
e15a3fb9 (<nicolas@holamundo.io> 2023-10-02 11:46:35 +1300 4)
e15a3fb9 (<nicolas@holamundo.io> 2023-10-02 11:46:35 +1300 5) - Listar
e15a3fb9 (<nicolas@holamundo.io> 2023-10-02 11:46:35 +1300 6) - Agregar
a14a3449 (<nicolas@holamundo.io> 2023-10-02 11:48:44 +1300 7) - Marcar como terminada
eccf13ef (<nicolas@holamundo.io> 2023-10-02 11:49:10 +1300 8) - Notificar al usuario sobre la tarea en determinada fecha
´´´

# Etiquetas para versionado
git tag <labelName> <hash-commit>               Crea una etiqueta
git tag                                         Muestra etiquetas
git tag -a <tag> -m "<message>"                 Crea una etiqueta con descripcion
git tag -n                                      Te muestra los tag y su descripcion
git checkout <labelName>                        navegar entre etiquetas o posicionarte donde se encuentra esta etiqueta
git show <labelName>                            muestra el contenido de la etiqueta

# Encontrando bugs con bisect

## Seccion 4: Gestion de ramas
### Que son las ramas?
        Copia de un proyecto sin alterar el proyecto estable

### gestion de ramas





 
