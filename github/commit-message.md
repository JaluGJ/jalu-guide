# Buenas practicas en los mensajes de commits

> - [Índice](#buenas-practicas-en-los-mensajes-de-commits)
>   - [Tipos de cambios](#tipos-de-cambio)
>   - [Donde](#donde)
>   - [Que hiciste](#que-hiciste)
>   - [Ejemplos](#ejemplos-completos)

Una buena practica en los mensajes de commits es que sean informativos, concisos y claros, decir ***QUÉ*** tipo de cambio hiciste, ***DONDE*** lo hiciste y poner ***QUÉ*** cambiaste.  
Un estructura sería `tipo de cambio (donde): que hiciste`

> _Estas buenas practicas pueden variar segur la empresa en la que entren a trabajar_

A continuación les voy a dejar un cuadro de tipos de cambios y que significan

## Tipos de cambio

|Tipo de cambio|Definición|
|---|---|
|*feat*| Agrega algo nuevo, una función o algo |
|*fix*| Arregla una función que fallaba, o un bug |
|*perf*| Mejora de codigo que se reflejan en el rendimiento |
|*refactor*| Refactorizar codigo, como nombre de variables o funciones, o reestructurarlos/modularizarlo |
|*style*| Cambios en el formato, como cantidad de espacios, puntos y como, cosas que no afecten el rendimiento |
|*test*| Se agregan o corrijen tests |
|||

## Donde

El donde hace referencia a la posicion de la carpeta y archivos que hiciste el cambio. Ojo, no es la ruta completa, sino que el comienzo de la ruta y el final. En el siguiente cuadro les doy un par de ejemplos  

|Donde|Explicación|
|---|---|
|(client/navbar)| Es en el frontend (por ello, client) y el archivo que se modifico o se agregó, es el **navbar**. <br> No es necesaria la extension del archivo|
|(client/navbar/index)| En este caso, u otro similar donde sea necesario explcar que el cambio se dio sobre el archivo index, ya que suelen existir varios archivos index.|
|(client/redux/action) | Aqui pueden agregar un lugar más, para dar más especificidad a que archivo fueron a modificar, por si no es suficiente solo decir el archivo final|
|(api/xxx-route)| Es en el backend (por ello, api) y el archivo que se modifico o se agrego es el **xxx-route**. <br> no es necesaria la extension del archivo|
|(api/routes/index)| Al igual que antes, si se va a modificar el archivo index, no es suficiente información, por lo que es necesario especificar la carpeta|
|||


## Que hiciste

Aqui existen muchas sugerencias sobre que escribir especificamente. La convencion mas conocida es las que usa el [framework de Angular](https://github.com/angular/angular/blob/22b96b9/CONTRIBUTING.md#-commit-message-guidelines). Como antes mencionamos, debemos ser concisos y claros, y que mejor que una palabra que defina una acción y comentar cual es el cambio. En resumen, una descripción.  
Es buena practica que: 
1. No este en mayusculas
2. No termine en punto "."
3. No escribirlo en pasado  
Abajo te dejo una listita de palabras clave para estos commits con un ejemplo

|Palabra clave|Definición|Español|Ejemplo|
|---|---|---|---|
|add|Es añadir un archivo, carpeta, funcion, etc|_añadir_| **add new yyy-route** |
|fix|Es corregir y arreglar algo del codigo|_arreglar_| **fix bug on sidebar function** |
|change|Es cambiar algo del codigo, como nombres o estructuras |_cambiar_|**change yyy.name to yyy.fullname on yyy.model**|
|remove|Es eliminar alguna funcion o archivo, etc|_quitar_| **remove auth folder for no use anymore** |
|update|Es actualizar codigo con nuevos parametros o mejoras|_actualizar_| **update dependencies to improve code** |


## Ejemplos completos

Bueno, como para que vean un par de ejemplos mezclando todas las partes del codigo, les dejo las siguientes lineas

```
feat(api/route/index): add new routes for bbb-route

fix(client/navbar): remove useEffect dependency cause loop

refactor(api/aaa-controler): add new folders and files to componentize
```