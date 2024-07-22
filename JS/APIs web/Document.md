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