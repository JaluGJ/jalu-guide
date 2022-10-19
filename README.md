    (si descargaste esto, te recomiendo que lo abras con el preview de VSCode)

# JALU-GUIA DE GITHUB PARA UN PF ORDENADO 

Hola! Este md es una guía practica para las configuraciones rapidas y simples de github junto a comandos, para poder hacer el pf en herny y muchos de estos comandos los utilizaras en el futuro en tu trabajo.

REITERO, ES UNA GUIA SIMPLE, SE PUEDEN HACER COSAS MAS COMPLEJAS Y TAMBIEN ELEVAR EL NIVEL DE SEGURIDAD. PERO POR AHORA, VAMOS A LOS SIMPLE.

 ## Crear el repositorio 

 ---

>_Uno de lo miembros del grupo deberá crear el repositorio de _github_ en donde estará alojado el repositorio._

Entra a github.com y, al lado del menu de su usuario (donde aparece su foto en un pequeño circulo) tienen un simbolo  **"+"** al clickear, ven la opcion de __"new repository"__ el cual los dirije directamente para crear un nuevo repositorio. Le dan un nombre al repositorio. Les recomiendo fuertemente que le den el nombre que va a tener su proyecto, y no "PF-Henry-XX".

Luego conservan la selección de que sea "public" y **no** añadan ni README file ni .gitignore aun. Esto es para que github les permita  les de los pasos para hacer la clonacion y preparar el repositorio. 

Una vez dado el nombre, le dan a la opcion de "create repositoy" y luego, el dueño del respositorio sigue los pasos indicados para crear el repositorio. Y si, hacer todos los pasos de la primer opcion, desde el comando `echo "# XXX" >> README.md` hasta el ultimo comando `git push -u origin main`

## Añadir miembros _colaboradores_ al repositorio

---

>_Es hora de añadir al equipo de trabajo al repo._

Una vez creado el repo con el nombre del proyecto, deberá dar acceso a modificaciones a sus otros compañeros, para ello, el creador del repo debe ir a la seccion `settings` (o configuración), y a la opcion "collaborators" o "colaboradores"

Tendran a la vista, un boton verde en el que se lee "Add people", al hacerle click, les aparecerá un modal en el cual les pide el ***nombre de usuario, el nombre completo o el email*** de las personas que seran colaboradores del proyecto.

En este momento, piden los usuarios de el equipo, y añaden a los colaboradores.

>A los colaboradores les llegara un mail de invitacion para acceder a modificar el repo

Una vez finalizado este paso, es hora de crear las protecciones y las ramas

## Crear Ramas y Protegerlas

---

>_Un buen control sobre las ramas permitira que haya paz en el equipo._

Ya el repositorio esta creado y estan añadidos todos los colaboradores. Si seguiste correctamente los pasos anteriores, tu repositorio debería estar ubicado sobre una rama llamada `main` y ya no debería existir una rama llamada `master`. 
>Si aun tienes una rama llamada master, te recomiendo que hagas los pasos que te indica github para subir un repo ( es decir, la parte de comandos que van desde `echo...` hasta el `git push...`)

### **Crear Rama**

Bien, existen 2 maneras de crear ramas, por `comandos` y a traves de la pagina de `github` en el mismo repo.

>Opcion 1: `Github`
>>+ Hay una barra que dice `<> Code` `⊙ Issues` ... En esta barra, le das a code (si es que no estas en ella ya) y le das a donde dice `branch`, que esta pegadito al lado del cuadrado más claro que dice `main` 
>>+ Una vez adentro, vas a ver la opcion `New Branch` en un cuadrado verde y le haras click. 
>>+ Tras hacerle click aparecerá un modal con un espacio tipo input donde colocar el nombre de la nueva rama. Podran observar que, por encima de ese espacio dice `Branch name`, que significa, nombre de la rama.
>>+ El nombre de la rama deberá ser `dev` (pueden ponerle _development, developer, desarrollo_ o el nombre que ustedes prefieran que tenga que ver con desarrollo, porque en esta rama trabajaran, y deployaran sobre main mas adelante)
>>+ Le dan a la opcion `Create Branch` y *Voilà* lista la rama

>Opcion 2: `comandos`
>+ En la consola de VSCode, (o la que utilicen), desde la carpeta donde tienen el repositorio van a hacer los siguientes comandos
>
>       git branch dev
>       git push -u origin dev
>
>+ Si vuelves a tu github, podras ver, selecionando donde dice `main`, que la rama ya está creada  

### **Proteger Rama**

Ahora, ve nuevamente a la opcion ` ⚙ Settings` y podras ver que en la barra lateral, hay una opcion que dice `Branches` (o _Ramas_). Ve a esa opcion y aqui haremos la proteccion de ramas y tambien cambiaremos cual es la rama default del proyecto (para hacer las cosas más faciles) 

>+ Vamos a cambiar la rama por defecto
>>1. Al final del recuadro donde dice `main` deberías tener un icono con dos flechas, una apuntando hacia la derecha y otra a la izquierda <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-arrow-switch">
    <path d="M5.22 14.78a.75.75 0 001.06-1.06L4.56 12h8.69a.75.75 0 000-1.5H4.56l1.72-1.72a.75.75 0 00-1.06-1.06l-3 3a.75.75 0 000 1.06l3 3zm5.56-6.5a.75.75 0 11-1.06-1.06l1.72-1.72H2.75a.75.75 0 010-1.5h8.69L9.72 2.28a.75.75 0 011.06-1.06l3 3a.75.75 0 010 1.06l-3 3z"></path>
</svg> (algo asi). Hazle click
>>2. Te aparecera un pequeño modal que te permitira cambiar las ramas. Cliquea donde dice `main`, y selecciona la rama `dev`.
>>3. Le das al recuadro que dice `update` y luego al recuadro de `I understand, update...`
>+ Veras que `main` cambio a `dev`

Vamos a proteger las ramas `main` y `dev`

A lo que se refiere proteger las ramas, es que esas ramas no puedan ser sobreescritas en el repositorio, hasta no tener los permisos y autorizaciones de otras personas del equipo, para así no borrar el trabajo que haya hecho otro.

Los siguientes son los pasos necesarios para proteger una rama (esto deben hacerlo con cada rama que quieran proteger, por separado)
>1. Cliquean el boton que dice `Add rule`
>2. Completan el campo obligatorio que es el nombre de la rama a proteger (`main` o `dev`)
>3. Dentro de las opciones, seleccionan `Require a pull request before mergin` y veran que ya queda seleccionada la opcion __Require approvals__. 
>4. Debajo de la opción require approvals, veran un recuadro que dice __required number of approvals before merging__ en el cual deben definir la cantidad de personas que deben aprobar sus cambios al repo, antes de cambiarlo efectivamente. Mi recomendación es que sean 2 para `main` y 1 para `dev`
>5. Van al final de la pagina y le dan al boton verde que dice `Create`

Y listo, ya tienen protegidas las rutas.


## (Biblia de comandos para trabajar)
    1. git checkout dev // ir a dev (antes de empezar a trabajar)
    2. git pull origin dev // traer los cambios desde el remoto(antes de empezar a trabajar)
    3. git checkout -b (nombre de la rama) // para crear e ir a esa rama.  
    (la rama solo de  la tarea. no poner nada que no fuera lo de la rama)(antes de empezar a trabajar)"UserModel"
    4. git push -u origin (nombre de la rama) // primer push para crear la rama en el remoto (este push se puede omitir)(antes de empezar a trabajar)"UserModel"

    --- RECIEN AHORA PUEDE EMPEZAR A TRABAJAR EN EL CODIGO ---
    --- UNA VEZ TERMINAN DE TRABAJAR, HACEN LO QUE SIGUE ---

    git add . (o, mejor dicho, todos los archivos que van al commit)
    git commit -m "bla, bla" 

    ("ADD / userModel "
    "FIX / userModel"
    "BUG/ UserModel"
    "ADD / UserRoute, getUsers Create)

    git checkout dev
    git pull origin dev (esto se hace siempre, por si alguien hizo cambios mientras trabajabas)
    git checkout (nombre de la rama en que se trabajo) "UserModel"
    git merge dev (ver si aparecen conflictos, si aparecen solucionarlos)
    (si hay conflictos, resolverlos. y volver a hacer un commit)
    git push

    Hacer el pull request en github
    (visual te tira un Link.... el link largo... con ctrl + click, vas a la direccion y ahi te da para hacer el pull request)
//////////////////////////////////////////////////////////////////////////////////////////////////////