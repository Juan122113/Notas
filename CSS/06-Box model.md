# Box Model.

[Documentación oficial.](https://developer.mozilla.org/es/docs/Web/CSS/CSS_Box_Model/Introduction_to_the_CSS_box_model)
Ejemplos: [HTML](https://github.com/Juan122113/CursoCSS/blob/main/05-BoxModel/BoxModel.html)- [CSS](https://github.com/Juan122113/CursoCSS/blob/main/05-BoxModel/estilosBoxModel.css)
[Gráfico](https://github.com/Juan122113/CursoCSS/blob/main/05-BoxModel/Box%20Model%20Curso.png)

Para comprender CSS debemos comprender que todos los elementos son tratados como cajas, o como rectángulos o cuadrados. Estas cajas tienen propiedades con las cuales podremos cambiar el tamaño de los elementos, su posicionamiento y sobre todo mejorar su diseño. El **box model** en CSS es la manera o la estructura que compone una caja o un elemento en CSS el cual se divide en capas. 
Como se ve en esta [imagen](https://github.com/Juan122113/CursoCSS/blob/main/05-BoxModel/Box%20Model%20Curso.png), que representa a una caja como en cualquier elemento en CSS, es exactamente la misma estructura para todos los elementos, ya sea un \<h1>, un \<div> o un \<p>, todos ellos tienen un content (contenido), un padding (relleno), un border (borde) y un margin (margen). En principio solamente hay un contenido, por ejemplo el lorem de un párrafo, una imagen o cualquier elemento que esté incrustado en el HTML. Después viene la siguiente capa que es el padding o el relleno, la siguiente capa que es el borde y por último la capa del margen que permite alejar o acercar a otros elementos. Este es el **box model**, es la base para crear sitios web.

## Capa de contenido.

Ejemplos: [HTML](https://github.com/Juan122113/CursoCSS/blob/main/05-BoxModel/BoxModelContent.html) - [CSS](https://github.com/Juan122113/CursoCSS/blob/main/05-BoxModel/estilosBoxModelContent.css)

O **área de contenido**, delimitada por el límite del contenido, contiene el contenido "real" del elemento, como lo puede ser el texto, imagen o un reproductor de video. Su dimensiones son el ancho del contenido (o el ancho de la caja de contenido) y la altura del contenido (o la altura de la caja de contenido). A menudo tiene un color de fondo o una imagen de fondo.

## Capa de relleno o Padding.

[Documentación oficial.](https://developer.mozilla.org/es/docs/Web/CSS/padding)
Ejemplos: [HTML](https://github.com/Juan122113/CursoCSS/blob/main/05-BoxModel/BoxModelPadding.html) - [CSS](https://github.com/Juan122113/CursoCSS/blob/main/05-BoxModel/BoxModelContent.html)


Es la segunda capa en el box model. Se encuentra entre el borde y el contenido, esto nos ayuda a crear un espacio entre el borde del elemento y su contenido haciendo que no se peguen, de esta manera damos un diseño más armonioso. Pero agregar padding puede incrementar el alto o ancho del elemento debido a que el box model tiene tres capas que cambian el tamaño, el contenido, el padding y el borde.
Se divide en cuatro propiedades, es decir, hay cuatro propiedades para modificar el padding, cada propiedad está hecha para cada dirección. Direcciones del elemento: arriba, abajo, izquierda y derecha.

### Abreviaciones.

En CSS hay propiedades que abrevian a otras propiedades, un ejemplo es que podemos abreviar las cuatro propiedades de padding (padding-top, padding-bottom, padding-right, padding-left) en una sola (padding). A esto se le conoce como un shorthand, una manera de abreviar propiedades en una. Se puede tener el mismo resultado de las cuatro propiedades en una. La propiedad padding puedeN recibir máximo cuatro valores y mínimo un valor. El orden de anotación que se sigue en los cuatro valores es el de las manecillas del reloj: arriba, derecha, abajo, izquierda.
Si se quieren anotar tres valores entonces se sigue el siguiente orden: arriba, derecha-izquierda, abajo. La derecha y la izquierda comparten el mismo valor.
Si se quieren anotar dos valores entonces se sigue el siguiente orden: arriba-abajo, derecha-izquierda. La derecha y la izquierda, y arriba y abajo comparten el mismo valor.

Documentación oficial:
+ [padding-top](https://developer.mozilla.org/es/docs/Web/CSS/padding-top)
+ [padding-right](https://developer.mozilla.org/en-US/docs/Web/CSS/padding-right)
+ [padding-bottom](https://developer.mozilla.org/es/docs/Web/CSS/padding-bottom)
+ [padding-left](https://developer.mozilla.org/en-US/docs/Web/CSS/padding-left)

## Capa de borde.

[Documentación oficial](https://developer.mozilla.org/es/docs/Web/CSS/border)

Es la capa que sigue después del padding. Es la última capa que modifica el tamaño de los elementos y permite definir la línea del borde agregando diferentes estilos, tamaños y colores, el borde en CSS tiene estas tres características el color, el estilo y el ancho. Para que un borde funcione debemos de tener al menos 2 características las cuales son: el estilo y el tamaño, el color no es tan importante porque se toma por defecto.
Border es otro shorthand, una abreviación de: border-width, border-style y border-color. También puede usarse con la propiedades top, right, bottom y left.

Documentación oficial:
+ [border-top](https://developer.mozilla.org/es/docs/Web/CSS/border-top)
+ [border-right](https://developer.mozilla.org/es/docs/Web/CSS/border-right)
+ [border-bottom](https://developer.mozilla.org/es/docs/Web/CSS/border-bottom)
+ [border-left](https://developer.mozilla.org/es/docs/Web/CSS/border-left)

### Border-width.

[Documentación oficial](https://developer.mozilla.org/es/docs/Web/CSS/border-width)

Define el ancho del borde. Normalmente se acostumbra a usar unidades de medida pero podemos usar palabras reservadas como: 

+ thin -> permite crear un borde muy fino.
+ medium -> permite crear un borde mediano.
+ thick -> permite crear un borde más grueso que el mediano.

Border-width es un shorthand de cuatro propiedades que controlan los cuatro ejes del elemento: arriba, derecha, abajo, izquierda. Esto quiere decir que tenemos cuatro propiedades que componen a border-width:

+ border-top-width
+ border-right-width
+ border-bottom-width
+ border-left-width

También se pueden controlar los cuatro lados del borde solo con la propiedad border-width de la misma manera que se hacía con el padding, en el sentido de las agujas del reloj. Si se ponen dos o tres valores también sucede los mismo que en padding.

Documentación oficial:
+ [border-top-width](https://developer.mozilla.org/en-US/docs/Web/CSS/border-top-width)
+ [border-right-width](https://developer.mozilla.org/en-US/docs/Web/CSS/border-right-width)
+ [border-bottom-width](https://developer.mozilla.org/es/docs/Web/CSS/border-bottom-width)
+ [border-left-width](https://developer.mozilla.org/en-US/docs/Web/CSS/border-left-width)

### Border-style.

[Documentación oficial](https://developer.mozilla.org/es/docs/Web/CSS/border-style)

Define los estilos de la línea del borde de los cuatro lados de el elemento. Al igual que border width es un  shorthand que abrevia cada una de las propiedades para cada dirección del elemento. Se comporta con las mismas reglas que border-width.
Distintos valores:

+ **solid**  -> es el estilo estandar, es el más usado.
+ **dotted** -> define un borde de puntos. 
+ **dashed** -> define un borde de guiones. 
+ **double** -> define un borde de lineas dobles. 
+ __groove__ -> define un borde con un estilo como si estuviéramos sumergiendo el elemento.
+ **ridge** -> define un borde de perspectiva 3d. 

Documentación oficial:
+ [border-top-style](https://developer.mozilla.org/en-US/docs/Web/CSS/border-top-style)
+ [border-right-style](https://developer.mozilla.org/en-US/docs/Web/CSS/border-right-style)
+ [border-bottom-style](https://developer.mozilla.org/es/docs/Web/CSS/border-bottom-style)
+ [border-left-style](https://developer.mozilla.org/en-US/docs/Web/CSS/border-left-style)

### Border color.

[Documentación oficial](https://developer.mozilla.org/es/docs/Web/CSS/border-color)

Define el color del borde de los cuatro lados del elemento. Es un shorthand de cuatro propiedades que modifican el color de cada una de las direcciones de el elemento. Se comporta con las mismas reglas que border-width y border-style.

Documentación oficial:

+ [border-top-color](https://developer.mozilla.org/es/docs/Web/CSS/border-top-color)
+ [border-right-color](https://developer.mozilla.org/en-US/docs/Web/CSS/border-right-color)
+ [border-bottom-color](https://developer.mozilla.org/es/docs/Web/CSS/border-bottom-color)
+ [border-left-color](https://developer.mozilla.org/es/docs/Web/CSS/border-left-color)

Ejemplos de border: [HTML](https://github.com/Juan122113/CursoCSS/blob/main/05-BoxModel/BoxModelBorder.html) - [CSS](https://github.com/Juan122113/CursoCSS/blob/main/05-BoxModel/estilosBoxModelBorder.css)

## Capa de margin.

[Documentación oficial](https://developer.mozilla.org/es/docs/Web/CSS/margin)
Ejemplo: [HTML](https://github.com/Juan122113/CursoCSS/blob/main/05-BoxModel/BoxModelMargin.html) - [CSS](https://github.com/Juan122113/CursoCSS/blob/main/05-BoxModel/estilosBoxModelMargin.css)

Permite establecer un margen o una separación en cuatro direcciones del elemento. Esta es la única capa del box model que no afecta el tamaño del elemento debido a que es una capa externa que se encarga de crear márgenes o separaciones. Es también un shorthand de las cuatro propiedades al igual que sucede con border: top, right, bottom y left.

Documentación oficial:

+ [margin-top](https://developer.mozilla.org/en-US/docs/Web/CSS/margin-top)
+ [margin-right](https://developer.mozilla.org/es/docs/Web/CSS/margin-right)
+ [margin-bottom](https://developer.mozilla.org/es/docs/Web/CSS/margin-bottom)
+ [margin-left](https://developer.mozilla.org/en-US/docs/Web/CSS/margin-left)

También es bueno aclarar que los márgenes pueden ser negativos:

margin-left: -100px;

Esto hace que en vez de alejarlo del margen 100px lo "acerca" 100px, resultando en la superposición del elemento con el margen, luce cortado.

### Márgenes automáticos.

En CSS podemos usar el valor auto, este solamente funciona de manera horizontal en márgenes (hay una excepción en flex box). Solamente podemos usar márgenes automáticos si se cumplen dos reglas, la primera es que el elemento debe ser un display block y la segunda es que debe tener un widht definido.

+ **margin-left**: auto; (envía al bloque a la derecha),
+ __margin-right__: auto; (envía al bloque a la izquierda, pero esta manera es por defecto)

Si se coloca tanto **margin-left**: auto como __margin-right__: auto entonces se consigue centrar al elemento. Pero esto se puede reducir si se escribe:

margin: 0 auto;

Esto es un shorthand.
Solamente se puede centrar con margin si se cumplen las dos condiciones mencionadas anteriormente.

### Colapso de márgenes.

Es un comportamiento que sucede cuando dos márgenes se combinan y se vuelven uno solo, esto solamente pasa con los márgenes verticales, es decir, margin-top y margin-bottom. Cuando dos hermanos adyacentes chocan sus márgenes, lo que pasa es que se van a fusionar, se van a volver un margen solamente y va a predominar el margen con mayor tamaño. 

#### Colapso de márgenes de elementos hijo.

Esto pasa normalmente con el primer o con el último elemento que tengas como hijo. Lo que sucede es que se fusionan o colapsan los márgenes de padre e hijo. Esto sucede porque ambos márgenes se tocan. Se puede solucionar manipulando border y padding. Entonces, por ejemplo, si al padre se le pone un padding o un border de 0.1px se soluciona, porque se está colocando una capa que evita que se toquen el margen del padre y del hijo. Esto sucede tanto en margin top y bottom.

## Box-sizing.

[Documentación oficial](https://developer.mozilla.org/es/docs/Web/CSS/box-sizing)

Si se tiene un width y un hight determinado, por ejemplo 200px cada uno, más un padding, por ejemplo de 50px, más un borde, por ejemplo de 5px; el elemento en cuestión no medirá 200px de ancho si no que sumará su contenido, su padding y su borde, esto hará que tenga 250px de ancho y de alto. 

width: 200px;

height: 200px;

padding: 20px;

border: 5px  solid  chocolate;


Pero si tengo un width en porcentaje 100% lo que sucede es que se desborda el elemento, esto es porque al 100% del navegador hay que agregarle el padding y el borde. Si, por ejemplo, un elemento es necesario que mida 300px en total (incluyendo padding y borde) se deberían hacer cálculos por cada elemento, esto no es algo óptimo y es un gran problema que el padding y el borde afecte al tamaño final. Hay un propiedad que se encarga de modificar este comportamiento, esta propiedad es **box-sizing**. Por __defecto__ su valor es **content-box**, que es el mismo comportamiento recién descrito. Pero con el valor __border-box__ las propiedades width y height son definitivas. Con esto la suma de todos los componentes (content, padding y border) serían las del width y height. Retomando el ejemplo anterior, en este caso sí mediría 200px de ancho y alto. La suma es primero al borde, luego al padding y lo sobrante al contenido.

box-sizing: border-box;

width: 200px;

height: 200px;

padding: 20px;

border: 5px  solid  chocolate;

## Elementos en CSS.

Ejemplos: [HTML](https://github.com/Juan122113/CursoCSS/blob/main/05-BoxModel/card/elementos.html) - [CSS](https://github.com/Juan122113/CursoCSS/blob/main/05-BoxModel/card/estilosElementos.css)

Hay dos tipos de elementos o cajas en CSS y HTML, elementos en bloque y en línea:

### En bloque.

Son las cajas que tienen por defecto un display block. Podemos saber que una caja es un bloque por las siguientes características:
1. Genera un salto de línea debido a que toma el 100% de su contenedor.
2. Los elementos bloque pueden usar todas la propiedades del box model.
También se puede ver con la herramienta inspeccionar, en la pestaña computed (Chrome) o Distribución (Firefox) qué tipo de display tiene.

### En línea.

Son las cajas que tienen un display inline. Podemos saber que es una caja inline si:
1. Se colocan juntos, aparecen en la misma línea, uno al lado del otro, pero con un espacio entre ellos. Si se quiere quitar ese espacio se deben poner las etiquetas pegadas.
2. Solamente ocupan el espacio de su contenido y no les pueden aplicar propiedades del box model. Tampoco aplican los padding, los márgenes y los bordes de manera vertical, es decir, los de arriba y abajo; se los puede agregar pero tienen un comportamiento muy raro. Sí se pueden agregar a los costados.

### Display: Inline-block.

Este es un elemento híbrido. Se usa si se necesita que un elemento se coloque uno al lado del otro pero que pueda ocupar todas las propiedades del box model.
