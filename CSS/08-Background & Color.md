# Color.

[Documentación oficial.](https://developer.mozilla.org/es/docs/Web/CSS/color)
[Documentación oficial valores.](https://developer.mozilla.org/es/docs/Web/CSS/color_value)
[Ejemplos](https://github.com/Juan122113/CursoCSS/tree/main/07-Fondos%20y%20Colores)
Página web generadora de colores: https://coolors.co/

La propiedad color indica el color que tendrán los textos en los elementos.

## Palabras clave.

Hay muchas maneras de agregar colores en CSS. La **primer manera** es por medio de __palabras clave__ de los colores, por ejemplo; red, tomato, green, etc. 

## Rgb.

La **segunda manera** es por medio de __rgb__, **rgb** es un valor tipo función que nos permite definir un color en base de tres colores primarios: rojo, verde y azul o red, green y blue. __Rgb__ puede tener tres valores, es decir, su mínimo de valor que va a recibir son tres valores, que los separaremos por comas; el primero será el valor que represente al color rojo, el segundo al color verde y el tercero al color azul. Su valor permitido para cada parámetro es de 0 a 255, por ejemplo:

color: rgb(0, 0, 0); 
el color final en este caso sería negro.

color: rgb(255, 255, 255);
el color final en este caso sería blanco.

**Rgb** también admite un cuarto valor, la transparencia. Por defecto está en uno, que indica que no hay transparencia; el valor 0 indica la mayor transparencia, entre estos dos números se indica la transparencia deseada. Este valor también es conocido como valor alfa.

## Número hexadecimal.

La __tercer manera__ de agregar un color es con un **número hexadecimal**. Se basa en el sistema de numeración hexadecimal que parte desde el 0 hasta la letra f, siendo esta el mayor valor. En algunos casos se pueden usar mínimo tres valores, pero en la mayoría de casos se usan seis valores. Los primeros dos valores corresponden al color rojo, los dos siguientes al verdes y los dos últimos al azul. Esto es parecido a rgb, salvo que en este caso no se separan por comas. Antes del valor se escribe un numeral #.

color: #ff0000;
color: #f00
color rojo

## Hcl.

Hcl es el último valor que veremos. Es muy similar a rgb debido a que es una función y de igual manera requiere, mínimos, tres parámetros separados por comas, pero a diferencia de rgb cada valor representa algo distinto a un color. 

El primer valor es hue o también conocido como tono o matiz de color. Este valor va desde el 0 al 360. Estos valores se basan en el círculo cromático, o sea, se anota el valor del color que se quiera usar.

El segundo parámetro es la saturación o saturation. Esta se representa con porcentajes que van del 0 al 100%. Cuando está al 100% el color está totalmente saturado, cuando está al 0% está insaturado, es decir, es un color gris.

Está el tercer valor que es el lightnes o la luminosidad. De igual manera se utilizan porcentajes del 0 al 100%. El 100% indica un luminosidad completamente blanca y el 0% una luminosidad completamente negra. En este caso se recomienda siempre usarla al 50%.

Y por último hcl también acepta un cuarto valor igual es de alfa, es decir, la transparencia que va de 0 a 1. 1  es un elemento que no tiene transparencia y 0 es una transparencia total.

color: hsl(210, 100%, 50%, 1);

Aunque haya distintas formas de agregar colores todas tienen el mismo resultado.
Todo esto también sirve para cualquier propiedad que utilice colores, por ejemplo: **background-color**.

# Fondo.

[Ejemplos](https://github.com/Juan122113/CursoCSS/tree/main/07-Fondos%20y%20Colores)

En CSS podemos agregar fondos a los elementos esto se hace por medio de la propiedad __background__ [(documentación oficial)](https://developer.mozilla.org/es/docs/Web/CSS/background), esta propiedad es un shorthand de varias propiedades que permite modificar los fondos en CSS para los elementos. Solamente vamos a ver las propiedades más relevantes de **background**.

Se pueden agregar múltiples backgrounds agregándole más de un valor:

background-image: url(wave.svg), linear-gradient(135deg, #667eea  0%, #764ba2  100%);

## Background color.

[Documentación oficial.](https://developer.mozilla.org/es/docs/Web/CSS/background-color)

Permite agregar un color de fondo al elemento. Podemos agregar los colores que vimos anteriormente.

## Background image.

Es una propiedad que permite agregar imágenes de fondo a un elemento. Para agregar una imagen de fondo usamos la función url que me permite referenciar a las imágenes. Si la imagen es más pequeña que el elemento esta se repite.

También se pueden agregar gradientes para generar un degradé entre dos colores mediante el valor **linear-gradient**.

## Background-repeat.

[Documentación oficial.](https://developer.mozilla.org/es/docs/Web/CSS/background-repeat)

Para que la imagen de background image no se repita usamos background-repeat. Por defecto su valor es **repeat**. Para que no se repita se coloca __no-repeat__. También se puede colocar **repeat-x** para que se repita solamente en el eje x o __repeat-y__ para que se repita solamente en el eje y.

## Background-position.

[Documentación oficial.](https://developer.mozilla.org/es/docs/Web/CSS/background-position)

Permite posicionar la imagen. Tiene valores como: **top**, __left__, **right**, __bottom__ y **center**. Estos valores también se pueden combinar entre si.

## Background-size.

[Documentación oficial.](https://developer.mozilla.org/es/docs/Web/CSS/background-size)

Permite darle un tamaño a la imagen. Si se coloca un valor este aplica para el ancho y el alto. Si se colocan dos valores el primero aplica el ancho y el segundo al alto. También se usan palabras reservadas como valores, por ejemplo: 
+ __cover__ -> lo que hará es que la imagen se va a estirar al elemento, es decir, la imagen va a cubrir al elemento pero aunque la cubra habrá partes de la imagen que no se vean porque sobrepasan al elemento. Si no quieres eso se puede usar **contain**.
+ __contain__ -> ajusta perfectamente la imagen al elemento.

## Background-attachment.

[Documentación oficial.](https://developer.mozilla.org/es/docs/Web/CSS/background-attachment)
[Ejemplos](https://github.com/Juan122113/CursoCSS/tree/main/22-Landing%20page%20sunny/sunnyside-agency-landing-page-main)

Determina si la posición de la imagen de fondo será fija dentro de la pantalla o se desplazará con su bloque contenedor.
