# Storage 07/16


[Documentación oficial](https://developer.mozilla.org/es/docs/Web/API/Storage)

La interfaz `Storage` de la API de almacenamiento web provee acceso al almacenamiento de la sesión o al almacenamiento local para un dominio en particular, permitiéndote, por ejemplo, añadir, modificar o eliminar elementos de datos almacenados.


## Ejemplo.


Aquí tenemos un objeto `Storage` al llamar a `localStorage`. Primero probamos si el almacenamiento local contiene elementos de dato usando `!localStorage.getItem('bgcolor')`. Si lo hace, ejecutamos una función llamada `setStyles()` que obtiene los elementos usando `localStorage.getItem()` y utiliza dichos valores para actualizar los estilos de la página. Si no, ejecutamos otra función, `populateStorage()`, que utiliza `localStorage.setItem()` para definir los valores de los elementos, luego ejecuta `setStyles()`.

```js
if (!localStorage.getItem("bgcolor")) {
    populateStorage();
} else {
    setStyles();
}

function populateStorage() {
    localStorage.setItem("bgcolor", document.getElementById("bgcolor").value);
    localStorage.setItem("font", document.getElementById("font").value);
    localStorage.setItem("image", document.getElementById("image").value);

    setStyles();
}

function setStyles() {
    var currentColor = localStorage.getItem("bgcolor");
    var currentFont = localStorage.getItem("font");
    var currentImage = localStorage.getItem("image");

    document.getElementById("bgcolor").value = currentColor;
    document.getElementById("font").value = currentFont;
    document.getElementById("image").value = currentImage;

    htmlElem.style.backgroundColor = "#" + currentColor;
    pElem.style.fontFamily = currentFont;
    imgElem.setAttribute("src", currentImage);
}
```