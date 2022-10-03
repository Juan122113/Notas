# Sintaxis de Markdown
## Elementos de bloque

### Párrafos y saltos de línea

Parrafo: Para generar uno nuevo simplemente separa el texto mediante una línea en blanco **(pulsando dos veces intro)**

Así

Salto de línea: Para realizarlo y empezar **una frase en una línea siguiente dentro del mismo párrafo**, tendrás que pulsar **dos veces la barra espaciadora antes de pulsar una vez intro**.  
Así

### Encabezados

Las `#` **almohadillas** son uno de los métodos utilizados en Markdown para crear encabezados. Debes usarlos añadiendo **uno por cada nivel**.

Es decir,

# Encabezado 1
## Encabezado 2
### Encabezado 3
#### Encabezado 4
##### Encabezado 5
###### Encabezado 6

También puedes cerrar los encabezados con el mismo número de almohadillas, por ejemplo escribiendo 
### Encabezado 3 ###
 Pero la única finalidad de esto es un **motivo estético**.

Existe otra manera de generar encabezados, aunque este método está **limitado a dos niveles**.

Consiste en _subrayar_ los encabezados con el símbolo `=` (para el encabezado 1), o con guiones `-` para el encabezado 2.

Encabezado 1
===
Encabezado 2
---

No existe un número concreto `=` o `-` que necesites escribir para que esto funcione, ¡incluso bastaría con uno!

Encabezado 1
=
Encabezado 2
-

### Citas

Las citas se generan utilizando el carácter _mayor que_ `>` al comienzo del bloque de texto.
> Un país, una civilización se puede juzgar por la forma en que trata a sus animales.  — Mahatma Gandhi

Si la cita en cuestión se compone de **varios párrafos**, deberás añadir el mismo símbolo `>` al comienzo de cada uno de ellos.
>Creo que los animales ven en el hombre un ser igual a ellos que ha perdido de forma extraordinariamente peligrosa el sano intelecto animal.
>Es decir, que ven en él al animal irracional, al animal que ríe, al animal que llora, al animal infeliz. — Friedrich Nietzsche

Incluso puedes concatenar varios `>>` para crear **citas anidadas**.
> Esto sería una cita como la que acabas de ver
> 
> >Dentro de ella puedes anidar otra cita
>
> La cita principal llegaría hasta aquí

### Listas
#### Listas desordenadas

Para crear **listas desordenadas** utiliza **`*` asteriscos, `-` guiones, o `+` símbolo de suma**.
* Elemento de lista 1
* Elemento de lista 2
- Elemento de lista 3
- Elemento de lista 4
+ Elemento de lista 5
+ Elemento de lista 6

Para generar **listas anidadas** dentro de otras, simplemente tendrás que añadir **cuatro espacios en blanco antes del siguiente `*`, `-` o `+`.
- Elemento de lista 1
- Elemento de lista 2
    - Elemento de lista 3
    - Elemento de lista 4
        - Elemento de lista 5
        - Elemento de lista 6

#### Listas ordenadas
Para crear listas ordenadas debes utilizar la sintaxis de tipo: _«número.»_ `1.`
1. Elemento de lista 1
2. Elemento de lista 2
    + Elemento de lista 3
    + Elemento de lista 4
        1. Elemento de lista 5
        2. Elemento de lista 6

### Códigos de bloque

Si quieres crear un bloque entero que contenga código. Lo único que tienes que hacer es **encerrar dicho párrafo entre dos líneas formadas por tres `~` virgulillas**.
~~~
Creando códigos de bloque.
Puedes añadir tantas líneas y párrafos como quieras.  
~~~

### Reglas horizontales

Para crearlas, en una línea en blanco deberás incluir **tres de los siguientes elementos**: asteriscos, guiones, o guiones bajos.

***
---
___

También puedes separarlos mediante un espacio en blanco por pura estética.

* * *
- - - 
_ _ _


## Elementos de línea

### Énfasis (negritas y cursivas)

Markdown utiliza **asteriscos** o **guiones bajos** para enfatizar.
Simplemente tendrás que envolver palabras o textos en éstos símbolos para conseguir _cursivas_ o **negritas**.

*cursiva*
_cursiva_
**negrita**
__negrita__

Por supuesto si quieres utilizar los dos tipos de énfasis no tienes más que **_combinar la sintaxis_**, envolviendo la palabra entre tres asteriscos o tres guiones bajos.

***cursiva y negrita***
___cursiva y negrita___

### Links o enlaces

#### Links o enlaces en línea

Son los enlaces de toda la vida. Como su nombre indica, se encuentran en línea con el texto.
Se crean escribiendo la palabra o texto enlazada entre `[]` **corchetes**, y el link en cuestión entre `()` **paréntesis**.
[enlace en línea](http://www.google.com)

#### Links o enlaces como referencia

La desventaja del método anterior, es que si utilizas links demasiado complejos o largos pueden dificultarte la lectura de tu texto.

Para solucionarlo y crear tu contenido de una manera más ordenada puedes generar enlaces de referencia.

Esto quiere decir que en tu texto enlazarás **_palabras o códigos concretos_** (formados por letras y/o números), que en otro lugar más apartado de tu documento tendrás definidos como determinadas URL.

[nombre que quieres darle a tu enlace][nombre de tu referencia]

[nombre de tu referencia]: http://www.google.com

Esto se ve más claro con un ejemplo.

Me llamo Javier Cristobal y tengo un blog sobre [productividad mac][blog]

En dicha [web][blog] recopilo artículos sobre todo lo relacionado a automatización, gestión y eficiencia.

[blog]: http://www.leagueoflegends.com

La referencia `[blog]` puede estar incluida en cualquier parte del documento, así puedes organizarte mejor y de una manera más _limpia_, recopilando todas tus referencias en un mismo lugar.

#### Links automáticos

Verás esta forma **dentro de elementos varios**

### Código

En según que tipo de publicaciones (sobre todo las de carácter técnico), necesitarás añadir pequeñas secciones donde mostrar código de otro lenguaje, atajos de teclado, o demás contenido que no debería ser tratado como tal.

Para ello tienes disponible dos alternativas.

#### Código puro `<code>`

La forma más sencilla de escribir código en Markdown es envolver el texto entre dos comillas sencillas ` (Se le denomina acento grave, es la tilde pero escrita al revés: alt+96)

`Esto es una línea de código`

#### Texto preformateado `<pre>`

La otra manera de añadir código en Markdown es **comenzar el párrafo con cuatro espacios en blanco**.

    Esto es una línea de código

Ojo, ¡estos espacios deberás incluirlos **en cada línea que escribas**! Para añadir código en bloque es mejor utilizar la sintaxis que viste anteriormente:

### Imágenes

Insertar una imagen con Markdown se realiza de una manera prácticamente idéntica a insertar [links](https://markdown.es/sintaxis-markdown/#links).

Solo que en este caso, deberás añadir un símbolo de **`!` exclamación** al principio y el **enlace** no será otro que **la ubicación de la imagen**.

![Texto alternativo](ruta/a/la/imagen.jpg)

El _texto alternativo_ es lo que se mostraría si la carga de la imagen fallase.

También podrás añadir un **título alternativo** entrecomillándolo al final de la ruta. Esto sería el título mostrado al dejar el cursor del ratón sobre la imagen.

![Texto alternativo](ruta/a/la/imagen.jpg "Título alternativo 2")

Ya que al añadir imágenes también estás tratando con URLs, puedes utilizar el método que viste anteriormente para **incluir links mediante referencias**, solo que en este caso **los enlaces de referencia serán aquellos donde se encuentre tu imagen**.

Ejemplo:

![nombre de la imágen][img1]
![nombre de la imágen2][img2]

[img1]: /ruta/a/la/imagen.jpg "Título alternativo"
[img2]: /ruta/a/la/imagen2.jpg "Título alternativo"

## Elementos varios

### Links automáticos

Estos son necesarios cuando lo que quieres es **mostrar una URL completa**, y no un enlace enmascarado bajo una palabra o frase como ocurre con los links en línea.

Para generar links automáticos tan solo tendrás que rodearlos con los símbolos `< >`

<http://www.google.com>

### Omitir Markdown

Si has llegado hasta aquí es probable que te estés preguntando **cómo he conseguido escribir ciertos símbolos** como * asteriscos o _ guiones bajos, sin que Markdown los interprete para convertirlos en negritas, cursivas…

Esto es muy sencillo, ya que en este lenguaje existe un elemento estrella para especificar que todo lo que escribas a continuación, no se interprete como Markdown.

Se trata de la barra invertida `\`. (Alt + 92)

**Escribiéndola justo delante** de cualquiera de los elementos que verás a continuación, los mismos **no tendrán efecto** a la hora de convertirse en negritas, cursivas, links…

```
\  barra invertida
`  acento invertido
*  asterisco
_  guión bajo
{} llaves
[] corchetes
() paréntesis
#  almohadilla
+  símbolo de suma
-  guión
.  punto
!  exclamación
```

\*Omitir Markdown



