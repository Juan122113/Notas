
# \<head>\</head>

El elemento head de un documento HTML  es la parte que no se muestra en el navegador cuando se carga la página. Contiene información como el título (\<title>) de la página, enlaces al CSS, enlaces para personalizar favicon, y otros metadatos. [Documentación oficial.](https://developer.mozilla.org/es/docs/Learn/HTML/Introduction_to_HTML/The_head_metadata_in_HTML)

## Metadatos: el elemento \<meta>.

**\<meta>** Los metadatos son datos que describen datos, y HTML tiene una forma "oficial" de introducir metadatos en un documento, el elemento \<meta>. 

[Ejemplos de etiquetas meta.](https://github.com/Juan122113/curso-html-2022/blob/main/meta/index.html)

### Atributos.

La mayoría tienen un:
+ **name** -> Que hace referencia a qué tipo de metadato le estamos dando al navegador y cual es el contenido de ese metadato.
+ **content** -> Contenido.

### Diferentes tipos.

**description** -> Breve descripción de la página. Es lo que aparece en google debajo del título de la web.
**author** -> Donde se indica el autor de la web.

### Open Graph Protocol

Es un protocolo que creó facebook principalmente para poder elegir cuando compartimos nuestro sitio web qué es lo que se muestra en esa publicación. Por ejemplo: cuando compartimos un link en facebook, debajo del mismo aparece una imagen, el título, una url y una descripción, que salga esta información es gracias a este protocolo. Este protocolo afecta a practicamente todo lo que compartimos, whatsap, instagram, en un blog, en cualquier sitio donde podamos compartir links (twitter no porque tiene su propio protocolo) este es el protocolo que dicta el contenido que se va a ver. Es importante ponerlo en nuestras páginas porque si no lo ponemos, el propio facebook o la propia plataforma serán las que decidan qué contenido se va a mostrar. Y si no encuentra ninguno, simplemente pondrá el link solamente. [Documentación oficial.](https://ogp.me/)

###  Twitter card.

Es básicamente lo mismo que open graph protocol pero exclusivo para twitter. Si no se lo usa, este protocolo lee las propiedades equivalentes de open graph; pero no todas las propiedades de twitter están contenidas en open graph. [Documentación oficial.](https://developer.twitter.com/en/docs/twitter-for-websites/cards/overview/abouts-cards) - [Validación del código de la twitter card.](https://cards-dev.twitter.com/validator)

## Favicon.

Abreviatura de **favorite icon** (**ícono favorito**). Enriquece el diseño del sitio, son referencias a íconos personalizados.
Para hacerlo bien, hacerlo también para navegadores desactualizados, para móviles, apple, etc., hay que ir a la página https://www.favicon-generator.org/ para generar todos los íconos correspondientes, también genera las etiquetas.

#### [Fontawesome.](https://fontawesome.com/)

Es una librería de iconos, de las más usadas del mundo. Para usarla hay que poner un código dado por la página en el \<head> del documento html (`<script  src="https://kit.fontawesome.com/b9dac75233.js"  crossorigin="anonymous"></script>`). Luego se elige el icono preferido y se ingresa a la página del mismo, se hace click en la etiqueta html para copiarla y se la pega en el body. [Ejemplo.](https://github.com/Juan122113/curso-html-2022/blob/main/meta/iconos.html)

## Accesibilidad.

Es el hecho de poder hacer una página web que sea accesible para todo el mundo, independientemente que si pueden verla o no.

### Atributos.

+ **tabindex** -> Permite al usuario moverse por la página en determinado orden.
+ **rol** -> Especialment diseñado para gente invidente que usa navegadores por voz. Le da al navegador información sobre qué tipo de elemento estamos posicionándonos.
+ **aria** -> Especialment diseñado para gente invidente que usa navegadores por voz. Da más información al usar un navegador de voz. 
[Ejemplos de lo visto en accesibilidad.](https://github.com/Juan122113/curso-html-2022/blob/main/meta/accesibilidad.html)
Documentación oficial:
    + [Especificación de la w3c.](https://www.w3.org/WAI/ARIA/apg/)
    + [Especificación de la mdn.](https://developer.mozilla.org/es/docs/Web/Accessibility/ARIA)
    + [Documentación de google.](https://web.dev/semantics-aria/)
    + [Post sobre ARIA.](https://www.lullabot.com/articles/what-heck-aria-beginners-guide-aria-accessibility)

