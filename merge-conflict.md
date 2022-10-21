# Si llegaste acá, que no panda el cunico©

> - [Índice](#si-llegaste-acá-que-no-panda-el-cunico© "índice")
>   - [Solucion 1](#método-1-source-control-y-file-comparator "solucion 1")
>   - [Solucion 2](#método-2-merge-editor "solucion 2")


Y, aparecio un conflico en el mergeo, luego de hacer `git merge dev` y te apareció, en consola, algo así

```
Auto-mergin xxx_file.js
CONFLICT(content): Merge conflict in xxx_file.js
Automatic merge failed; fix conficts and then commit the result.
```

Quedate tranquilo, que la solución es MUCHISIMO mas facil de lo que crees. Solo que ha que hacer el mergeo manualmente. Y no, no es que tenes que copiar el codigo a mano (aunque a veces si), solo tenes que mezclar las partes que corresponden unir.

Por suerte, nuestro querido VSCode tiene el maravilloso Source Control, y también unos controladores de versionado, que nos permiten hacer el trabajo de unir ambos archivos de una manera mucho mas sencilla. 

## Método 1: Source control y file-comparator

![source control](./Images/merge-conflict.png "source control")

Podremos ver en nuestros archivos en el source control, en la zona de "merge changes" que son los cambios de mergeo.  
Al hacerle click al archivo, se nos abrirá el archivo mostrandonos los conflictos generados.  
Resaltado en __Verde__, podras ver los cambios hechos por tí, es decir, los que se encuentran en la rama que estas **TU**.  
Resaltado en __Azul__, podras ver lo cambios que vienen desde la rama que mergeas. En este caso, como el comando fue `git merge dev`, serán los cambios que trae la rama `dev`

![file-comparator](./Images/file-editor.png "file comparator")  
![file-comparator-2](./Images/file-editor-2.png "file-comparator-2")

Por encima de el recuadro verde, podran ver cuatro opciones  
`Accept Current Change | Accept Incoming Changes | Accept Both Changes | Compare Changes`  
Al aceptar una de ellas, sea la opcion que acepten, reemplazará o unira el codigo.

> _Está muy bien definido que es current y que es incoming en la imagen. Incluso el mismo VSCode te lo muestra_  

Puede suceder que tengas mas de uno de estos cuadritos de cambios, para partes especificas de codigo.  

>_Tambien cabe destacar que, podes utilizar este metodo, o hacer la union bien a mano. Es decir, borrarás este "HEAD" el "main" y corregiras a mano el codigo que está en el medio. Cada quien toma su forma de resolverlo._

Una vez lo resuelves, guardas el archivo y te debería aparecer del siguiente modo en el source-control

![sorce-control](./Images/merge-conflict-2.png "source-control")

podras ver que **YA TIENE UN MENSAJE DE COMMIT**. dejalo tal y como está, y le das click a commit. Una vez commiteado. En tu consola veras que la rama en la que estas tiene un `(rama|MERGING)`. simplemente le daras a enter para que salga del estado de merging y veras lo siguiente (segun la rama y carpeta donde estes)

![consola](./Images/merge-conflict-3.png "consola")

Una vez hecho el enter, puedes proceder con el git push.

>_Si el `(rama|MERGING)`_ no se va, y queda ahí, es que todavia te quedan archivos con conflictos.

## Método 2: Merge-editor

>Este es otro método para resolver los conflictos. 

![file-comparator-2](./Images/file-editor-2.png "file-comparator-2")

Cuando entras, desde el source control, al archivo que está en conflicto (como mostramos en la parte anterior) podras divisar en la parte inferior derecha, un boton que dice **Resolve in Merge Editor** o **Resolver en editor de mergeo**.  
Al hacerle click, podras divisar lo que coloco en la siguiente imagen, que es otro editor de mergeo. Este tiene varias funciones, pero por ahora, veremos las basicas

![merge-editor](./Images/merge-editor.png "merge-editor")

Aquí tambien tienes los accept, como antes, pero los tienes separados en `Accept incoming|Accept Both` y `Accept Current|Accept Both`, la ventaja que supone esto, representa en poder ver, lado a lado, las diferencias en el codigo. sumado a que, a medida que vas aceptando las diferentes partes de codigo, se muestran, en el recuadro de abajo, cómo va quedando el código como resultado final.

> DETALLE: no siempre va a aparecer esta opcion de Accept Incoming, etc. A veces, apareceran unos recuadritos oscuros, que representan una linea, o una sección de codigo, en la que es necesario elegir solo uno de las dos partes del codigo. Cuando le hacen click, en ese cadradito que se ubica sobre la izquierda aparecera un pequeño circulo blanco, que representara que parte del codigo se quedará.

Una vez resueltos los conflictos, podran ver que, la opción "Complete Merge" se liberará, restando 0 confictos a solucionar. Cuando le dan click al boton `Complete Merge` se solucionara el conflicto y podran ver, desde el **Source Control** la misma imagen que antes 

![sorce-control](./Images/merge-conflict-2.png "source-control")

en la que lo cambios ya están en zona de "Staged Changes", permitiendo así, hacer el commit y luego el push, del mismo modo que en el otro caso (Enter en la consola, luego git push) .

LISTO, NO HAY MAS CONFLICTOS
>_Cabe destacar que el conflicto aquí generado es simple y no tiene tanta profundidad debido a que es en modo de ejemplo._

[Volver al indice](#si-llegaste-acá-que-no-panda-el-cunico© "inicio")