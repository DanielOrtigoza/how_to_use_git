## Configuración inicial de Git

Esto consiste en establecer su nombre y correo electrónico, ya que cada `commit` que se realice usará esta información para identificarlo como autor.

Desde `Git Bash` o `terminal`, ejecute los siguientes comandos:

```
$ git config --global user.name "su_nombre"
$ git config --global user.email su_correo@example.com
```

La opción `--global` permite que esta configuración sólo sea necesaria una vez, de ahí en adelante Git la usará para todo lo que se haga en el equipo.

En caso de necesitar cambiar dicha información para un proyecto específico, ubíquese en la carpeta correspondiente y ejecute los comandos sin la opción `--global`

Compruebe la configuración realizada, ejecutando el comando:

```
$ git config --list
```

## Comando básicos de Git

`git init` comando para crear un repositorio 

`ls -a`comando para mostrar todos los archivos de una carpeta (incluidos los archivos ocultos) 

`git status`comando para ver el estado del repositorio  

`git add .`comando para agregar archivos al área de preparación (previo a hacer el commit)  

En caso de que salga el error

```jsx
warning: could not open directory 'git_practice_basic_concepts-master/basics_concepts/git_practice_basic_concepts/recetas/Colombia/': Filename too long
error: open("git_practice_basic_concepts-master/basics_concepts/git_practice_basic_concepts/imagenes/ajiaco.jpg"): Filename too long
error: unable to index file 'git_practice_basic_concepts-master/basics_concepts/git_practice_basic_concepts/imagenes/ajiaco.jpg'
fatal: adding files failed
```

`git config --system core.longpaths true`desde un cmd como administrador, correr el siguiente comando 

`git commit -m "mensaje de lo que se está haciendo”`comando para realizar un commit 

`git log`comando para ver los cambios realizados 

en caso de usar el comando `git lop -p` la forma de salir de ahí es presionando la letra `q`

`git diff [id_commit_1]..[id_commit_2]` comando para mirar las diferencias entre dos commits  

`git checkout [id_commit]` comando para volver a una versión anterior  

`git switch -` comando para salir del checkout anterior y volver a la rama principal 

`git clone [url de github]` comando para clonar un repositorio de GitHub en base al url web 

`git remote -v` comando para ver la conexión con el repositorio remoto

`git remote rename origin [nuevo nombre del repositorio]` comando para renombrar un repositorio remoto

`git push -u [nombre de la rama origen] [nombre de la rama]` comando para mandar cambios de local al repositorio remot, i.e. `git push -u origin master`

### Comandos para restaurar una versión anterior

`git reset --hard [id_commit]` comando para volver a esa versión del repo usando el id del commit  

despues de hacer esto, la forma de mandar estos cambios al repo remoto es:

`git push -f [nombre de la rama origen] [nombre de la rama]`

`git pull` comando para actualizar el repositorio local con todo lo del repositorio remoto

`git branch [nombre de la rama a crear]` comando para crear una rama

`git branch -a` comando para ver las ramas existentes en el repositorio

`git branch --vv` comando para ver las ramas asociadas al repositorio local y al remoto

`git checkout [nombre de la rama a cambiar]` comando para cambiar de una rama a otra

`git push --set-upstream origin [nombre de la rama]` comando para hacer un push desde local al repositorio remoto y publicar la rama en el repositorio remoto

`git tag -a [nombre de la etiqueta a crear] -m “Mensaje”` comando para crear una etiqueta

`git tag` comando para ver la lista de todas las etiquetas del repositorio

`git show [nombre de la etiqueta]` comando para ver la etiqueta

`git tag -d [nombre de la etiqueta a crear]` comando para eliminar una etiqueta 

comandos para comparar dos ramas, cada uno muestra información diferente

`git diff --name-status [nombre de la rama 1]..[nombre de la rama 2]` 

`git diff --stat [nombre de la rama 1]..[nombre de la rama 2]` 

`git diff [nombre de la rama 1]..[nombre de la rama 2]` 

comando para fusionar dos ramas, primero me paro en la rama que voy a fusionar

`git checkout [rama principal a la cual quiero fusionar cambios realizados en otra rama]`

`git merge [rama secundaria con cambios que quiero traer a la rama principal]` 

`git branch --no--merged` comando para ver las ramas que no están merged con la rama en la que estoy parado 

`git branch --merged`