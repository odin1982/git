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

## Quitar error CRLF
```
git config core.autocrlf true
```

## Branch
Es una línea de tiempo de commits

            commit inicial   README.md
Master -----*---------------*--------------
                            |
                     Branch  --------------

## Merge 
Fast Forward            - Cambio transparente sin conflictos
Uniones Automaticas     
Union Manual            - git no puede resolver de forma automatica

## Tags - Etiquetas
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


## Stash
Boveda segura donde se pueden mover todos los cambios, no se recomienda realizar stash.


## Rebase
Permite unir commit separar commits hacer squash renombrar nombres de los commits, se recomienda que se haga local y que no haya impactado en un repositorio remoto.



