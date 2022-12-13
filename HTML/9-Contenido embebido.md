# ¿Qué es el contenido embebido?

[Ejemplo de inserción de contenido embebido en http.](https://github.com/Juan122113/curso-html-2022/blob/main/contenido-embebido/contenido%20embebido.html)

+ El contenido embebido es todo el contenido que nos traemos desde fuera (imágenes, video, audio, etc.).
+ Estos archivos son los que más peso (tamaño) añaden a un sitio web.
+ Los tipos más conocidos son:
    + Imágenes
    + Audio
    + Video
    + Iframes (no son en sí contenido embebido, pero sí es contenido que se trae desde fuera)

## Imágenes

**\<img>** -> Son las que más se utilizan y son las que más problemas suelen traer. [Documentación oficial.](https://developer.mozilla.org/es/docs/Web/HTML/Element/img)

+ Los formatos de imágenes para web los podemos clasificar en 2 tipos:
    + Vectoriales:
        + svg -> formato de archivo vectorial que solo se abre en un navegador (recomendado siempre que se pueda). Se puede insertar en HTML a través de **\<img>** o copiando y pegando todo su código. SI se necesita trabajar con el svg a través de CSS o JavaScript para hacer algún tipo de programación o modificación del mismo en tiempo real, entonces se debe copiar y pegar todo el código.
    + Mapa de bits:
        + jpg -> formato más comprimido pero no soporta animaciones ni transparencias.
        + png 8 y 24 (si necesitáis transparencias)
        + gif (si necesitais una imágen animada)
        + webp -> el formato que menos pesa y principalmente para web. [Documentación oficial.](https://developers.google.com/speed/webp) - [Conversor de imágenes webp.](https://imagen.online-convert.com/es/convertir-a-webp)

### Diferencia entre svg y una imágen de mapa de bits.

+ Las __imágenes de mapa de bits__ cuando se hace zoom pierde calidad, los **svg** no.
+ Las __imágenes de mapa de bits__ aregan peso a la web, los **svg** no.

### Atributos.

+ **src** -> La ruta de donde está nuestra imagen. El URL de la misma.
+ **alt** -> Es obligatorio. Lo que tenemos que poner es la representación de la imagen o lo que queremos transmititr con esa imagen. Si no lo ponemos también funciona pero aparece un error de la W3C.
+ **srcset** -> Es un set de links de donde puede cargar las imágenes en función de una condición. Existe la posibilidad de que el navegador sea muy antiguo y no soporte **srcset**, entonces se debe agregar **src**. [Documentación oficial](https://developer.mozilla.org/es/docs/Learn/HTML/Multimedia_and_embedding/Responsive_images) (Imágenes adaptables).

### Etiqueta picture.

**\<picture>\</picture>** -> Es una tecnología más moderna y experimental pero está soportada por los navegadores principales. Funciona como __srcset__ pero con más opciones. Hay que agregarle una etiqueta \<img  src="/contenido-embebido/assets/images/Gamer.jpg"  alt="Gamer"> para que tenga una copia "por si acaso", si no no hace nada, si es que el navegador no lo soporta. [Documentación oficial.](https://developer.mozilla.org/es/docs/Web/HTML/Element/picture)
Dentro de **picture** se le agrega la etiqueta **\<source>** que lleva los atributos __srcset__ y __media__.

#### Atributos

**media** -> Para indicar el ancho en el  que queramos que funcione.

## Audio.

Para introducirlo solo hay que agregar la etiqueta **\<audio>\</audio>**. [Documentación oficial.](https://developer.mozilla.org/es/docs/Web/HTML/Element/audio)

### Atributos.

+ **src** -> La ruta de donde está nuestro audio. El URL del mismo.
+ **controls** -> Sirve para poder ver un reproductor. Es un atributo booleano.
+ **autoplay** -> Hace que el archivo se reproduzca automáticamente al cargar la página. Sin embargo los navegadores actuales están bloqueando el autoplay siempre y cuando el contenido no esté silenciado.
+ **muted** -> Sirve para tener el contenido silenciado. De esa forma el autoplay no se bloquearía.
+ **loop** -> Sirve para que el archivo se vuelva a reproducir una vez que termine.

## Video.

Sirve para insertar un video dentro del documento html. Es muy parecido a audio. **\<video>\</video>**[Documentación oficial.](https://developer.mozilla.org/es/docs/Web/HTML/Element/video)

### Atributos.

+ **src** -> La ruta de donde está nuestro video. El URL del mismo.
+  **controls** -> Sirve para poder ver un reproductor. Es un atributo booleano.
+  **autoplay** -> Hace que el archivo se reproduzca automáticamente al cargar la página. Sin embargo los navegadores actuales están bloqueando el autoplay siempre y cuando el contenido no esté silenciado.
+ **muted** -> Sirve para tener el contenido silenciado. De esa forma el autoplay no se bloquearía.
+ **loop** -> Sirve para que el archivo se vuelva a reproducir una vez que termine.
+ **poster** -> Sirve para indicar cual va a ser nuestra imagen inicial.

## Iframes.

**\<iframe>\</iframe>** Básicamente es tomar una web e introducirla dentro de la nuestra. Por ejemplo, en un video de YouTube, cuando se aprieta el botón compartir, la primera opción es insertar, al hacer click YouTube nos proporciona un iframe. Pasa con un montón de páginas que dan componentes para nuestra web. El problema que tienen es que si vemos los que tienen dentro es demasiado contenido que agrega mucho tiempo de carga a la página.[Documentación oficial.](https://developer.mozilla.org/es/docs/Web/HTML/Element/iframe)

### Atributos básicos.

+ **width** -> Ancho.
+ **height** -> Alto.
+ **src** -> La ruta de donde está nuestro iframe. El URL del mismo.

## Etiqueta figure.

**\<figure>\</figure>** Sirve para meter contenido relacionado pero que es opcional que esté. [Documentación oficial.](https://developer.mozilla.org/es/docs/Web/HTML/Element/figure)
La etiqueta __\<figcaption>\</figcaption>__ sirve para agregar un texto debajo o encima de la imagen, tabla, fragmento de código, etc., dependiendo donde se escriba el código respectivamente.

[Ejemplo de inserción de contenido embebido en http.](https://github.com/Juan122113/curso-html-2022/blob/main/contenido-embebido/contenido%20embebido.html)



