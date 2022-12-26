# Border-radius.

Permite redondear las esquinas del elemento. Esto nos permite generar diversos estilos entre formas levemente redondeadas, círculos o figuras ovaladas. Podemos usar unidades de medidas como píxeles, porcentajes y otras. Si se coloca un porcentaje de 50% se genera un círculo si es que el ancho y el alto son iguales, es decir, el elemento debe tener una forma cuadrada, si esto no es así entonces crea un óvalo. [Documentación oficial.](https://developer.mozilla.org/en-US/docs/Web/CSS/border-radius) - [Ejemplos.](https://github.com/Juan122113/CursoCSS/tree/main/06-Radius-Shadow)

Esta propiedad es un shorthand de cuatro propiedades:
+ [border-top-left-radius](https://developer.mozilla.org/es/docs/Web/CSS/border-top-left-radius)
+ [border-top-right-radius](https://developer.mozilla.org/es/docs/Web/CSS/border-top-right-radius)
+ [border-bottom-right-radius](https://developer.mozilla.org/es/docs/Web/CSS/border-bottom-right-radius)
+ [border-bottom-left-radius](https://developer.mozilla.org/es/docs/Web/CSS/border-bottom-left-radius)
Estas cuatro propiedades se pueden agregar a la propiedad de border-radius anotando sus valores en el orden de las agujas de reloj. Si solo se anotan tres valores entonces el primero va a corresponder a border-top-left-radius, el segundo a border-top-right-radius, el tercero a border-bottom-right-radius y el cuarto valor que falta, border-bottom-left-radius, lo va a tomar de su contrario: border-top-right-radius.  Si se colocan dos valores, el primero será para border-top-left-radius y su contraparte, border-bottom-right-radius, y el segundo valor para border-top-right-radius y su contraparte, border-bottom-left-radius.

# Box-shadow.

[Documentación oficial.](https://developer.mozilla.org/es/docs/Web/CSS/box-shadow)- [Ejemplos.](https://github.com/Juan122113/CursoCSS/tree/main/06-Radius-Shadow)

Nos permite agregar sombras a un elemento. Las sombras en CSS es la copia exacta de un elemento tanto en forma como en tamaño. Por defecto acepta dos valores.
Se pueden crear varias sombras del mismo elemento colocando una coma al final de sus valores y volviendo a comenzar con la colocación de los mismos. Ejemplo:

box-shadow: 100px  -100px  20px  0  hsla(236, 37%, 59%, 0.397), 100px  200px  0  -100px  orange, 200px  100px  0  -70px;

## Valores.

Se escriben en este orden.

+ **offset-x** -> permite el movimiento de derecha a izquierda. Es obligatorio. Si se ponen número positivos lo mueve hacia la derecha, si son negativos hacia la izquierda.
+ **offset-y** -> permite el movimiento de arriba ya bajo. Es obligatorio. Si se ponen número positivos lo mueve hacia la abajo, si son negativos hacia la arriba.
+ **blur** -> difuminado de la sombra.
+ **spread** -> es el esparcimiento de la sombra.
+ **color** -> se toma por defecto del color del elemento.
