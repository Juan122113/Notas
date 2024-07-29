# element 07/02


[Documentación oficial](https://developer.mozilla.org/en-US/docs/Web/API/Element)

`element` en la API de DOM representa un objeto de un documento HTML o XML. Es el tipo base más general de un objeto en la jerarquía de nodos del DOM. Los elementos pueden tener atributos y contienen otros nodos, incluidos texto y otros elementos. Es la clase base para las clases más específicas como `HTMLElement`, `SVGElement`, etc.


## Métodos.


### Element.getAttribute() 07/04


[Documentación oficial](https://developer.mozilla.org/es/docs/Web/API/Element/getAttribute)

`getAttribute()` devuelve el valor del atributo especificado en el elemento. Si el atributo especificado no existe, el valor retornado puede ser tanto `null` como `""` (una cadena vacía).


#### Sintaxis.


```js
var atributo = element.getAttribute(nombreAtributo);
```

donde

- `atributo` es una cadena que contiene el valor del atributo `nombreAtributo`.
- `nombreAtributo` es el nombre del atributo del cual se quiere obtener el valor.


#### Ejemplo.


```js
var div1 = document.getElementById("div1");
var align = div1.getAttribute("align");

alert(align); // Muestra el valor de la alineación (align) del elemento con id="div1"
```


### Element.setAttribute 07/05


[Documentación oficial](https://developer.mozilla.org/es/docs/Web/API/Element/setAttribute)

Establece el valor de un atributo en el elemento indicado. Si el atributo ya existe, el valor es actualizado, en caso contrario, el nuevo atributo es añadido con el nombre y valor indicado.


#### Ejemplo


En el siguiente ejemplo, `setAttribute()` se utiliza para establecer atributos en un `<button>`.


##### HTML


```html
<button>Hola Mundo</button>
```


##### JavaScript


```js
var b = document.querySelector("button");

b.setAttribute("name", "helloButton");
b.setAttribute("disabled", "");
```

Esto demustra dos cosas:

- La primera llamada a `setAttribute()` muestra cómo se cambia el valor del atributo `name` a "helloButton". Puede ver esto utilizando el inspector de página de su navegador.
- Para establecer el valor de un atributo booleano, como `disabled` se puede especificar cualquier valor. Una cadena de texto vacía o el nombre de un atributo son valores recomendados. Todo lo que importa es que si el atributo está presente, *independientemente de su valor actual*, su valor se considera como `true`. La ausencia del atributo significa que su valor es `false`. Estableciendo una cadena vacía (`""`) como el valor del atributo `disabled`, se estaría cambiando `disabled` a `true`, lo que provoca que el botón sea deshabilitado.


## Element: evento click


[Documentación oficial](https://developer.mozilla.org/es/docs/Web/API/Element/click_event)

Un elemento recibe un evento `click` (clic) cuando se presiona y se suelta un botón del dispositivo señalador (como el botón principal del mouse) mientras el puntero se encuentra dentro del elemento.


### Ejemplos


Este ejemplo muestra el número de clics consecutivos en un `<button>`.


#### HTML


```html
<button>Clic</button>
```


#### JavaScript


```js
const button = document.querySelector("button");

button.addEventListener("click", (event) => {
  button.textContent = 'Recuento de clics: ${event.detail}';
});
```