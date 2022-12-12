# Formularios

## Estructura básica

La estructura básica de un formulario se compone de 4 elementos. [Ejemplos de estructura básica,](https://github.com/Juan122113/curso-html-2022/blob/main/formularios/estructura-basica.html)

**\<form>\</form>** -> es la etiqueta que engloba nuestro formulario. Representa una sección de un documento que contiene controles interactivos que permiten a un usuario enviar información a un servidor web. [Documentación oficial.](https://developer.mozilla.org/es/docs/Web/HTML/Element/form)

**\<label>\</label>** -> Representa una etiqueta para un elemento en una interfaz de usuario. Sirve para escribir el nombre del campo a rellenar. Debe tener el atributo for al cual se le indica un id que lo que hará será emparejar el label con su input correspondiente. [Documentación oficial.](https://developer.mozilla.org/es/docs/Web/HTML/Element/label)

**\<input>** -> Se usa para crear controles interactivos para formularios basados en la web con el fin de recibir datos del usuario. Sirve para crear un campo que permitirá al usuario interactuar. [Documentación oficial.](https://developer.mozilla.org/es/docs/Web/HTML/Element/input)

**\<button>\</button>** -> Botón. Crea un botón que permitirá enviar el formulario. [Documentación oficial.](https://developer.mozilla.org/es/docs/Web/HTML/Element/button) [Ejemplos de estructura básica.](https://github.com/Juan122113/curso-html-2022/blob/main/formularios/estructura-basica.html)

## Tipos de input.

[Ejemplos de tipos de input.](https://github.com/Juan122113/curso-html-2022/blob/main/formularios/tipos-de-input.html)

**input type:**

+ **button** -> Se comporta igual que un botón <button>. Pero no sirve para enviar el formulario (en HTML)

+ **date** -> Se utiliza para introducir una fecha.

+ **datetime** -> Obsoleto

+ **datetime-local** -> fecha y hora, no funciona en firefox.

+ **time** -> Se utiliza para introducir una hora. (TIP: Se recomienda usar date y time para seleccionar fecha y hora ya que datetime-local no funciona para Firefox.
hidden -> Campo oculto, puede contener valor pero no se mostrará.)

+ **email** -> Se utilia para introducir un email.

+ **hidden** -> Campo oculto, puede contener valor pero no se mostrará.

+ **month** -> Se utiliza para introducir un mes.

+ **password** -> Se utiliza para contraseñas.

+ **search** -> Se utiliza para las barras de búsqueda.

+ **submit** -> Se utiliza para enviar el formulario.

+ **tel** -> Se utiliza para introducir número telefónicos.

+ **time** -> Se utiliza para introducir una hora. (TIP: Se recomienda usar date y time para seleccionar fecha y hora ya que datetime-local no funciona para Firefox.
hidden -> Campo oculto, puede contener valor pero no se mostrará.)

+ **url** -> Se utiliza para introducir URLs.

+ **week** -> Se utiliza para introducir el número de semana del año.

+ **color** -> Se utiliza para especificar un color.

+ **number** -> Se utiliza para valores numéricos.

+ **range** -> Se utiliza para establecer un rango. También aceptan el atributo **step** que sirve para determinar de cuanto en cuanto se mueve la barra de range. También tiene el atributo **min** y **max** que sirven para determinar el rango total de la barra.

+ **reset** -> Se utiliza para resetear el formulario. Borra los datos introducidos y los deja como estaban desde un principio.

+ **text** -> Valor por defecto.

[Ejemplos de tipos de input.](https://github.com/Juan122113/curso-html-2022/blob/main/formularios/tipos-de-input.html)

### Inputs de selección.

[Ejemplos de inputs de selección.](https://github.com/Juan122113/curso-html-2022/blob/main/formularios/inputs-de-selecci%C3%B3n.html)

+ **radio** -> Permite seleccionar una única opción de una lista de opciones relacionadas. Para que se seleccione solo una única opción se debe incluir el atributo **name**, que es obligatorio, donde se debe indicar el mismo nombre en cada elemento que se quiere seleccionar para indicar al navegador que los inputs pertenecen a la misma categoría. El atributo **checked** hace que un input quede marcado por defecto. El atributo **value**, también obligatorio, sirve para decirle al formulario cuando lo enviemos, qué valor es el que contiene el elemento. Ejemplo:

\<form>

\<h2>Género\</h2>

\<label>Masculino

\<input  type="radio"  name="gender" value="masculino" checked>

\</label>

\<label>Femenino

\<input  type="radio"  name="gender" value="femenino">

\</label>

\<label>Desconocido

\<input  type="radio"  name="gender" value="desconocido">

\</label>

\</form>

+ **checkbox** -> Permite seleccionar varias opciones de una lista de opciones relacionadas. También usa el atributo **name** y el **value** obligatoriamente, y el atributo **checked**, que se puede usar para marcar varios elementos, pero no funciona, en este caso, en Firefox.

+ **\<select>\</select>** -> Crea una lista de opciones donde podemos seleccionar una o varias opciones. Cada opción irá dentro de una etiqueta \<option> \</option>. Si tenemos muchas opciones podemos ordenarlas por categorías a través de la etiqueta \<optgroup> con el atributo label para nombrar la categoría. También usa el atributo **name** (que va en elemento  **select**) y el **value** (que va en el elemento option). Si quisieramos que se pueda seleccionar más de uno tenemos el atributo **multiple**, presionando la tecla cntrl se pueden seleccionar. [Documentación oficial.](https://developer.mozilla.org/es/docs/Web/HTML/Element/select) 

+ **datalist** -> Son muy similares a los **select** pero estos incluyen un filtro para que se pueda buscar de una forma más sencilla. [Documentación oficial.](https://developer.mozilla.org/es/docs/Web/HTML/Element/datalist)

Es muy importante que a los formularios se le ponga un **name** si no se los pone, es como que ese campo no existiera.

[Ejemplos de inputs de selección.](https://github.com/Juan122113/curso-html-2022/blob/main/formularios/inputs-de-selecci%C3%B3n.html)

### Más elementos.

[Ejemplos de más elementos.](https://github.com/Juan122113/curso-html-2022/blob/main/formularios/mas-elementos.html)

+ **\<fieldset>\</fieldset>** -> Se utiliza para agrupar elementos dentro de un formulario. [Documentación oficial.](https://developer.mozilla.org/es/docs/Web/HTML/Element/fieldset)

+ **\<legend>\</legend>** -> Representa una etiqueta para el contenido del fieldset. [Documentación oficial.](https://developer.mozilla.org/es/docs/Web/HTML/Element/legend)

+ **file** -> Este input se utiliza para cargar archivos y enviarlos desde un formulario.

+ **\<meter>\</meter>** -> Representa un valor dentro de un rango conocido. Dentro de él, __low__ y __high__ se usan para marcar un valor alto o bajo, si la barra está dentro de estos valores, cambia de color. [Documentación oficial.](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/meter)

+ **\<progress>\</progress>** -> Representa el progreso de una tarea.

+ **\<textarea>\</textarea>** -> Se utiliza para introducir texto en un formulario. Dentro de él están __cols__ y __rows__ (colúmnas y filas), para hacerlo más ancho y/o mas alto. [Documentación oficial.](https://developer.mozilla.org/es/docs/Web/HTML/Element/textarea)

[Ejemplos de más elementos.](https://github.com/Juan122113/curso-html-2022/blob/main/formularios/mas-elementos.html)


## Atributos.

[Ejemplos de atributos.](https://github.com/Juan122113/curso-html-2022/blob/main/formularios/atributos-formularios.html)

Hay muchísimos. Estos son los principales:

+ **placeholder** -> Da una pista de lo que el usuario tiene que introducir. Ejemplo:

\<form>
\<input  type="text"  placeholder="Introduce tu nombre">
\</form>

+ **required** -> Hace que un campo sea obliatorio.

+ **readonly** -> Hace que un campo sea de solo lectura.

+ **disabled** -> Desactiva el campo, no se podrá escribir en el autofocus.

+ **min - max** -> Establece el mínimo y máximo de un campo numérico.

+ **minlenght - maxlenght** -> Establece el mínimo y máximo de carácteres de un campo de texto.

+ **selected** -> Equivale a checked en los select, sirve para establecer una opción por defecto.

+ **autofocus** -> Para poner el foco por defecto al cargar el formulario. El foco significa que simule que el usuario a hecho click.

[Ejemplos de atributos.](https://github.com/Juan122113/curso-html-2022/blob/main/formularios/atributos-formularios.html)

## Get vs post

+ **Get** -> Es el método por defecto. Es el método que se ejecuta cuando se entra a una página a través de la URL.
+ **Post** -> Este método es el envio de formularios a través de la parte de atrás de la página por llamarlo de alguna manera. [Ejemplo.](https://github.com/Juan122113/curso-html-2022/blob/main/formularios/get-vs-post.html)
