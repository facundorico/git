# Comandos GIT

git --version //Nos da la version de git en consola

// -- viene palabra completa / - viene abreviatura

// archivo .gitkeep se crea en un lugar donde quiero que el folder este aunque sea vacio, ej: upload

git help // ayuda de git

git config --global user.name "Juan Perez" // nombre de configuracion global

git config --global user.email "juanperez@gmail.com" // email de configuracion global

git config --global -e // ver config, editar, agregar, etc

git init // Inicializa el repositorio

git status // Info de commits

git add name.js // agrega el archivo al stage

git add . // agrega todos los archivos al stage

git reset name.js // Saca archvio del stage

git commit -m "mensaje" // Commit con mensaje

git log // muestra los logs

git checkout -- . // reconstruir proyecto a como estaba el ultimo commit

git branch // Indica en que rama estamos trabajando

git branch -m master main // cambia el nombre de la rama de master a main

git config --global init.defaultBranch main // queda en default global que el branch inicial es main y no master

git commit -am "Readme updated" // Add y commit con mensaje en la misma linea (el archivo debe tener seguimiento)

git add \*.html // Add de todos los archivos con esa extención

git add js/\*.js // Add de todos los archivos js especificando directorio

git add css/ // Add de todo lo que tiene la carpeta css

git status --short // Muestra el status de forma reducida

git config --global alias.s "status --short" // Crea un alias de git status --short llamado simplemente con git s

git log --oneline // git log en una linea con hash corto

git log --oneline --decorate --all --graph // gil loc corto con grafico de branches y decorado

git diff // Listo por consola las diferencias o cambios de un archivo

git diff --staged // Diferencias en staged

git commit --amend -m "Mensaje" // Enmienda el mensaje del ultimo commit

git reset --soft HEAD^ // Reset al commit anterior a HEAD, si uso HEAD^2 es 2 commit antes, y asi sucesivamente

git reset --mixed 7ec9f95 // Reset parecido al soft pero sacando del stage

git reset --hard 7ec9f9 // Borra los cambios subsiguientes al commit, reset destructivo

git reflog // Referencia cronologica de todo lo que paso en GIT

git mv destruir-mundo.md salvar-mundo.md // Remover del mismo directorio al mismo (renombrar)

git rm salvar-mundo.md // Remueve el archivo nombrado

## Git Ignore

.gitignore // Archivo de raiz que contiene todos los archivos a los que no hay que darle seguimiento

## Branches

git branch // Lista todas las ramas locales

git branch -a // Lista todas las ramas

git branch -r // Lista todas las ramas remotas

git branch -m nuevarama nuevonombrerama // Cambia el nombre de la rama

git branch -d // Elimina la rama

git branch -h // Help de ramas

git checkout -b nombre_del_branch origin/nombre_del_branch // Creamos un nuevo branch localmente, basados en el branch remoto

git remote update origin --prune // Actualiza todas las ramas remotas para ver en local y remoto

git branch rama-villanos // Crea una nueva rama llamada "rama-villanos"

git checkout rama-villanos // Nos movemos a la rama-villanos

git merge rama-villanos // Mergea la rama-villanos sobre la que estoy parado (en este caso estoy parado en master)

git branch -d rama-villanos // Borra la rama-villanos

git branch -d rama-villanos -f // Borra la rama-villanos forzando

git checkout -b rama-villanos // Creamos la rama-villanos y nos movemos a ella

git remote update origin --prune // Actualiza todas las ramas remotas para ver en local y remoto

## Tags

git tag // Lista los releases

git tag super-release // Crea un tag con el nombre super-release para esa versión

git tag -d super-release // Borra el tag

git tag -a v1.0.0 -m "Version 1.0.0 lista" // Crea el tag con anotacion y mensaje

git tag -a v0.1.0 e51ee53 -m "Version Alpha de nuestra app" // Crea el tag para una version especifica pasandole el HASH

git show v0.1.0 // Muestra info del tag especificado

## Stashes

git stash // Genera un stash de lo cambiado en el momento que lo ejecuté

git stash list // Lista todos los stashs guardados

git stash pop // Toma el ultimo stash, lo borra y lo pone en progreso junto con los cambios que realize despues

git stash clear // Borra todos los stash en el branch

git stash apply stash@{2} // Trae el stash del hashcode nombrado

git stash drop stash@{2} // Borra el stash del hashcode nombrado

git stash show stash@{2} // Muestra cambios en el stash del hashcode nombrado

git stash save "Agregamos feature ABC" // Agrega el stash con la info del mensaje

git stash list --stat // Muestra mas informacion de cada uno de los stashes generados

## Atajos mas usados

git checkout -b nuevarama // Creo rama y me muevo a ella en un solo comando

git commit -m "feat:new funcionality" // Commit con mensaje

git push origin nombrederama // Pusheo donde estoy parado hacia la rama remota nombrederama

git pull origin master // Traigo los cambios de master a mi origin local

git clone https://nombredelrepo.git // Clono el repo git