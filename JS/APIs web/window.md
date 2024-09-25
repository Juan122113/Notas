# Window


[Documentación oficial](https://developer.mozilla.org/es/docs/Web/API/Window)

El objeto `window` representa la ventana que contiene un documento DOM, o sea, es el objeto global que representa la ventana del navegador en la que se muestra el contenido del documento. La interfaz `Window` no solo representa ventanas, si no también marcos (`iframes`) y pestañas.


## Propiedades.


### Window.document


[Documentación oficial](https://developer.mozilla.org/es/docs/Web/API/Window/document)

Retorna una referencia al documento contenido en la ventana.


#### Ejemplo.


```html
<!doctype html>
<html>
  <head>
    <title>Hola, Mundo!</title>
  </head>
  <body>
    <script type="text/javascript">
      var doc = window.document;
      console.log(doc.title); // Hola, Mundo!
    </script>
  </body>
</html>
```


<div id="localStorage">

### Windows.localStorage 


[Documentación oficial](https://developer.mozilla.org/es/docs/Web/API/Window/localStorage)

[Ejemplo](https://github.com/Juan122113/beginner-html-site-styled-gh-pages/blob/main/scripts/main.js)

La propiedad de solo lectura `localStorage` te permite acceder al objeto local `Storage`; los datos persisten almacenados entre las diferentes sesiones de navegación.


#### Sintaxis


```js
miStorage = window.localStorage;
```


##### Valor


Un objeto `Storage` que se puede utilizar para acceder al espacio de almacenamiento local del origen actual.


### Window.sessionStorage


[Documentación oficial](https://developer.mozilla.org/es/docs/Web/API/Window/sessionStorage)

La propiedad `sessionStorage` permite acceder a un objeto `Storage` asociado a la sesión actual. La propiedad `sessionStorage` es similar a [`localStorage`](#localStorage), la única diferencia es que la información almacenada en [`localStorage`](#localStorage) no posee tiempo de expiración, por el contrario la información almacenada en `sessionStorage` es eliminada al finalizar la sesión de la página.


#### Sintaxis


```js
// Almacena la información en sessionStorage
sessionStorage.setItem("key", "value");

// Obtiene la información almacenada desde sessionStorage
var data = sessionStorage.getItem("key");
```


##### Valor


Un objeto de tipo `Storage`.


#### Ejemplo


El siguiente código accede al objeto `Storage` de la sesión actual del dominio y le añade un elemento utilizando `Storage.setItem()`.

```js
sessionStorage.setItem("myCat", "Tom");
```

El siguiente ejemplo graba de forma automática el contenido de un campo de texto, y si el navegador es actualizado accidentalmente, restaura el contenido del campo de texto para no perder lo escrito.

```js
// Obtiene el campo de texto que vamos a monitorear
var field = document.getElementById("field");

// Verificamos si tenemos algún valor auto guardado
// (esto solo ocurrirá si la página es recargada accidentalmente)
if (sessionStorage.getItem("autosave")) {
  // Restaura el contenido al campo de texo
  field.value = sessionStorage.getItem("autosave");
}

// Espera por cambios en el campo de texto
field.addEventListener("change", function () {
  // Almacena el resultado en el objeto de almacenamiento de sesión
  sessionStorage.setItem("autosave", field.value);
})
```


## Métodos


### Window.fetch() 09/25


[Documentación oficial](https://developer.mozilla.org/es/docs/Web/API/Window/fetch)

El método `fetch()` lanza el proceso de solicitud de un recurso de la red. Esto devuelve una promesa que resuelve al objeto `Response` que representa la respuesta a la solicitud realizada.


#### Sintaxis


```js
Promise<Response> fetch(input[, init]);
```


##### Parámetros


*input*

  Define el recurso que se quiere solicitar.
  Puede ser:
  - Un `USVString` con la URL del recurso a solicitar. Algunos navegadores aceptan los esquemas `blob:` y `data:`.
  - Un objeto `Request`.

*init*(Opcional)

  Objeto de opciones que contiene configuraciones para personalizar la solicitud.


##### Return value


Una `Promise` que resuelve a un objeto `Response`.


#### Ejemplo


En el ejemplo de solicitud con Request creamos un nuevo objeto `Request` usando el constructor pertinente, y realizamos una solicitud usando `fetch()`. Dado que estamos solicitando una imagen, ejecutamos `Body.blob()` en la respuesta para darle el tipo MIME correspondiente para que sea gestionada apropiadamente, luego creamos un objeto URL de ella para mosrarla en un elemento `<img>`.

```js
var miImagen = document.querySelector("img");

var miSolicitud = new Request("flores.jpg");

fetch(miSolicitud)
  .then(function (respuesta) {
    return respuesta.blob();
  })
  .then(function (respuesta) {
    var objeto = URL.createObjectURL(respuesta);
    miImagen.src = objeto;
  });
```


### Window.prompt()


[Documentación oficial](https://developer.mozilla.org/es/docs/Web/API/Window/prompt)

El método `Window.prompt()` muestra un diálogo con mensaje opcional, que solicita al usuario que introduzca un texto. Opcionalmente, también se puede agregar que figure el texto que se prefiera en el espacio donde se coloca la entrada de texto. 


#### Ejemplo


```js
let sign = prompt("What's your sign?");

if (sign.toLowerCase() == "aquarius") {
  alert("Wow! I'm a Aquarius too!");
}

// there are many ways to use the prompt feature
sign = window.prompt(); // open the blank prompt window
sign = prompt(); // open the blank prompt window
sign = window.prompt("Are you feeling lucky?"); // open the window with Text "Are you feeling lucky?"
sing = window.prompt("Are you feeling lucky?", "sure"); // open the window with Text "Are you feeling lucky?" and default value "sure"
```


## Eventos


### GlobalEventHandlers.onclick


[Documentación oficial](https://developer.mozilla.org/es/docs/conflicting/Web/API/Element/click_event)

La propiedad **onclick** devuelve el manejador del evento `click` del elemento actual.


#### Sintaxis


```js
element.onclick = functionRef;
```


#### Ejemplo


```html
<html lang="en">
    <head>
        <meta charset="UTF-8" />
        <title>onclick event example</title>
        <script>
            function initElement() {
                var p = document.getElementById("foo");
                // NOTE: showAlert(); or showAlert(param); will NOT work here.
                // Must be a reference to a function name, not a function call.
                p.onclick = showAlert;
            };

            function showAlert(event) {
                alert("onclick Event detected!");
            }
        </script>
        <style>
            #foo {
                border: solid blue 2px;
            }
        </style>
    </head>
    <body onload="InitElement();">
        <span id="foo">My Event Element</span>
        <p>click on the above element.</p>
    </body>
</html>
```

O se puede usar una función anónima, como esta:

```js
p.onclick = function(event) { alert("moot!"); };
```