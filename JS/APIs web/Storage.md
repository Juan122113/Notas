# Storage


[Documentación oficial](https://developer.mozilla.org/es/docs/Web/API/Storage)

La interfaz `Storage` de la API de almacenamiento web provee acceso al almacenamiento de la sesión o al almacenamiento local para un dominio en particular, permitiéndote, por ejemplo, añadir, modificar o eliminar elementos de datos almacenados.


<div id = "EjemploStorage"></div>

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


## Métodos


### Storage.getItem()


[Documentación oficial](https://developer.mozilla.org/es/docs/Web/API/Storage/getItem)

El método `getItem()` de la interfaz `Storage` devuelve el valor de la clave cuyo nombre se le pasa por parámetro.


#### Sintaxis


```js
var aValue = storage.getItem(keyName);
```


##### Parámetros


*`keyName`*
    Una `DOMString` que contiene el nombre de la clave cuyo valor se quiere obtener.


##### Devuelve


Una `DOMString` que contiene el valor de la clave.


#### Ejemplo


Ver [ejemplo de Storage](#EjemploStorage)


### Storage.setItem()


[Documentación oficial](https://developer.mozilla.org/es/docs/Web/API/Storage/setItem)

El método `setItem()` de la interfaz `Storage`, cuando reciba una clave y un valor, añadirá estos al almacén, o actualizará el valor si la clave ya existe.


#### Ejemplo


La siguiente función crea tres ítems dentro del almacenamiento local.

```js
function populateStorage() {
    localStorage.setItem("bgcolor", "red");
    localStorage.setItem("font", "Helvetica");
    localStorage.setItem("image", "myCat.png");
}
```


### Storage.removeItem()


[Documentación oficial](https://developer.mozilla.org/es/docs/Web/API/Storage/removeItem)

El método `removeItem()` de la interfaz `Storage` elimina la clave cuyo nombre recibe por parámetro del almacenamiento.


#### Sintaxis


```js
storage.removeItem(keyName);
```


##### Parámetros


***keyName***

    Una `DOMString` que contiene el nombre de la clave que se desea eliminar.


##### Devuelve


Ningún valor.


#### Ejemplo


```js
function populateStorage() {
    localStorage.setItem("bgcolor", "red");
    localStorage.setItem("font", "Helvetica");
    localStorage.setItem("image", "myCat.png");

    localStorage.removeItem("image");
}
```

De la misma manera funciona con `sessionStorage`.


### Storage.clear() 08/08


[Documentación oficial](https://developer.mozilla.org/es/docs/Web/API/Storage/clear)

El método `clear()`, al invocarlo, elimina todos los registros del almacén local.


#### Ejemplo


```js
function populateStorage() {
    localStorage.setItem("bgcolor", "red");
    localStorage.setItem("font", "Helvetica");
    localStorage.setItem("image", "myCat.png");

    localStorage.clear();
}
```