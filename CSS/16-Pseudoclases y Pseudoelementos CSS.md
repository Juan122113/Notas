# Pseudoclases y Pseudoelementos CSS.

[Documentación oficial.](https://developer.mozilla.org/es/docs/Learn/CSS/Building_blocks/Selectors/Pseudo-classes_and_pseudo-elements)
[Ejemplos.](https://github.com/Juan122113/CursoCSS/tree/main/17-pseudoclases-pseudoelementos)

## Pseudoclases.

[Documentación oficial.](https://developer.mozilla.org/es/docs/Web/CSS/Pseudo-classes)

Son un tipo de selector en CSS que indica mayormente el estado de un elemento y nos ayuda a generar interacciones en nuestra página con CSS. Las pseudoclases siempre empiezan con dos puntos ":" y tienen una especificidad de 10. 

En su mayoría, las pseudoclases indican un estado de nuestra página, pero también hay pseudoclases como root. La pseudoclase root nos sirve para declarar custom properties en la raíz del documento, ya que root es exactamente lo mismo que HTML. Por ejemplo, si al HTML le doy un background-color: black, pero después a root le doy  un background-color: tomato, va a tomar el background-color de root, por que root es una psuedoclase que representa lo mismo que la etiqueta HTML, solamente que al ser una psudoclase tiene una especificidad de 10, mayor que la especificidad de HTML que es un selector de tipo y solo es de 1.

Las psuedoclases pueden ir solas o acompañadas de otro selector. Por ejemplo:

.link:hover{

}

### :hover

[Documentación oficial.](https://developer.mozilla.org/es/docs/Web/CSS/:hover)

Coincide cuando el usuario interactúa con un elemento con un dispositivo señalador, pero no necesariamente lo activa. Generalmente se activa cuando el usuario se desplaza sobre un elemento con el cursor. Indica cuando el usuario está pasando el mouse sobre un elemento. Normalmente se agrega a un selector.

### :active

[Documentación oficial.](https://developer.mozilla.org/es/docs/Web/CSS/:active)

Indica cuando el usuario está presionando a un elemento en nuestro documento HTML y una vez que el usuario deje de presionar a ese elemento ya no está en el estado :active, esto quiere decir que solamente va a estar activa esta pseudoclase cuando esté presionando este elemento.

### :target

[Documentación oficial.](https://developer.mozilla.org/es/docs/Web/CSS/:target)

Representa un elemento único (*el elemento objetivo*) con un id que coincide con el fragmento de la URL.

### :checked

[Documentación oficial.](https://developer.mozilla.org/es/docs/Web/CSS/:checked)

Representa cualquier __radio__, **checkbox** u __option__ (\<option> en un elemento \<select>) que está marcado o conmutado a un estado *on*. Indica cuando un input de tipo radio, checkbox o select están activos. Es decir, indica el estado cuando están activos.

Para que, al hacer click, un input *checkbox* pase a la pseudo clase __checked__ el *for* del label correspondiente debe coincidir con el _id_ del input e input debe ser el hermano adyacente del elemento que se quiera modificar. 

### :focus

[Documentación oficial.](https://developer.mozilla.org/es/docs/Web/CSS/:focus)

Indica cuando el usuario está haciendo foco o está activo en un input. Estado focus o activo es cuando el cursor está ubicado en el input listo para escribir. Generalmente se activa cuando el usuario hace clic, toca un elemento o lo selecciona con la tecla "Tab" del teclado.

### :placeholder-shown

[Documentación oficial.](https://developer.mozilla.org/en-US/docs/Web/CSS/:placeholder-shown)

Indica el estado cuando se muestra el place holder, es decir, representa cualquier \<input> o \<textarea> que esté mostrando texto de placeholder.

### :nth-of-type

[Documentación oficial.](https://developer.mozilla.org/es/docs/Web/CSS/:nth-of-type)
[Ejemplos.](https://github.com/Juan122113/CursoCSS/tree/main/22-Landing%20page%20sunny/sunnyside-agency-landing-page-main)

Selecciona uno o más elementos de un tipo dado, en función de su posición entre un grupo de hermanos.

## Pseudoelementos.

[Documentación oficial.](https://developer.mozilla.org/es/docs/Web/CSS/Pseudo-elements)

Los pseudoelementos empiezan con doble dos puntos "::". En vez de indicar estados como las pseudoclases, en su mayoría, los pseudoelementos permiten crear estilos extra en CSS. Su especificidad es de uno.

### ::before y ::after

[Documentación oficial de ::before.](https://developer.mozilla.org/es/docs/Web/CSS/::before)
[Documentación oficial de ::after.](https://developer.mozilla.org/es/docs/Web/CSS/::after)

Son dos pseudoelementos fundamentales. Solo se puede crear una propiedad **::before** y __::after__ por elemento, esto es por la cascada de CSS. Estos pseudoelementos pueden usar cualquier propiedad de CSS. La característica más singular es que permiten crear elementos sin que los escribamos en el HTML sino en el CSS. 

Las imágenes no permiten usar **::before** y __::after__ porque son replace elements.

#### content

Se pueden crear elementos con ::before y ::after gracias a la propiedad **content**. El valor de __content__ se escribe con comillas. Al escribir la propedad **content** más las comillas ya se está creando un elemento. El elemento creado será hijo del elemento que estamos modificando con los pseudoelementos ::before o ::after. Siempre se debe usar la propiedad __content__ junto con las comillas como valor aunque no tenga texto, si se borra, entonces el pseudoelemento desaparece.
