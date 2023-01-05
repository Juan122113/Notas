# Flexbox.

[Documentación oficial.](https://developer.mozilla.org/es/docs/Web/CSS/CSS_Flexible_Box_Layout/Basic_Concepts_of_Flexbox)
[Ejemplos.](https://github.com/Juan122113/CursoCSS/tree/main/12-Flexbox)

Es un módulo de CSS que fue diseñado para crear sitios flexibles y adaptables a dispositivos móviles, sitios que se adapten a cualquier dispositivo, por eso se llama **flexbox**, porque nos permite darle flexibilidad a los elementos.

Para comenzar con __flexbox__ debemos tener un contenedor, y ese contenedor, mínimo, debe tener un elemento dentro.

Para declarar **flexbox** hay que escribir dentro del contenedor la propiedad __display__ pero con el valor **flex**. Al hacer esto estamos usando __flexbox__ y creamos un contexto donde el contenedor ahora se llamará **flex container** y los elementos se llamarán __flex items__, pero solamente los hijos directos de el contenedor se llamarán así.

Por más que los hijos del contenedor sean elementos de bloque, lo que hace **flexbox**, es poner a los elementos uno al lado del otro y comienzan a aparecer desde el borde inicial del contenedor. Esto es lo que hace __flexbox__, nos permite poner un elemento al lado del otro aunque sean elementos bloque. Se llama flexible, porque por ejemplo, si se le da a dos o más elementos de un contenedor un ancho de 300px y al contenedor se le da un ancho de 300px, no lo desbordan a pesar de que estén uno al lado del otro, aquí entra la flexibilidad en **flexbox** que nos permite hacer a los elementos más pequeños para que se ajusten al contenedor.

## Propiedades para el contenedor o flex-container.

### Flex direction.

[Documentación oficial.](https://developer.mozilla.org/es/docs/Web/CSS/flex-direction)

En __flexbox__ tenemos dos ejes, el main axis o eje principal y el cross axis o el eje secundario. Por defecto, el main axis va de izquierda derecha y el eje secundario va de arriba hacia abajo. Pero esto se puede modificar con **flex direction**. __Flex direction__ nos permite cambiar el eje principal en el que trabaja **flexbox**.

#### Valores.

+ __row__ -> es  su valor por defecto, cuando está **row**, el eje principal va de izquierda a derecha y el secundario de arriba a abajo.
+ __row-reverse__ -> en este caso el eje principal cambia de derecha hacia izquierda, al revés del valor por defecto; pero el eje secundario continua igual.
+ **column** -> este es un valor en columna que cambia el main axis, ahora en vez de ser horizontal va a ser vertical, es decir, va de arriba hacia abajo; en este caso el cross axis será de izquierda a derecha.
+ __column reverse__ -> en este caso el main axis empieza desde abajo hacia arriba y el cross axis será de izquierda a derecha.

### Flex-wrap.

[Documentación oficial.](https://developer.mozilla.org/es/docs/Web/CSS/flex-wrap)

Define el comportamiento de los hijos cuando su tamaño sumado rebasa el tamaño del main axis. Por defecto el main axis ahora es horizontal.

#### Valores.

+ **nowrap** -> valor por defecto, es decir, que si algunos elementos sobrepasan el tamaño del main axis se hacen más pequeños.
+ __wrap__ -> en este caso, si los elementos no entran, uno al lado del otro,  en el ancho del contenedor, entonces se crean líneas nuevas en el cross axis, verticalmente, de arriba hacia abajo.
+ **wrap-reverse** -> es exactamente lo mismo que wrap, solamente que ahora se comienza desde el final del cross axis.

### Justify-content.

[Documentación oficial.](https://developer.mozilla.org/en-US/docs/Web/CSS/justify-content)

Cambia la alineación en el main axis. Para realizar esto hay que tener espacio disponible en el eje principal.

#### Valores.

+ __flex-start__ -> valor por defecto. Lo que hace es que agrupa a todos los flex items y los alinea al principio del main axis.
+ **flex-end** -> es la contraparte de flex-start, manda a los elementos a la derecha del container, porque la derecha es el final del main axis, en el caso de que flex-direction esté en row; pero si está en el valor de column entonces se irían abajo del contenedor.
+ __center__ -> nos permite centrar a los flex items. También depende de los valores de flex-direction.
+ **space-between** -> hace que los elementos se distribuyan equitativamente por todo el main axis. Pero el primer elemento se pegará siempre al inicio del main axis y el último elemento se pegará al final del main axis.
+ __space-around__ -> en este caso todos los elementos se distribuyen equitativamente en ambos lados. En el caso de que haya un elemento al lado del otro sus dos espacios se suman.
+ **space-evenly** -> da un espacio equitativo tanto en las esquinas como en medio de los elementos, no importa si hay un elemento al lado del otro.

### Align-items.

[Documentación oficial.](https://developer.mozilla.org/es/docs/Web/CSS/align-itemss)

Establece el valor align-self sobre todos los descendientes directos de un grupo. La propiedad align-self indica la alineación de un elemento dentro del bloque que lo contiene. En Flexbox, nos permite modificar el cross axis. **Align-items** hace que todos los elementos que no tengan un height definido se estiren por todo el cross axis.

#### Valores.

+ __strech__ -> valor por defecto.
+ **flex-start** -> manda a los elementos al inicio del cross axis.
+ __flex-end__ -> manda a los elementos al final del cross axis.
+ **center** -> centra a los elementos en el cross axis.
+ __baseline__ -> hace que los elementos se alineen en base a la línea base de los elementos. La línea base sería mas o menos el borde inferior de los textos.

### Align-content.

[Documentación oficial.](https://developer.mozilla.org/en-US/docs/Web/CSS/align-content)

Sirve solamente para el cross axis. Solo funciona cuando hay más de una fila o columna, es decir, cuando un elemento o más de un elemento se desbordan.

#### Valores.

+ **normal** -> valor por defecto.
+ __flex-start__ -> a todos los elementos los agrupa y los manda al inicio del cross axis.
+ **flex-end** -> agrupa a todos los elementos y los manda al final del cross axis.
+ __center__ -> agrupa a todos los elementos y los centra.
+ **space-between** -> manda a los elementos a las esquinas. Si, por ejemplo, tenemos tres elementos, al primero lo manda al inicio del cross axis y al último al final del cross axis, y en base a eso reparte el espacio disponible equitativamente.
+ __space-around__ -> da el mismo espacio para cada lado de los elementos, pero en el caso de que haya un elemento al lado del otro, sus dos espacios se suman.
+ **space-evenly** -> da el espacio equitativamente para todos los lados.

## Propiedades para los elementos o flex-items.

### Order.

[Documentación oficial.](https://developer.mozilla.org/es/docs/Web/CSS/order)

Especifica el orden utilizado para disponer los elementos en su contenedor flexible. Todos los elementos tienen un order que por defecto es de 0. El __order__ permite cambiar el orden de los flex items.

### Flex-grow.

[Documentación oficial.](https://developer.mozilla.org/es/docs/Web/CSS/flex-grow)

Define el factor de crecimiento de todos los elementos. Por defecto su valor es 0. Lo que hace **flex-grow** es que detecta si hay espacio sobrante y en caso de que lo haya determina qué tanto le va a quedar de espacio a cada elemento.

Por ejemplo, si se coloca un __flex-grow__ de 1 a un grupo de tres elementos, estos van a estirarse hasta abarcar el espacio sobrante. Pero si al elemento 2 se le asigna un **flex-grow** de 2, este elemento toma dos veces más del espacio sobrante. Suponamos que el espacio sobrante son 100px y si cada elemento tiene un __flex-grow__ de 1 pero el elemento 2 tiene un **flex-grow** de 2 entonces 100px entre 4 (4 espacios sobrantes) es igual a 25px; el elemento 1 y el elemento 3 que tienen un __flex-grow__ de 1 tomarán 25px de ese espacio disponible, pero el elemento 2 tomará 50px de ese espacio, porque tiene un **flex-grow** de 2. 

### Flex-shrink.

[Documentación oficial.](https://developer.mozilla.org/es/docs/Web/CSS/flex-shrink)

Es lo contrario a flex-grow. **Flex-shrink** especifica el factor de contracción de un flex item. Los flex items se encongerán para llenar el contenedor de acuerdo a su número __flex-shrink__, cuando el tamaño por defecto de los flex items sea mayor al de su contenedor flex container.

Por ejemplo, si dentro de un contenedor con un max-width de 800px, tenemos 3 elementos con un width de 300px cada uno, por defecto en flex-box los elementos se hacen más pequeños para entrar en su contenedor, porque tienen un __flex-shrink__ en 1 que hace que todos se hagan más pequeños por igual, pero si se lo pone en 0 se le quita la habilidad de que se hagan más pequeños.

### Flex-basis.

[Documentación oficial.](https://developer.mozilla.org/es/docs/Web/CSS/flex-basis)

Nos permite indicar el tamaño de los elementos en el main axis, por defecto el main axis es horizontal, es decir, por defecto define el width. Y si debajo de **flex-basis** se coloca un width, el with no se aplica porque el __flex-basis__ tiene más prioridad que el width o el height. Y si se cambia la dirección en el contenedor, por ejemplo, a columnas, vertical, entonces el **flex-basis** pasa a ser el alto.

### Align-self.

[Documentación oficial.](https://developer.mozilla.org/es/docs/Web/CSS/align-self)

Permite alinear solamente al elemento que estamos seleccionando y permite modificarlo a través del cross axis o del eje vertical. Sirve para Grid también.

#### Valores.

Tiene los mismos valores que align-items.

+ __strech__ -> valor por defecto.
+ **flex-start** -> manda a los elementos al inicio del cross axis.
+ __flex-end__ -> manda a los elementos al final del cross axis.
+ **center** -> centra a los elementos en el cross axis.
+ __baseline__ -> hace que los elementos se alineen en base a la línea base de los elementos. La línea base sería mas o menos el borde inferior de los textos.

### Place-self.

[Documentación oficial.](https://developer.mozilla.org/en-US/docs/Web/CSS/place-self)
[Ejemplos.](https://github.com/Juan122113/CursoCSS/tree/main/22-Landing%20page%20sunny)

Este es un shorthand. Permite alinear un elemento individual en las direcciones de bloque y en línea a la vez (es decir, las propiedades align-self y allow-self) en un sistema de diseño relevante como Grid o Flexbox. Si el segundo valor no está presente, el primer valor también se usa para él.



