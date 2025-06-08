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



