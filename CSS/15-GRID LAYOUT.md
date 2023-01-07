# CSS GRID LAYOUT.

[Documentación oficial.](https://developer.mozilla.org/es/docs/Web/CSS/CSS_Grid_Layout)
[Ejemplos.](https://github.com/Juan122113/CursoCSS/tree/main/15-CSS-GRID)

Es un sistema de cuadrículas el cual es el sistema más poderoso en CSS para diseñar sitios web. Esto es gracias a su sistema bidimensional, lo que significa que vamos a utilizar tanto columnas, también llamadas columns, como filas, también llamadas rows, a diferencia de flexbox, donde solamente podíamos manipular al main axis.

En CSS se designa en un contenedor, escribiendo:

display: grid;

Y esto se convierte en un contexto de __grid__, donde el contenedor se vuelve un **grid** container y los hijos directos del contenedor se vuelven __grid__ items.

Si los elementos no tienen un ancho o alto definido en css **grid** se van a estirar por defecto

## Filas y columnas,

Se le llama Grid, que significa cuadrícula, porque se utilizan **filas** y __columnas__, estas **filas** y __columnas__ crean una cuadrícula, cada **fila** y __columna__ está formada por dos líneas (**Grid-lines**), una línea de inicio y una línea final. Por el número de **filas** y __columnas__ que tengamos hay una línea extra, si tenemos tres **filas** y/o __columnas__ tendremos cuatro líneas en las __filas__ y cuatro líneas en las **columnas**.

### Grid-template-columns.

[Documentación oficial.](https://developer.mozilla.org/es/docs/Web/CSS/grid-template-columns)

Esta es la propiedad para crear columnas. Dentro se puede poner cualquier unidad de medida. Para crear varias columnas se debe dejar un espacio entre valores:

grid-template-columns: 30%  50px  100px;

### Grid-auto-rows.

[Documentación oficial.](https://developer.mozilla.org/es/docs/Web/CSS/grid-auto-rows)

Esta propiedad especifíca el tamaño de una nueva fila creada de forma implícita. Las filas se generan automáticamente porque tienen la propiedad __grid-auto-rows__ en su valor __auto__, esto define que todas las filas que se creen automáticamente van a tomar un espacio automático. También se puede escribir una unidad de medida que sería el valor para cada fila.

### Grid-auto-columns.

[Documentación oficial.](https://developer.mozilla.org/es/docs/Web/CSS/grid-auto-columns)
[Ejemplos.](https://github.com/Juan122113/CursoCSS/tree/main/22-Landing%20page%20sunny/sunnyside-agency-landing-page-main)

Especifica el tamaño de una columna de cuadrícula creada implícitamente.

### Grid-template-rows.

[Documentación oficial.](https://developer.mozilla.org/es/docs/Web/CSS/grid-template-rows)

Se pueden crear filas con esta propiedad. Es la misma dinámica que con grid-auto-rows, se puede ingresar un valor. Si se ingresa solo un valor ese valor se la asigna a la primer fila, las restantes toman el espacio sobrante si grid-auto-rows está en el valor auto tomando el espacio sobrante por defecto.

Si, por ejemplo, se agregan tres filas pero solo hay elementos suficientes para dos filas, entonces la tercera no se ve. Pero se puede visualizar en Google Chrome, yendo a inspeccionar, haciendo click en la etiqueta "grid" del contenedor de grid en el código html, luego yendo a la pestaña "Layout" para hacer click en la sección de "section.container". 

### repeat()

[Documentación oficial.](https://developer.mozilla.org/es/docs/Web/CSS/repeat)

Lleva dos parámetros, el primer valor es el número de veces que se va a crear una columna o una fila y el segundo valor la unidad que tendrá esa fila o columna. Ejemplo:

grid-template-columns: repeat(10, 10%);

#### auto-fit

Sirve para crear filas y columnas dinámicamente, es decir, el tamaño de las filas y columnas cambia dependiendo el contexto, se ajusta a un cierto tamaño. Por ejemplo: si tengo 900px de espacio disponible y tres elementos de 300px solamente va a crear tres filas porque solamente entran tres columnas de 300px.

grid-template-columns: repeat(auto-fit);

### min-max

[Documentación oficial.](https://developer.mozilla.org/es/docs/Web/CSS/minmax)

Define un rango de tamaño mayor o igual que *min* y menor o igual que _max_. Sirve para indicar el tamaño mínimo y máximo de filas y columnas. Ejemplo:

~~~
grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
~~~

En este caso está indicando que las columnas no sean menores a 250px y si se puede crear más de una columna entonces se van a dividir de manera equitativa gracias al fr.

### fr

Si, por ejemplo, quiero crear tres columnas que ocupen toda la grid, entonces se les da un valor del 33%:

grid-template-columns: repeat(3, 33%);

Aquí está sobrando un 1% y aunque se coloque "33,3333333%" hasta infinito, sigue sobrando un pequeño espacio.

En CSS GRID hay una unidad de medida que se llama **fr**. Esta unidad indica que el espacio disponible se divida en fracciones. Por ejemplo:

grid-template-columns: 1fr  1fr  1fr;

En este ejemplo va a tomar todo el espacio disponible y va a dividirlo entre tres fracciones, y cada columna va a tener un espacio igual y va a repartir el espacio equitativamente para cada columna. Pero por ejemplo, si a la segunda columna se le pusiera un valor de 2 fracciones entonces ocuparía el doble del espacio que las otras dos. Esto es porque se toma el espacio disponible, se lo divide entre cuatro y a la segunda columna se le da un valor de dos fracciones y a las otras dos de una fracción.

### Row-gap.

[Documentación oficial.](https://developer.mozilla.org/en-US/docs/Web/CSS/row-gap)

Permite crear espaciados entre filas.

### Column-gap.

[Documentación oficial.](https://developer.mozilla.org/en-US/docs/Web/CSS/column-gap)

Permite crear espaciados entre columnas.

### Gap.

[Documentación oficial.](https://developer.mozilla.org/es/docs/Web/CSS/gap)

Permite crear espaciados entre columnas y filas. Con un valor da un espaciado igual a ambas y con dos valores el primer valor es para filas y el segundo para columnas.

### Justify-self.

[Documentación oficial.](https://developer.mozilla.org/en-US/docs/Web/CSS/justify-self)
[Ejemplo.](https://github.com/Juan122113/CursoCSS/tree/main/16-room-homepage-master)

Permite alinear grid items en las filas. Establece la forma en que se justifica, se ubica, un item dentro de su contenedor de alineación a lo largo del eje apropiado.

### Grid-auto-flow.

[Documentación oficial.](https://developer.mozilla.org/en-US/docs/Web/CSS/grid-auto-flow)
[Ejemplo.](https://github.com/Juan122113/CursoCSS/tree/main/16-room-homepage-master)

Controla cómo el algoritmo de ubicación automática funciona, especificando exactamente como los items que se ubican automáticamente se posicionan en la cuadrícula.

### Align-items.

[Documentación oficial.](https://developer.mozilla.org/es/docs/Web/CSS/align-items)
[Ejemplos.](https://github.com/Juan122113/CursoCSS/tree/main/22-Landing%20page%20sunny/sunnyside-agency-landing-page-main)

Establece el valor align-self sobre todos los descendientes directos de un grupo. La propiedad align-self indica la alineación de un elemento dentro del bloque que lo contiene. En Grid controla la alineación de los elementos en el eje Block (eje de columnas) dentro de su área grid.

## Celdas.

Una vez que creamos la GRID, la cuadrícula, que es la suma de filas y columnas, se crean __celdas__, que es la parte más pequeña en GRID. Y al principio todos los elementos que estén dentro de la GRID van a ocupar una **celda** por defecto, que es la parte más pequeña de una GRID.

## Líneas.

Las cuadrículas están compuestas de __líneas__, **lineas** verticales o __líneas__ en columnas, y __líneas__ horizontales o **líneas** en filas (culumn grid lines, row grid lines).

### Grid-column.

[Documentación oficial.](https://developer.mozilla.org/en-US/docs/Web/CSS/grid-column)

Gracias a esta propiedad podemos posicionar a los grid items en base a líneas. Acepta dos valores, el primer valor es un número entero, después se separa por una diagonal y el segundo valor también es un número entero. Básicamente indica la línea inicial y la línea final hablando en columnas, es decir, el primer número indica el número de línea donde empieza este elemento hablando de columnas y el segundo, el número final o la línea final donde termina este grid item:

grid-column: línea inicial / línea final;

El valor -1 indica el final de la grid.

### Grid-row.

[Documentación oficial.](https://developer.mozilla.org/en-US/docs/Web/CSS/grid-row)

Es exactamente lo mismo que grid-column pero ahora hablamos de líneas en filas.


## Áreas.

Es el espacio entre cuatro grid lines. Un __grid area__ puede estar formado por el número que sea de celdas, pero un **grid area** siempre debe ser rectangular o cuadrado.

### Grid-template-areas.

[Documentación oficial.](https://developer.mozilla.org/es/docs/Web/CSS/grid-template-areas)

Especifica nombres para cada una de las grid areas.

Ejemplo:

~~~
grid-template-areas:
"element1 element1 element1 element2 element2"
"element1 element1 element1 element2 element2"
"element3 element3 element3 element2 element2"
"element3 element3 element3 element2 element2"
"element4 element4 element4 element4 element4";
~~~

Este es un ejemplo para un grid de cinco filas por cinco columnas. De esta manera se define cada área para el grid. Si se pasa al inspector se van a poder ver los nombres de área en el navegador. Las áreas siempre deben ser cuadradas o rectangulares, si esto no es así por lo menos en un área, se rompen todas las demás.

Para que una celda quede vacía se debe colocar un punto "." en su lugar. Ejemplo:

~~~
grid-template-areas:
"element1 element1 element1 element2 element2"
"element1 element1 element1 element2 element2"
"element3 element3 element3 element2 element2"
"element3 element3 element3 element2 element2"
"element4 element4 element4 element4 .";
~~~

### Grid-area.

[Documentación oficial.](https://developer.mozilla.org/en-US/docs/Web/CSS/grid-area)

La propiedad abreviada __grid-area__ especifica el tamaño y la ubicación de un elemento de cuadrícula (grid item) dentro de una cuadrícula al contribuir con una línea, un tramo o nada (automático) a su ubicación en la cuadrícula, especificando así los bordes de su área de cuadrícula.

Se escribe dentro de los grid items.

### Align-self.

[Documentación oficial.](https://developer.mozilla.org/en-US/docs/Web/CSS/align-self)
[Ejemplo.](https://github.com/Juan122113/CursoCSS/tree/main/16-room-homepage-master)

Permite alinear al grid item en las columnas.




