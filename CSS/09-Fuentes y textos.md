# Fuentes.

[Ejemplos](https://github.com/Juan122113/CursoCSS/tree/main/08-Fuentes)

## Font family.

[Documentación oficial.](https://developer.mozilla.org/es/docs/Web/CSS/font-family)

Define una lista de fuentes para nuestros elementos. Acepta más de un valor.

font-family: verdana, cursive;

Al poner la coma estoy diciéndole que si verdana no se encuentra va a tomar la fuente cursiva. Y si se coloca otra coma más la palabra arial, entonces si no se encuentran las dos anteriores va a tomar la última fuente.

Entonces podemos decir que **font family** define una lista de fuentes con orden de prioridad según se encuentre la fuente. Este tipo de letra se agrega al elemento seleccionado per oes heredable.

No todas la computadoras tienen instaladas las mismas fuentes. Por ejemplo, si se usa verdana Visual Studio Code arroja distintas fuentes para esta propiedad. Si verdana no está en la computadora va a tomar la siguiente de la lista, en este caso Geneva, si esta no está va a tomar tahoma y si tahoma no está va a tomar sans-serif. Es poruqe son fuentes similares.

Si se necesita que la página tenga una fuente forzosamente, o sea, que se vea en todas las computadoras y en cualquier dispositivo móvil hay que ir a **Google Fonts** (https://fonts.google.com/). Este es un banco de fuentes gratuito. Allí debes seleccionar una fuente, luego debes seleccionar todos los estilos de la fuente seleccionada que se requieran. La recomendación es que se carguen todas las fuentes que se necesiten porque se van a tomar estas fuentes de un tercero y esto implica que se van a cargar datos a la página y puede que se haga un poco más lenta la carga de la página. Para tomar la fuente hay dos maneras: se puede copiar el código HTML y pegarlo en la etiqueta \<head>; o la otra opción es por medio de CSS, en la página de la fuente se selecciona el botón "import", se copia el contenido, se lo pega en la parte más superior del documento CSS, se borra la etiqueta \<style>, se regresa a Google Fons y se copia el contenido de "CSS rules to specify families" y se pega en body de CSS. Ahora se pueden cambiar los font-weight (tamaño/peso de la fuente) que se seleccionaron de la página de Google Fons.

## Font-weight.

[Documentación oficial.](https://developer.mozilla.org/es/docs/Web/CSS/font-weight)

Define el peso de una fuente. Es decir, define si la fuente, la cual tiene la propiedad, va a estar en negritas, normal o super delgada.

### Valores.

+ normal
+ bold -> negrita.
+ bolder
+ lighter

Pero no todas las fuentes tiene los pesos de fuente para soportar lighter y bolder. Solamente por defecto están: normal y bold.

También se pueden agregar los números que aparecen en Google Fonts como valores. 

## Font-style.

[Documentación oficial.](https://developer.mozilla.org/es/docs/Web/CSS/font-style)

Define el estilo de la fuente. Por defecto su valor es "normal".

## Font-size.

 [Documentación oficial.](https://developer.mozilla.org/es/docs/Web/CSS/font-size) 
 [Ejemplo.](https://github.com/Juan122113/CursoCSS/blob/main/01-introducci%C3%B3n-css/css/estilos.css)
  
Especifica la dimensión de la letra.

## Text-align.

[Documentación oficial.](https://developer.mozilla.org/en-US/docs/Web/CSS/text-align)

Permite definir la alineación horizontalmente del contenido del elemento. Mayormente se usa para textos e imágenes. Por defecto su valor es **start**, es decir, que va de izquierda a derecha; pero se puede poner __end__, que irá de derecha a izquierda; **center** que centrará el texto o __justify__ que justificará el texto.

## Line-height.

[Documentación oficial.](https://developer.mozilla.org/es/docs/Web/CSS/line-height)

Permite definir el tamaño de línea de los textos. Por defecto su valor es **normal** o lo que sería igual a 1.2 (esto varía entre navegadores por el user agent) pero también podemos usar píxeles que en este caso su valor igual serían 19.2px porque el valor de 1 equivale a 16px.

## Text-transform.

[Documentación oficial.](https://developer.mozilla.org/es/docs/Web/CSS/text-transform)
[Ejemplo.](https://github.com/Juan122113/CursoCSS)

Especifica el cambio entre mayúsculas y minúsculas del texto del elemento. Puede ser usada para que un texto aparezca completamente en mayúsculas, en minúsculas, o con la primera letra de cada palabra en mayúscula. Valores:

+ __uppercase__ -> sirve para indicar mayúsculas.


