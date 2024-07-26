# Node


[Documentación oficial](https://developer.mozilla.org/es/docs/Web/API/Node)

En el contexto del DOM (Document Object Model), un **Node** es una unidad básica de la estructura de un documento web. Es una clase base abstracta para varios tipos de objetos, permitiendo que se usen de manera similar e intercambiable. Los tipos de nodos incluyen:

- **Elementos (`element`)**
- __Documentos (`document`)__
- **Fragmentos de Documentos (`documentFragment`)**
- __Textos (`text`)__
- **Comentarios (`Comment` )**


## Propiedades de instancia.


### Node.textContent 06/28


[Documentación oficial](https://developer.mozilla.org/es/docs/Web/API/Node/textContent)

[Ejemplo](https://github.com/Juan122113/beginner-html-site-styled-gh-pages/blob/main/scripts/main.js)

La propiedad `texContent` de la interfaz `Node` representa el contenido de texto de un nodo y sus descendientes.


#### Ejemplo.


```js
// Dado el siguiente fragmento HTML:
// <div id="divA">Esto <span>es</span> un texto</div>

// Lee el contenido textual:
var text = document.getElementById("divA").textContent;
// |text| contiene la cadena "Esto es un texto".

// Escribe el contenido textual:
document.getElementById("divA").textContent = "Esto es un nuevo texto";
// EL HTML "divA" ahora contiene una nueva cadena:
//    <div id="divA">Esto es un nuevo texto</div>
```