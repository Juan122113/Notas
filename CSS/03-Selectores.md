# Selectores.

Los selectores es la primer parte de una regla CSS. Definen qué elementos del HTML serán modificados. Todos los elementos de HTML  que coincidan con el selector que declaremos, se verán afectados por los estilos de dicho selector. [Documentación oficial (de todos los selectores).](https://developer.mozilla.org/es/docs/Web/CSS/CSS_Selectors) - Ejemplos: [HTML](https://github.com/Juan122113/CursoCSS/blob/main/02-selectores/selectores.html) [CSS](https://github.com/Juan122113/CursoCSS/blob/main/02-selectores/estilosselectores.css)

## Selector de tipo.

También conocido como selector de nombre o de etiqueta, es conocido así porque selecciona una etiqueta directamente del HTML mediante el nombre de la etiqueta que queremos modificar. En otras palabras, el selector es el nombre de la etiqueta tal cual sin ninguna modificación.

## Selector de clase.

Es el más usado, e incluso hay metodologías para escribir clases de una mejor manera. Selecciona a elementos por el nombre dentro del atributo class, es decir, todos los elementos que tengan un atributo class pueden ser seleccionados pero en base al nombre que tengan dentro. Un elemento puede tener más de una clase. Antes de seleccionar una clase hay que poner un **punto "."**.

## Selector de ID.

Selecciona elementos por el nombre que está dentro del atributo ID. Para seleccionar a un elemento por su ID, debes poner un __numeral (#)__ antes de ese nombre y posteriormente el nombre que va dentro del ID. Los ID no se deben repetir, son identificadores únicos de cada elemento, solamente se usarán para modificar a un solo elemento. No se aconseja el uso de este selector.

## Selector universal.

Permite seleccionar a todos los elementos en el documento HTML. Se lo debe colocar al principio del documento para evitar problemas. En principio el selector universal tiene una especificidad de 0, es decir, no cuenta tanto, lo cual se convierte en un problema. Se indica con un __asterisco *__, este indica que estamos seleccionando a todos los elementos. El selector universal viene en cada selector por defecto.

Ejemplos: [HTML](https://github.com/Juan122113/CursoCSS/blob/main/02-selectores/selectores.html) [CSS](https://github.com/Juan122113/CursoCSS/blob/main/02-selectores/estilosselectores.css)

## Selectores combinadores.

Combinan más de un selector básico. Permiten ser más específicos sobre qué elementos queremos seleccionar, es decir, vamos a ocupar más de un selector en estos selectores. Ejemplo de selectores combinadores: [HTML](https://github.com/Juan122113/CursoCSS/blob/main/02-selectores/combinadores/combinadores.html) [CSS](https://github.com/Juan122113/CursoCSS/blob/main/02-selectores/combinadores/estiloscombinadores.css)

### Combinador de descendientes.

Este combinador es representado por un espacio en blanco. Combina dos selectores donde el primer selector debe ser el ancestro del segundo selector. En pocas palabras, el segundo elemento debe estar dentro del primer elemento o del primer selector.

### Combinador de hijos directos.

Este combinador es muy similar al anterior pero es representado por un signo de mayor que ">", de igual manera combina dos selectores, donde el primer selector debe ser padre directo o contenedor directo del segundo selector. Es decir, a diferencia del combinador de descendientes que también seleccionaba a estas listas cuando seleccionabamos a todos los elementos con la clase lista que estuvieran dentro de este ul, ahora con el combinador de hijos directos será diferente, solamente seleccionará a los hijos directos. No es recomendable usar estos selectores ya que agrega demaciada especificidad.

### Combinador de hermano adyacente.

Este sí es recomendable de usar por que nos puede ayudar a crear animaciones con CSS. Este combinador es representado por un signo de **suma "+"**, combina dos selectores donde el segundo elemento o el segundo selector debe ser un hermano adyacente del primer elemento. Es decir, debe ser el siguiente hermano del primer selector y solamente selecciona a ese siguiente hermano.

### Combinador de hermanos generales.

Este combinador es representado por un signo de **virguilla "~"**, que  combina dos selectores donde el segundo selector debe ser un hermano siguiente al primer selector. Es muy similar al selector de hermano adyacente pero este seleccionará a los hermanos siguientes del punto de referencia que cumplan con la regla del selector.

## Selector de atributo.

En CSS podemos seleccionar elementos por medio de sus atributos, por ejemplo: clase, id, href, src, entre otros.
Se encierra al atributo dentro de __corchetes []__. 
Ejemplos de selectores combinadores: [HTML](https://github.com/Juan122113/CursoCSS/blob/main/02-selectores/atributo/atributo.html) - [CSS](https://github.com/Juan122113/CursoCSS/blob/main/02-selectores/atributo/estilosatributo.css)

### Selección mediante diferentes signos.

+ __virguilla ~__ -> Se puede hacer una selección de un atributo de manera parcial, por ejemplo, algunas palabras dentro de una frase, anteponiendo la **virguilla ~** al signo de igual. Este valor no debe estar alterado, es decir el valor debe estar separado por espacios. Ejemplo:

[value~="cursocss.com"]{

background-color: aqua;

}

+ __Acento circunflejo ^__ -> Lo que nos permite hacer es seleccionar el elemento que tenga como prefijo el valor elegido. Es decir, este valor, debe de ir al principio. Ejemplo: 

[value^="Aquí"]{

background-color: aquamarine;

}
+ **Signo de pesos \$** -> Este es lo contrario que el anterior, en vez de ser el prefijo ahora es el sufijo. Es decir, todos los elementos que terminen con la coincidencia elegida van a ser seleccionados. No importa que esté alterado. Ejemplo:

[value$="cursocss.com"]{

background-color: blueviolet;

}

+ __Asterisco *__ -> Es muy similar al selector universal y básicamente se comporta igual. No importa dónde se encuentre el elemento elegido, alterado o no, será seleccionado.
