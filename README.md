# GIT
## git basics
### getting a git repository
Existen dos formas:
- generar un repositorio de git en tu PC
- clonando un repositorio

### Removing files

caso 1: Borrandolo directamente
Al borrarlo directamente, tendras que ejecutar la instrucción git add para subir al staging area la eliminación del archivo

>rm <nombre-archivo>
>git add <nombre-archivo>
>git commit -m "Se elimina archivo <nombre-archivo>"

caso 2: Borrandolo con git rm <nombre-archivo>

>git rm <nombre-archivo>
>git commit -m "Se elimina archivo <nombre-archivo>" 

### git fetch vs git pull
La diferencia es que git fetch trae todos los cambios que no tienes pero no les hace merge y git pull si les hace merge


hola

avance: Private Small Team <166> page 166
