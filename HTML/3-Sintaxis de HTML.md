
# Sintaxis de HTML

Index.html: Lo normal al nombrar un archivo html.

## Etiquetas

**\<etiqueta>contenido de la etiqueta\</etiqueta>**: etiqueta de apertura y de cierre con la barra, en el medio de las dos es donde va el contenido.

### Estructura de un sitio web

+ **\<!DOCTYPE html>** -> Esta etiqueta define el estadar de documento que estamos siguiendo. Representa que estamos siguiendo el estandar HTML5. [Documentación oficial.](https://developer.mozilla.org/es/docs/Web/HTML/Element/html) - [Ejemplo.](https://github.com/Juan122113/curso-html-2022/blob/main/index.html)
+ **\<!--Contenido-->** -> Etiqueta para generar un comentario informativo.  [Ejemplo.](https://github.com/Juan122113/curso-html-2022/blob/main/index.html)
+ **\<head>\</head>** -> Representa una colección de datos o metadatos del documento. [Documentación oficial.](https://developer.mozilla.org/es/docs/Web/HTML/Element/head) - [Ejemplo.](https://github.com/Juan122113/curso-html-2022/blob/main/index.html)
+ **\<title>\</title>** -> Representa lo que aparece en la pestaña de la página web. Estas dos últimas etiquetas son datos que le pasamos al navegador con información de nuestra página web. El elemento title define el título del documento que se muestra en un browser la barra título o la pestaña de una página. [Documentación oficial.](https://developer.mozilla.org/es/docs/Web/HTML/Element/title) - [Ejemplo.](https://github.com/Juan122113/curso-html-2022/blob/main/index.html)
+ **\<body>\</body>** -> Representa todo el contenido del nuestra página web. [Documentación oficial.](https://developer.mozilla.org/es/docs/Web/HTML/Element/body) - [Ejemplo.](https://github.com/Juan122113/curso-html-2022/blob/main/index.html)
+ **\<p>\</p>** -> El elemento p (párrafo) es el apropiado para distribuir el texto en párrafos. [Documentación oficial.](https://developer.mozilla.org/es/docs/Web/HTML/Element/p) - [Ejemplo.](https://github.com/Juan122113/curso-html-2022/blob/main/titulos-y-parrafos.html)


#### Etiquetas de sección de contenido.

+ **\<header>\</header>** -> El elemento de header representa un grupo de ayudas introductorias o de navegación. Puede contener algunos elementos de encabezado, menú de navegación, el logotipo de la página, redes sociales... Ejemplo: 
\<header>Inicio
Novelas
Películas
Contacto\</header>
[Documentación oficial.](https://developer.mozilla.org/es/docs/Web/HTML/Element/header) - [Ejemplo.](https://github.com/Juan122113/curso-html-2022/blob/main/seccion-de-contenido.html)
+ __\<nav>\</nav>__ -> representa una sección de una página cuyo propósito es proporcionar enlaces de navegación, ya sea dentro del documento actual o a otros documentos. Ejemplos comunes de secciones de navegación son menús, tablas de contenido e índices. [Documentación oficial.](https://developer.mozilla.org/es/docs/Web/HTML/Element/nav) - [Ejemplo.](https://github.com/Juan122113/CursoCSS/blob/main/20-Men%C3%BA%20CSS/index.html)
 + **\<main>\</main>** -> Representa el contenido principal del body de un documento o aplicación. [Documentación oficial.](https://developer.mozilla.org/es/docs/Web/HTML/Element/main) - [Ejemplo.](https://github.com/Juan122113/curso-html-2022/blob/main/seccion-de-contenido.html)
+ **\<footer>\</footer>** -> El pie de página. [Documentación oficial.](https://developer.mozilla.org/es/docs/Web/HTML/Element/footer) - [Ejemplo.](https://github.com/Juan122113/curso-html-2022/blob/main/seccion-de-contenido.html)
+ **section** -> Es un contenedor genérico que agrupa contenido que está relacionado. Cuando creamos bloques cuyo contenido es parte de un bloque total usaremos section. [Documentación oficial.](https://developer.mozilla.org/es/docs/Web/HTML/Element/section) - [Ejemplo.](https://github.com/Juan122113/curso-html-2022/blob/main/seccion-de-contenido-II.html)
+ **article** -> Es un contenedor que representa contenido independiente, es decir, podemos leer ese fragmento en cualquier otro sitio y tendría sentido por sí mismo. [Documentación oficial.](https://developer.mozilla.org/es/docs/Web/HTML/Element/article) - [Ejemplo.](https://github.com/Juan122113/curso-html-2022/blob/main/seccion-de-contenido-II.html)
+ **aside** -> se utiliza para representar contenido relacionado pero que no forma parte del contenido principal. [Documentación oficial.](https://developer.mozilla.org/es/docs/Web/HTML/Element/aside) - [Ejemplo.](https://github.com/Juan122113/curso-html-2022/blob/main/seccion-de-contenido-IV.html)

#### Elementos títulos

Los elementos de **encabezado** implementan seis niveles de encabezado del documento, \<h1> es el más importante, y \<h6> el menos importante.
+ \<h1>\</h1>
+ \<h2>\</h2>
+ \<h3>\</h3>
[Documentación oficial.](https://developer.mozilla.org/es/docs/Web/HTML/Element/Heading_Elements) - [Ejemplo.](https://github.com/Juan122113/curso-html-2022/blob/main/titulos-y-parrafos.html)

#### Elementos de bloque

Todo lo visto hasta ahora se denominan elementos de bloque(?). Los elementos de bloque van a ocupar todo el ancho disponible aunque su contenido no lo haga, por lo que los elementos que pongamos a continuación saltarán a la siguiente línea. [Ejemplo.](https://github.com/Juan122113/curso-html-2022/blob/main/elementos-de-bloque.html)

##### Otras etiquetas de bloque.

**\<addres>\</addres>** -> Se utiliza para aportar información de contacto para el article más cercano o para todo el body. Ej: Sirve para anotar una dirección. [Documentación oficial.](https://developer.mozilla.org/es/docs/Web/HTML/Element/address) [Ejemplos de otras etiquetas de bloque.](https://github.com/Juan122113/curso-html-2022/blob/main/otras-etiquetas-bloque.html)

**\<blockquote>\</blockquote>** -> Crea citas en bloque, marca las citas a otros autores o documentos. Se utiliza para marcar las citas a otros autores o documentos. Se puede incluir el atributo cite para poner un enlace al documento original o fuente; esto no genera un enlace, solo queda como información para el navegador, solo queda en el código, no se vé en el HTML. [Documentación oficial.](https://developer.mozilla.org/es/docs/Web/HTML/Element/blockquote)

**pre** -> Representa texto preformateado. Se utiliza para tener código preformateado que necesita ser representado igual que se escribió. O sea, en el documento HTML queda igual como se escribió en el código. Los espacios dentro de este elemento también son mostrados como están escritos.[Documentación oficial.](https://developer.mozilla.org/es/docs/Web/HTML/Element/pre)

**\<div>\</div>** -> Sirve para crear secciones o agrupar contenidos. Se usa como división del documento, semánticamente no significa nada, es un contenedor genérico que se usa generalmente para dar estilos a través de css o para usar algo denominado "delegación de eventos" en javascript. Se usa para dividir contenido. [Documentación oficial.](https://developer.mozilla.org/es/docs/Web/HTML/Element/div) __Atributos:__
+ **class** -> es una lista de las clases del elemento separada por espacios. Las clases permiten a CSS y Javascript seleccionar y acceder a elementos específicos a través de los selectores de claseo funciones. [Documentación oficial.](https://developer.mozilla.org/es/docs/Web/HTML/Global_attributes/class) - [Ejemplo.](https://github.com/Juan122113/CursoCSS/blob/main/01-introducci%C3%B3n-css/index.html)
+ **style** -> contiene declaraciones de estilo CSS a ser aplicados a un elemento. [Documentación oficial.](https://developer.mozilla.org/es/docs/Web/HTML/Global_attributes/style) - [Ejemplo.](https://github.com/Juan122113/CursoCSS/blob/main/01-introducci%C3%B3n-css/index.html)

**\<hr>** -> horizontal rule, se utiliza para decirle al navegador que vamos a cambiar de tema. [Documentación oficial.](https://developer.mozilla.org/es/docs/Web/HTML/Element/hr) [Ejemplos de otras etiquetas de bloque.](https://github.com/Juan122113/curso-html-2022/blob/main/otras-etiquetas-bloque.html)

#### Elementos de línea

+ **em** -> emphasis. Es el apropiado para marcar con énfasis las partes importantes de un texto. Si, por ejemplo al texto del párrafo se le diera un número simbolico de 0, lo que está dentro de em tendría un valor de 1. [Documentación oficial.](https://developer.mozilla.org/es/docs/Web/HTML/Element/em) - [Ejemplo.](https://github.com/Juan122113/curso-html-2022/blob/main/elementos-de-linea.html)
+ **strong** -> más énfasis. Idem anterior pero con un valor de 2. Es el apropiado para marcar con especial énfasis las partes más importantes de un texto.[Documentación oficial.](https://developer.mozilla.org/es/docs/Web/HTML/Element/strong) - [Ejemplo.](https://github.com/Juan122113/curso-html-2022/blob/main/elementos-de-linea.html)
+ **small** -> menos énfasis que el texto normal. Idem anterior pero con un valor de -1. Hace el tamaño del texto una talla más pequeña (por ejemplo, de largo a mediano, o de pequeño a extra pequeño) que el tamaño mínimo de fuente del navegador. [Documentación oficial.](https://developer.mozilla.org/es/docs/Web/HTML/Element/small) - [Ejemplo.](https://github.com/Juan122113/curso-html-2022/blob/main/elementos-de-linea.html)
+ **br** -> forzar un salto de línea. [Documentación oficial.](https://developer.mozilla.org/es/docs/Web/HTML/Element/br) - [Ejemplo.](https://github.com/Juan122113/curso-html-2022/blob/main/elementos-de-linea.html)
+ **wbr** -> Salto de línea si hiciera falta. Word break opportunity representa una posición dentro del texto donde el explorador puede opcionalmente saltar una línea, aunque sus reglas de salto de línea de otra manera no crearían un salto en esa posición.Ejemplo: en links: C:\\\<wbr>Users\\\<wbr>Ammiel\\\<wbr>Desktop\\\<wbr>cursos\\\<wbr>html\\\<wbr>curso-html-2022\\\<wbr>elementos\\\<wbr>elementos-de-linea.html. [Documentación oficial.](https://developer.mozilla.org/es/docs/Web/HTML/Element/wbr) - [Ejemplo.](https://github.com/Juan122113/curso-html-2022/blob/main/elementos-de-linea.html)
+ **time** -> Se usa para representar un contenido de hora/fecha. Representa un periodo específico en el tiempo. Puede incluir el atributo datetime para convertir las fechas en un formato interno legible por un ordenador, permitiendo mejores resultados en los motores de búsqueda o características personalizadas como recordatorios. [Documentación oficial.](https://developer.mozilla.org/es/docs/Web/HTML/Element/time) - [Ejemplo.](https://github.com/Juan122113/curso-html-2022/blob/main/elementos-de-linea.html)
+ **i** -> italic o cursiva. [Documentación oficial.](https://developer.mozilla.org/es/docs/Web/HTML/Element/i) - [Ejemplo.](https://github.com/Juan122113/curso-html-2022/blob/main/elementos-de-linea.html)
+ **b** -> bold, negrita. [Documentación oficial.](https://developer.mozilla.org/es/docs/Web/HTML/Element/b) - [Ejemplo.](https://github.com/Juan122113/curso-html-2022/blob/main/elementos-de-linea.html)
+ **u** -> underline. Muestra el texto subrayado. [Documentación oficial.](https://developer.mozilla.org/es/docs/Web/HTML/Element/u) - [Ejemplo.](https://github.com/Juan122113/curso-html-2022/blob/main/elementos-de-linea.html)
+ **sup** -> define un fragmento de texto que se debe mostrar, por razones tipográficas, más alto, y generalmente más pequeño, que el tramo principal del texto, es decir, en superíndice. [Documentación oficial.](https://developer.mozilla.org/es/docs/Web/HTML/Element/sup) - [Ejemplo.](https://github.com/Juan122113/curso-html-2022/blob/main/elementos-de-linea.html)
+ **sub** -> define un fragmento de texto que se debe mostrar, por razones tipográficas, más bajo, y generalmente más pequeño, que el tramo principal del texto, es decir, en subíndice. [Documentación oficial.](https://developer.mozilla.org/es/docs/Web/HTML/Element/sub) - [Ejemplo.](https://github.com/Juan122113/curso-html-2022/blob/main/elementos-de-linea.html)

##### Otras etiquetas de línea.

**\<span>\</span>** -> Es un contenedor de línea, equivalente a div, se suele usar para encerrar palabras o pequeños textos y darles estilo a través de CSS o localizarlos desde javascript. Semánticamente no sinifica nada. [Documentación oficial.](https://developer.mozilla.org/es/docs/Web/HTML/Element/span) [Ejemplos de otras etiquetas de línea.](https://github.com/Juan122113/curso-html-2022/blob/main/otras-etiquetas-linea.html)

**\<q>\</q>** -> Es el equivalente a blockquote, significa quote, por eso el de bloque se llama block-quote. Sirve para poner citas pero en línea. Este elemento está destinado a citas breves que no requieren de saltos de párrafo. [Documentación oficial.](https://developer.mozilla.org/es/docs/Web/HTML/Element/q)

**\<code>\</code>** -> Sirve para encerrar código que queremos representar visualmente, suele ir unido con la etiqueta pre. [Documentación oficial.](https://developer.mozilla.org/es/docs/Web/HTML/Element/code) [Ejemplos de otras etiquetas de línea.](https://github.com/Juan122113/curso-html-2022/blob/main/otras-etiquetas-linea.html)


[Entidades especiales en HTML - Codigo ASCII.](https://ascii.cl/es/codigos-html.htm)


