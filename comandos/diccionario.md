# Mi pequeño diccionario de codigo/comandos

## Git

|Comando|Funcionalidad/Definicion|
|---|---|
|`git branch --list`| Muestra una lista de las ramas existentes |
|`git branch` [nombre]| Crea una nueva rama con el ***[nombre]*** indicado |
|`git branch -m/-M`  [nombre]| Renombra a la rama en la que estas parado, y reemplaza el nombre con lo que este en ***[nombre]*** |
|`git branch -d/-D`  [nombre]| Borra la rama indicada en ***[nombre]***|
|`git checkout`| Mostrara una lista con aquellos archivos no subidos a la rama en la que estas ubicado |
|`git checkout` [nombre] | Te posicionará en la rama indicada en ***[nombre]*** |
|`git checkout -b` [nombre]| Creará una rama nueva llamada ***[nombre]*** a partir de en donde estás parado, y te posicionará en la nueva rama |
|`git clone` [url] | clona un repositorio remoto ubicado en la ***[url]*** |
|`git init`| Crea un repositorio Git vacío o reinicializa uno existente |
|`git log`| Muestra todos los commits hechos hasta el momento |
|`git merge` [nombre]| Trae los archivos en la rama ***[nombre]*** y los mezcla con la rama en la que estas ubicado actualmente |
|`git pull` | Traerá todos los cambios que esten conectados a un repositorio, incluyendo ramas creadas, archivos nuevos, y cualquier cambio hecho, sobre la rama en la que estes ubicado |
|`git pull origin` [nombre]| Traerá solo los cambios efectuados en el origen, en la rama especificada en ***[nombre]*** |
|`git push`| Actualiza un repositorio remoto con los ultimos cambios generados |
|`git push origin` [nombre]| Actualiza la rama ***[nombre]*** un repositorio remoto con los ultimos cambios generados en esa rama |
|`git push -u origin` [nombre] | Sube la rama ***[nombre]*** al re |
|`git remote`| Podras ver una lista con los nombre a los distintos repositorios remotos creados con el comando `git remote add` _[nombre]_ [url repo] |
|`git remote rename` [nombre viejo] [nombre nuevo] | Cambia el nombre de la referencia de repositorio remoto ***[nombre viejo]*** por ***[nombre nuevo]*** |
|`git remote remove` [nombre]| Borra la conexion remota al repositorio con referencia ***[nombre]*** |
|`git remote set-url` [nombre] [newURL] [oldURL]| Reemplaza la ***[oldURL]*** (url vieja) por ***[newURL]*** (url nueva) en la conexion remota llamada ***[nombre]*** |
|`git remote add` _[nombre]_ [url repo]| Conecta tu instancia de Git con un el repositorio remoto ubicado en ***[url repo]*** y la referencia es ***[nombre]*** |
|`git stash`| Reserva los cambios en un directorio "sucio" aparte (recomiendo investigar) |
|`gitk`| El navegador de repositorio de Git |
|``|  |

## npm

| Comando | Función |
|---|---|
|`npm -v`| Devuelve la version de NPM instalada en tu computadora |
|`npm init`| Inicia, en la carpeta que se encuentra, una instancia de npm, creando un archivo package-json, listo para instalarle dependencias|
|`npm i` [paquete]| Instala la libreria especificada en ***[paquete]***  |
|`npx`| herramienta para ejecutar paquetes |
|`npx create-react-app` [nombre]| ejecutará el paquete de React y creara la carpeta ***[nombre]***|
 
## Node

| Comando | Función |
| --- | --- |
|`node -v`| Devuelve la version de Node instalada en tu computadora |
|`node` [nombre].js | ejecutara el archivo que coincida con ese nombre sobre la carpeta en donde este ubicado, con node |
|``|  |

## Bash

| Comando | Función |
| --- | --- |
|`ls`| Muestra los archivo de la carpeta en donde estes ubicado |
|`ls -a`| Muestra ***TODOS*** los archivos en la carpeta donde estes ubicado (incluye ocultos) |
|`pwd`| Muestra la direccion de la carpeta donde estes ubicado |
|`date`| Muestra la fecha y hora actual |
|`clear`| Limpia la consola de todos los comandos ejecutados |
|`mkdir` [nombre]| Crea un nuevo directorio (carpeta) en donde estes ubicado con el ***[nombre]*** indicado |
|`rm` [nombre] | Elimina el archivo ***[nombre]*** que se encuentre donde estes ubicado |
|`rm -f` [nombre] | Elimina el archivo ***[nombre]*** de forma forzada, en caso que no pueda hacerlo |
|`head` [nombre] | Muestra las primeras 10 lineas del archivo ***[nombre]*** |
|`tail` [nombre] | Muestra las ultimas 10 lineas del archivo ***[nombre]*** |
|`mv` [direccion origen] [direccion final] | Mueven el archivo/carpeta que se indique en ***[dirección origen]*** hacia la carpeta ***[dirección final]*** |
|``|  |