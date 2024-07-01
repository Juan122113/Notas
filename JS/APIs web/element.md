# element


## Element: evento click 06/29


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