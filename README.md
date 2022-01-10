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
