# Position.

Documentación oficial:
+ [Position](https://developer.mozilla.org/es/docs/Web/CSS/position)
+ [Top](https://developer.mozilla.org/es/docs/Web/CSS/top)
+ [Right](https://developer.mozilla.org/es/docs/Web/CSS/right)
+ [Bottom](https://developer.mozilla.org/es/docs/Web/CSS/bottom)
+ [Left](https://developer.mozilla.org/es/docs/Web/CSS/left)

[Ejemplos.](https://github.com/Juan122113/CursoCSS/tree/main/09-Unidades%20de%20medida)

La propiedad position de CSS especifica cómo un elemento es posicionado en el documento. Las propiedades top, right, bottom y left determinan la ubicación final de los elementos posicionados. Estas propiedades usan unidades de medida, por ejemplo: píxeles, rem, em, porcentajes o unidades de viewport.

## Flujo del navegador.

El flujo del navegador por defecto es, en simples palabra, la manera en que cada elemento se va posicionando. Cada vez que se crea un elemento, siempre se crea desde arriba y hacia la izquierda, y si se siguen agregando elementos se siguen colocando de la misma manera, este es el flujo por defecto. Podemos ir modificándolo con márgenes y con posicionamientos.

En CSS hay distintos tipos de posicionamientos y algunos de ellos nos permiten modificar el flujo del navegador.

## Tipos de posicionamiento.

### Static.

Es el valor que todos los elementos tienen por defecto.

### Relative.

Por defecto se posiciona como cualquier otro elemento, no hay ningún cambio al principio. Pero esta propiedad desbloquea cuatro valores, estos cuatro valores son valores de offset, es decir son valores que permiten cambiar o desplazar al elemento a través del navegador en base a una posición. En este caso, como hablamos de relative, su posición, a partir de la que se moverá, es su posición inicial, por eso se llama relativo, porque se mueve en base a su posicionamiento original o en base a si mismo. Por defecto desbloquea cuatro propiedades: top, right, bottom y left; estas cuatro propiedades nos permiten desplazar al elemento a través del navegador. Aunque se mueva, sigue conservando su posición de acuerdo al flujo.

#### Top.

Por ejemplo, si se le dan 50px, el elemento se mueve ese valor desde la parte de arriba. Si se quiere comparar con margin, esta propiedad empuja a los demás elementos de abajo, en este caso, pero top no. Top lo que hace es que a partir del borde superior del elemento o de la parte superior del elemento va a mover 50px hacia abajo al elemento pero sin modificar el posicionamiento de los demás. Ya estamos trabajando con el flujo de los elementos.

Entonces top nos permite mover al elemento desde la parte superior o el borde superior del elemento, desde ahí vamos a partir. Si ponemos un valor positivo, por ejemplo 100px, va a empujar hacia abajo, pero si ponemos un valor negativo, lo va a empujar hacia arriba, siempre partiendo desde el borde superior del elemento.

#### Right.

Nos permite mover al elemento desde la derecha o desde el borde derecho del elemento. Si ponemos un valor positivo lo mueve hacia la izquierda, si ponemos uno negativo lo mueve a la derecha. Es un poco contradictorio, pero para no confundirse conviene pensar que lo empuja desde la derecha, hablando de números positivos y al revés en el caso de números negativos.

#### Bottom.

Nos permite mover al elemento desde la parte inferior del mismo o desde el borde inferior. Con un valor positivo lo empuja hacia arriba, o sea desde abajo hacia arriba; y con un valor negativo lo empuja hacia abajo.

#### Left.

Nos permite mover al elemento desde izquierda, desde el borde izquierdo del elemento. Con un valor positivo lo empuja hacia la derecha, y con un valor negativo lo empuja hacia la izquierda.

### Absolute.

Cuando un elemento tiene un position absolute, ese elemento es removido completamente del flujo, es como si ya no existiera, ahora puede posicionarse en cualquier parte pero ya no tiene un espacio reservado.

Si relative usaba las propiedades top, left, right y bottom para moverse en base a su posición original, la referencia de origen de absolute es su ancestro o contenedor mas cercano que tenga un position diferente a static.

Entonces position absolute sirve para posicionarse en base a un ancestro, cuando un ancestro no tiene un position declarado entonces se posiciona al navegador.

### Fixed.

Es básicamente lo mismo que absolute porque el elemento modificado es removido completamente del flujo, pero la diferencia es que este elemento se posiciona directamente al viewport, se queda pegado en el viewport, a pesar de mover la página, de hacer scroll, el elemento queda fijado a la pantalla.

## Z index.

[Documentación oficial.](https://developer.mozilla.org/es/docs/Web/CSS/z-index)

Todos los elementos que tengan un position distinto a static desbloquean un contexto de apilamiento el cual, en pocas palabras, nos permite definir qué elemento estará por encima de otro en caso de que dos elementos lleguen a ocupar el mismo espacio en el navegador, esto se hace por medio de un eje z imaginario.

Cualquier elemento posicionado tiene un z index auto, que sería igual a 0; cuando es así siempre se va a mostrar el elemento que haya sido el último en ser escrito. Z index solamente acepta valores enteros, cualquier número que se elija. Se recomienda usar valores altos, como 100, 200, 300; ya que si se quiere poner un elemento en medio va a resultar más fácil.
