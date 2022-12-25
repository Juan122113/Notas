# Metodología BEM.

[Documentación oficial](https://getbem.com/)
Ejemplos: [PDF](https://github.com/Juan122113/CursoCSS/blob/main/04-BEM/BEM.pdf) - [HTML](https://github.com/Juan122113/CursoCSS/blob/main/04-BEM/BEM.html) - [CSS](https://github.com/Juan122113/CursoCSS/blob/main/04-BEM/BEMestilos.css)

BEM (Block Element Modifier) es una metodología que nos proporciona una manera de nombrar a nuestras clases en HTML para posteriormente usarlas en CSS. BEM nos ayudará a mantener nuestro código flexible, modular y sencillo. Sobre todo, nos ayudará a lidiar con problemas sobre especificidad.
BEM significa Block Element Modifier, esto es debido a que estas siglas componen la manera de nombrar en BEM.

## Bloque.

Es una parte independiente en nuestro HTML, no necesita de otros elementos para existir. Por ejemplo, una galería de imágenes o un menú, no necesitan de otros elementos para existir.
Los bloques tienen el nombre de lo que representará, ejemplo "header, menu, galeria, footer". Ejemplo:

~~~
<section class="gallery">

</section>
~~~

## Elementos.

Los elementos están ligados a los bloques. Un elemento siempre estará dentro de un bloque, debido a que es parte de él y es dependiente del bloque, por ejemplo una imagen necesita de una galería de imágenes para existir, o un enlace necesita de un menú para existir.
Los elementos tendrán el nombre primero de el bloque al que pertenece, dos guiones bajos y después el nombre de lo que representará. Ejemplo: "header__title, menu__item, galeria__img, footer__img"

\<section class="gallery">
   \<img src"" class="gallery__img">
\</section>

## Modificador.

Los modificadores son usados en elementos o bloques, se usan para representar una característica diferente que tendrá el bloque o elemento.
Lo modificadores tendrán el nombre del bloque o del elemento, después otra vez el nombre del elemento o bloque, dos guiones medios y la característica diferente que tendrá este bloque o elemento. Ejemplo: "boton--active" "header--wave"

\<button class="btn">Dame click\</button>
\<button class="btn">Dame click\</button>
\<button class="btn btn--active">Dame click\</button>
