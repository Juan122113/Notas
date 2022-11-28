# Atributos

Los elementos en HTML tienen **atributos**. Los atributos son valores adicionales que configuran los elementos y/o ajustan su comportamiento.
En terminos generales hay dos tipos de atributos
+ Comunes: Su sintaxis es -> atributo = "valor"
+ Booleano: Su sintaxis es -> atributo

[Documentación oficial](https://developer.mozilla.org/es/docs/Web/HTML/Attributes)


+ \<html **lang="en"**> -> establece en qué idioma se escribirá el documento.
    + \<html lang="en"> -> establece que el documento está en inglés.
    + \<html lang="es"> -> lang="es" establece que el documento está en español. [Documentación oficial.](https://developer.mozilla.org/es/docs/Web/HTML/Global_attributes/lang) - [Ejemplo.](https://github.com/Juan122113/curso-html-2022/blob/main/index.html)
+ \<meta **charset="UTF-8"**> -> Va dentro del \<head>. Se le indica que se va a utilizar el set de caracteres latino. Sirve para solucionar problemas de visualización con los acentos o distintos caracteres. **Meta:** de "metainformación". Sirve para aportar información sobre el documento. [Documentación oficial.](https://developer.mozilla.org/es/docs/Web/HTML/Element/meta)

Algunos atributos globales que están disponibles para la mayoría de etiquetas en HTML:

+ **class** -> Este atributo se usa para dar estilos a través de CSS. [Documentación oficial](https://developer.mozilla.org/es/docs/Web/HTML/Global_attributes/class) - [Ejemplo.](https://github.com/Juan122113/curso-html-2022/blob/main/atributos-comunes.html)
+ **id** -> Es un identificador único que se utiliza para seleccionar el elemento desde JS y para hacer navegación a través de anclas. El atributo global **id** define un identificador único (ID) en cual no debe repetirse en todo el documento. Su propósito es identificar el elemento al vincularlo (usando un identificador de framento), en scripts u hojas de estilo (con CSS). [Documentación oficial](https://developer.mozilla.org/es/docs/Web/HTML/Global_attributes/id) - [Ejemplo.](https://github.com/Juan122113/curso-html-2022/blob/main/atributos-comunes.html)
+ **title** -> Contiene un texto representando información relacionada al elemento al cual pertenece. Tal información puede típicamente, pero no necesariamente, ser presentada al usuario como un tip. Es un atributo que ayuda a la accesibilidad mostrando una descripción del elemento al que pertenece. Aparece el mensaje en un tooltip. Ejemplo: \<p  title="Este es un ejemplo del atributo title">Título con tooltip\</p>. [Documentación oficial](https://developer.mozilla.org/es/docs/Web/HTML/Global_attributes/title) - [Ejemplo.](https://github.com/Juan122113/curso-html-2022/blob/main/atributos-comunes.html)
+ **data-*** -> Es un atributo que nos permite guardar algún valor en la etiqueta HTML. Al nivel de HTML no se le encuentra ninguna utilidad. Pero con Javascript este atributo salva muchas veces de romperse la cabeza para solucionar problemas.
