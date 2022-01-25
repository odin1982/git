# git

## REPOSITORIO CENTRAL
Es cuando los desarrolladores trabajan directamente en un servidor

                        <--    Desarrollador_1
Repositorio Central     <--    Desarrollador_2
                        <--    Desarrollador_3


## REPOSITORIO DISTRIBUIDO
Es cuando cada desarrollador tiene su propia copia del repositorio


                            <--    Desarrollador_1 (Respositorio Propio)
Repositorio Distribuido     <--    Desarrollador_2 (Respositorio Propio)
                            <--    Desarrollador_3 (Respositorio Propio)

## --
El -- significa que en la instrucción va  a venir una palabra completa. 


## .git
Carpeta donde git le da seguimiento a tu repositorio


## .gitkeep
Le indicas a Git que le de seguimiento a esa carpeta aunque no tenga archivos o este vacia
El archivo .gitkeep es solo un archivo dummy para permitir que una carpeta vacía (excepto por ese archivo) se cree al clonar el repositorio, ya que las carpetas vacías no forman parte del control de versiones.


## HEAD
El HEAD siempre apunta al ultimo commit
HEAD^   - el techo significa el commit anterior antes del HEAD
HEAD^[numero-commits-anteriores]
HEAD^2  - dos commits anteriores  


## git reset
se usa mucho para viajes en el tiempo


## ERROR CRLF
```
git config core.autocrlf true
```

## BRANCH
Es una línea de tiempo de commits

            commit inicial   README.md
Master -----*---------------*--------------
                            |
                     Branch  --------------


## MERGE
Fast Forward            - Cambio transparente sin conflictos
Uniones Automaticas     
Union Manual            - git no puede resolver de forma automatica


## TAGS - ETIQUETAS
Son una referencia a un commit especifico
       
Master * -------------------------- * -------------------------- * ---------------------------- * --------
     Inicio                      Unimos                       Adiciones                    Creamos    
     Proyecto                   Trabajos                                                el ejecutable
                                   
                                   |                                                            |
                            version_1.0.0                                                   version_1.0.1


- Sirven para marcar versiones o releases
- Pueden ser palabras numeros

v1.0.0
1 = version mayor
0 = cierta funcionalidad pero no es una version mayor
0 = bug fix


## STASH
Boveda segura donde se pueden mover todos los cambios, no se recomienda realizar stash.


## REBASE
Permite unir commit separar commits hacer squash renombrar nombres de los commits, se recomienda que se haga local y que no haya impactado en un repositorio remoto.

Escenario: se tiene la rama MASTER, despues creamos un nuevo branch a ese nuevo branch se le hacen dos commits, pero en el master otra persona hace cambios a la rama master y son necesarios en la segunda rama Misiones Completadas, como le hariamos para actualizar la rama misiones completadas?

                                   |             |
                                   |             |
                      Más misiones *             * Mision 2 lista
                                   |             |
                      Más heroes   *             * Mision 1 lista
                                   |             |
                      Lista        *--------------      Rama misiones completadas
                                   |
                      Nuevo plan   *
                                   Master


Necesitamos hacer un rebase.

Lo que hariamos seria lo siguiente:
- git checkout rama-misiones
- git rebase master


                                   |                * Mision 2 lista
                                   |                |    
                                   |                * Mision 1 lista
                                   |                |    
                                   |----------------             
                                   |             
                      Más misiones *             
                                   |             
                      Más heroes   *             
                                   |             
                      Lista        *
                                   |
                      Nuevo plan   *
                                   Master

Para que sirve un rebase?
- Ordenar commits
- Corregir mensajes de los commits
- Unir commits
- Separar commits
- issues, wikis, estadisticas ilimitadas
- organiaciones ilimitadas
- participación gratutita en proyectos privados.



## GITHUB
Es una plataforma de desarrollo colaborativo de software para alojar proyectos.
- Repositorios ilimitados
- Paginas HTML,CSS y JS ilimitadas
- push, pull, clones ilimitados



Repositorio remoto
                                                               <- pull Person 1
Repositorio Local    -> push   ->     repositorio remoto
                                                               <- pull Person 2

Hosted Services:
- Bitbucket
- Github


Manejados por nosotros mismos:
- Gitosis


git remote add origin https://hithub.com/Klerith/udemy-heroes.git

- add: nuevo remote
- origin: el nombre de nuestro remote
- https://hithub.com/Klerith/udemy-heroes.git: dirección de Github



## PULL REQUEST
Hacer cambios en un repositorio que no nos pertenece
Una rama rama que se desprendio en un punto del tiempo de la rama principal y luego cuando quieres unir la rama atraves de un pull request, la idea del pull request no es solo hacer el merge y ya, si no el pull request es un analisis previo  de una persona que revisara que el merge se hizo correctamente


## MARKDOWN

tutoriales:
https://www.markdowntutorial.com/
https://www.webfx.com/tools/emoji-cheat-sheet/



## GIT FETCH
te muestra los cambios que existen antes de hacer un PULL


## FORK, CLONE Y COLABORACIONES
### FORK

Tomar el repositorio original y clonarlo a un lugar donde nosotros tenemos total acceso a ese repositorio

repositorio
publico en GITHUB         ------- FORK -------    mi-usuario/maps                             
google/maps                                       push,clone,commits, total acceso



### FLUJO DE TRABAJO

|             |   |
|             |   |
|             |   |
|             |   |
|             |   |
|             |   |
|             |   |
|             |   |
|             |   |
|             |   |
*-------------|   |
|  feature 2      |
|                 |
*-----------------|
|        feature_1 
|
master

Como ir a una rama
git fetch
git branch -a
git checkout [branch-name]

Como subir tus cambios
git checkout master
git merge [rama-que se le va hacer merge]
git push

cambios pull request
git push origin [rama]
- hacer pull request 

