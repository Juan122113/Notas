# Tablas

Las tablas en HTML sirven para mostrar contenido tabulado. [Documentación oficial.](https://developer.mozilla.org/es/docs/Web/HTML/Element/table) - [Ejemplos de tablas.](https://github.com/Juan122113/curso-html-2022/blob/main/tablas.html)

La estructura básica de una tabla se compone de:

**\<table>>\</table>** -> Etiqueta que encierra una tabla.

**\<tr>\</tr>** -> table row: etiqueta que construye una fila. [Documentación oficial.](https://developer.mozilla.org/es/docs/Web/HTML/Element/tr)

**\<td>\</td>** -> table data: etiqueta que construye una celda. [Documentación oficial.](https://developer.mozilla.org/es/docs/Web/HTML/Element/td)

Truco: el número de celdas dentro de un td establecerá el número de columnas de la tabla.

Los títulos de las tablas se establecen con la etiqueta **\<caption>\</caption>**, es una etiqueta opcional, y según la especificación esa etiqueta se coloca justo despues de la etiqueta table. [Documentación oficial.](https://developer.mozilla.org/es/docs/Web/HTML/Element/caption)

Las **cabeceras** de las tablas se establecen con la etiqueta __\<thead>\</thead>__. [Documentación oficial.](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/thead)
Dentro tendremos una etiqueta tr normal, pero en el caso de las celdas, las estableceremos con la etiqueta **\<th>\</th>** en lugar de td. [Documentación oficial.](https://developer.mozilla.org/es/docs/Web/HTML/Element/th)

El **contenido** de la tabla debe ir dentro de una etiqueta __\<TBody>\</TBody>__ para representar el cuerpo de la tabla. [Documentación oficial.](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/tbody)


Para hacer que las celdas **ocupen más de una fila o más de una columna** tenemos 2 atributos:

+ **rowspan**: sirve para que una celda ocupe más de una fila, el valor por defecto es 1.


 **colspan**: sirve para que una celda ocupe más de una columna, el valor por defecto es 1.

Cuando necesitamos **seleccionar una columna**, tenemos la etiqueta __\<colgroup>\</colgroup>__(definición: grupo de columnas, permite crear grupos de columnas), que nos permite seleccionar una columna en concreto. Dentro pondremos tantas etiquetas col como columnas tengamos, cada etiqueta col equivaldrá a una columna siguiendo el mismo orden que tienen en la tabla.

Si necesitamos que una etiqueta **col agrupe más de una columna**, tenemos el atributo **span**, que finciona exáctamente igual que rowspan y colspan.

[Ejemplos de tablas.](https://github.com/Juan122113/curso-html-2022/blob/main/tablas.html)
