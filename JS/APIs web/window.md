# Window. 06/23


[Documentación oficial](https://developer.mozilla.org/es/docs/Web/API/Window)

El objeto `window` representa la ventana que contiene un documento DOM, o sea, es el objeto global que representa la ventana del navegador en la que se muestra el contenido del documento. La interfaz `Window` no solo representa ventanas, si no también marcos (`iframes`) y pestañas.


## Propiedades.


### Window.document 06/25


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


## Eventos


### GlobalEventHandlers.onclick 06/30


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