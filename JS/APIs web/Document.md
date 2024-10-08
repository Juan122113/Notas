# Document


[Documentación oficial](https://developer.mozilla.org/es/docs/Web/API/Document)

La interfaz `Document` representa cualquier página web cargada en el navegador y sirve como punto de entrada al contenido de la página web, que es el árbol DOM (Document Object Model).


## Constructor.


`Document()`
	Crea un nuevo objeto `Document`


## Métodos.


### Document.querySelector()


[Documentación oficial](https://developer.mozilla.org/es/docs/Web/API/Document/querySelector)

Devuelve el primer elemento del documento que coincida con el grupo especificado de selectores.


#### Sintaxis.


```js
element = document.querySelector(selectores);
```

Donde:

- `element` es un objeto de tipo element.
- `selectores` es una cadena de caracteres que contiene uno o más selectores CSS separados por coma (funciona con un selector de HTML también).


#### Ejemplo.


En este ejemplo, obtendremos el primer elemento del documento con la clase "miClase":

```js
var el = document.querySelector(".miClase");
```


### Document.getElementById()


[Documentación oficial.](https://developer.mozilla.org/es/docs/Web/API/Document/getElementById)

Devuelve una referencia al elemento por su ID.


#### Sintaxis


```js
elemento = document.getElementById(id);
```


##### Parámetros


`id`

Es una cadena sensible a mayúsculas referida al ID único del elemento buscado.


##### Valor Retornado


`element`

Es una referencia a un objeto `Element`, o `null` si un elemento con el ID especificado no se encuentra en el documento.


#### Ejemplo


##### HTML


```html
<html>
	<head>
		<title>Ejemplo getElementById</title>
	</head>
	<body>
		<p id="para">Cualquier texto acá</p>
		<button onclick="changeColor('blue');">Azul</button>
		<button onclick="changeColor('red');">Rojo</button>
	</body>
</html>
```


##### JavaScript


```js
function changeColor(newColor) {
	var elem = document.getElementById("para");
	elem.style.color = newColor;
}
```