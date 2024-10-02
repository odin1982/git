/c/Users/odina/Documents/odin/programacion/git/ejercicios-de-practica/MyFirstNovel
# git
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



### commands
git config --global user.name                           informa el nombre de usuario de git
git config --global user.name "odin"                    setea tu nombre de ususario en git
git config --global user.email                          informa el email que git tiene configurado
git config --global user.email odin@gmail.com           setea el email para git
git status                                              da información del repositorio y su contenido
git init                                                crea un repositorio git nuevo
git add [file1]  [file2]                                Agrega archivos al Staging Area
git add .                                               agrega todos los archivos
git commit -m "[message text]"                          crea un commmit o una photo en ese instante del repositorio
git log                                                 muestra todos los commits del repo
git log --abbrev-commit                                 te muestra los commits con el hash abreviado
git log --oneline                                       te muestra los commits abreviados
