# Herencia, cascada y especificidad.

[Documentación oficial](https://developer.mozilla.org/es/docs/Learn/CSS/Building_blocks/Cascade_and_inheritance)
Ejemplos: [HTML](https://github.com/Juan122113/CursoCSS/blob/main/03-herencia%2C%20cascadayespecificidad/herencia-cascada-especificidad.html) - [CSS](https://github.com/Juan122113/CursoCSS/blob/main/03-herencia%2C%20cascadayespecificidad/estilos-herencia-cascada-especificidad.css)

## Cascada.

CSS se llama así por cascading style sheets, es decir, hojas de estilo en cascada ¿Por qué se llaman en cascada? Es por una característica que tiene CSS que es la cascada: es una manera de determinar qué selectores van a aplicar los estilos en caso de que haya más de un selector que cambie a un mismo elemento y le de un distinto estilo. La regla de la cascada es: se aplicarán los estilos de los últimos estilos declarados.

## Especificidad.

La cascada es el segundo método que se usa para determinar qué estilos se aplicarán en caso de haber más de un selector que modifique al mismo elemento. Porque el primer método o el método principal es la **especificidad**.
La __especificidad__ es el método primordial que define qué estilos se aplicarán. Tiene mayor importancia que la cascada. La especificidad es el valor que se le da a los selectores en CSS, cada selector tiene un valor diferente al otro. El selector con mayor especificidad es el selector del cual se mostrarán los estilos. En resumen, entre más grande sea la especificidad de un selector, este selector será el que se aplicará.

### Valor de cada selector.

+ **Valor de 1**: Son los selectores de tipo y pseudoelementos.
+ **Valor de 10**: Son los selectores de clase, atributo y pseudoclases.
+ **Valor de 100**: Son los selectores de ID.

Los valores de cada selector también se pueden sumar si se colocan juntos, por ejemplo:

**h1.title**{

color: crimson  !important;
font-family: cursive;
background-color: black;

}

/* 1+10 = 11 */

### Valor !important.

Este valor rompe la regla de la especificidad. Pero es una mala práctica y no se recomienda hacerlo porque puede tener problemas a largo plazo en proyectos grandes. Ejemplo:

h1.title{

color: crimson  !important;

}

### Otras malas prácticas.

Al igual que !important hay otra mala práctica que es crear estilos en línea:

\<h1  class="title"  id="title"  style="color: brown">Hola, soy un título\</h1>

Esta práctica también ignora la especificidad y pasa a ser el predominante a no ser que se coloque el valor !important.

## Herencia.

Es la característica de heredar estilos a los hijos de un contenedor. En pocas palabras, la herencia es la capacidad de los padres de heredar estilos a sus hijos. La herencia hereda solamente ciertos estilos, hay que estar pendiente porque esto puede llegar a ahorrarte código o te puede meter en problemas. Si uno quiere heredar un estilo que no se hereda por defecto entonces se debe colocar la leyenda **inherit** después de la propiedad elegida, por ejemplo:

body{

border: 3px  solid  orange;
font-family: arial;
color: steelblue;

}

  

.title{

border: inherit;

}
