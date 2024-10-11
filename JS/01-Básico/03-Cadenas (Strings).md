# Cadenas (Strings).


[Documentación oficial.](https://developer.mozilla.org/es/docs/Web/JavaScript/Reference/Global_Objects/String)


## Escapa comillas literales en cadenas.


Cuando estás definiendo una cadena debes comenzar y terminar con una comilla simple o doble. ¿Qué pasa cuando necesitas una comilla literal: " o ' dentro de tu cadena?

En JavaScript, puedes *escapar* una comilla de considerarse un final de cadena colocando una _barra invertida_ (`\`) delante de la comilla.

```js
const sampleStr = "Alan said, \\"Peter is learning JavaScript\\".";
```

Esto indica a JavaScript que la siguiente comilla no es el final de la cadena, sino que debería aparecer dentro de la cadena. Así que si imprimieras esto en la consola, obtendrías:

```js
Alan said, "Peter is learning JavaScript".
```


## Cita cadenas con comillas simples.


Los valores de *cadena* en JavaScript pueden escribirse con comillas simples o dobles, siempre y cuando comiencen y terminen con el mismo tipo de comillas. A diferencia de otro lenguajes de programación, las comillas simples y dobles funcionan igual en JavaScript.

```js
const doubleQuoteStr = "This sis a string";
const singleQuoteStr = 'This is also a string';
```

La razón por la que puedes querer usar un tipo de comilla sobre otro es si quieres usar ambos en una cadena. Esto puede suceder si quieres guardar una conversación en una cadena y tener la conversación entre comillas. Otro uso sería guardar una etiqueta \<a> con varios atributos entre comillas, todo dentro de una cadena.

```js
const conversation = 'Finn exclaims to Jake, "Algebraic!"';
```

Sin embargo, esto se convierte en un problema cuando es necesario utilizar las comillas externas dentro de ella. Pero si tienes esa misma comilla en algún lugar del medio, la cadena se detendrá antes de tiempo y arrojará un error.

```js
const goodStr = 'Jake ask Finn, "Hey, let\\'s go on an adventure?"';
const badStr = 'Finn responds, "Let's go!"';
```

Aquí badStr arrojará un error.

__Nota:__ La barra invertida \ no debe confundirse con la barra diagonal /. No hacen lo mismo.


## Escapa secuencias en cadenas.


Las comillas no son los únicos caracteres que pueden ser *escapados* dentro de una cadena. Hay dos razones para usar caracteres de escape:

1. Para permitirle usar caracteres que de otra manera no se podrían representar dentro de una cadena, como el carácter nueva línea.
2. Para permitirle representar múltiples comillas en una cadena sin que JavaScript malinterprete lo que quieres decir.

__Código__ &ensp; &nbsp;  **Resultado**
      \'  &ensp; &ensp; &ensp; &ensp; &ensp;              comilla simple
      \" &ensp; &ensp; &ensp; &ensp; &ensp;             comilla doble
      \\ &ensp; &ensp; &ensp; &ensp;  &ensp;             barra invertida
      \n &ensp; &ensp; &ensp; &ensp; &ensp;            línea nueva
      \t &ensp; &ensp; &ensp; &ensp; &ensp;            línea nueva
      \t  &ensp; &ensp; &ensp; &ensp; &ensp;                   tabulador
      \r &ensp; &ensp; &ensp; &ensp; &ensp;             retorno del carro
      \b &ensp; &ensp; &ensp; &ensp; &ensp;           límite de palabra
      \f &ensp; &ensp; &ensp; &ensp; &ensp;        fuente de formulario

_Ten en cuenta que la barra invertida en sí debe ser escapada para poder mostrarla como una barra invertida_

**Ejemplo:**

```js
const myStr =  "FirstLine\n\t\\\SecondLine\nThirdLine";
```

Da como resultado:

```js
FirstLine  
	\SecondLine  
ThirdLine
```


## Cocatena cadenas con el operador "más".


En JavaScript cuando el operador + se utiliza con un valor de cadena (String), se le llama operador de *concatenación*. Puedes construir una nueva cadena a partir de otras cadenas _concatenándolas_ juntas.

**Ejemplo**

```js
'My name is Alan,' + 'I concatenate.'
```

__Nota:__ Ten cuidado con los espacios. La concatenación no añade espacios entre las cadenas concatenadas, así que tendrás que añadirlos por tu cuenta.

Ejemplo:

```js
const ourStr = "I come first. " + "I come second.";
```

La cadena I come first. I come second. se mostraría en la consola.


## Concatena cadenas con el operador "más igual".


También podemos utilizar el operador += para *concatenar* una cadena al final de una variable de cadena existente. Esto puede ser muy útil para romper una cadena larga en varias líneas.

__Nota:__ Ten cuidado con los espacios. La concatenación no añade espacios entre las cadenas concatenadas, así que tendrás añadirlos por tu cuenta.

Ejemplo:

let ourStr = "I come first. ";
ourStr += "I come second.";

ourStr ahora tiene un valor de la cadena I come first. I come second. .


## Contruye cadenas con variables.


A veces necesitarás construir una cadena. Al usar el operador de concatenación (+), puedes insertar una o más variables en una cadena que estés construyendo.

Ejemplo:

const ourName = "freeCodeCamp";
const ourStr = "Hello, our name is " + ourName + ", how are you?";

ourStr tendrá como valor la cadena Hello, our name is freeCodeCamp, how are you?.


## Agregar variables a cadenas.


Al igual que podemos crear una cadena sobe múltiples líneas a partir de las cadenas *literales*, también podemos añadir variables a una cadena usando el operador "más igual" (+=).

Ejemplo:

```js
const anAdjective = "awesome!";
let ourStr = freeCodeCamp is ";
ourStr += anAdjective;
```

ouStr tendrá el valor de freeCodeCamp is awesome!.


## Encontrar la longitud de una cadena.


[Documentación oficial.](https://developer.mozilla.org/es/docs/Web/JavaScript/Reference/Global_Objects/String/length)

Puedes encontrar la longitud de un valor de cadena (String) escribiendo .length después de la variable de cadena o literal de cadena.

console.log("Alan Peter".length);

El valor 10 se mostrará en la consola. Toma nota que el carácter espacial entre "Alan" y "Peter" también se cuenta.

Por ejemplo, si creamos una variable const firstName = "Ada", podríamos averiguar la longitud de la cadena Ada usando la propiedad firstName.length.


## Utilizar la notación de corchetes para encontrar el primer carácter en una cadena.


La _notación de corchetes_ es una forma de obtener un carácter en un índice (index) específico dentro de una cadena.

La mayoría de lenguajes de programación modernos, como JavaScript, no empiezan a contar dese 1 como lo hacen los humanos. Empiezan desde 0. Esto se conoce como indexación *basada en cero*.

Por ejemplo, el carácter en el índice 0 de la palabra Charles es C. Así que si declaramos const firstName = "Charles", puedes obtener el valor de la primera letra de la cadena usando firstName[0].

Ejemplo:

```js
const firstName = "Charles";
const firstLetter = firstName[0];
```

firstLetter tendrá una cadena con valor C.


## Comprender la inmutabilidad de las cadenas.


En JavaScript, los valores de cadena (Script) son _inmutables_, lo que significa que no pueden ser alterados una vez creados.

Por ejemplo, el siguiente código producirá un error debido a que la letra B en la cadena Bob no puede ser cambiada por la letra J:

let myStr = "Bob";
myStr[0] = "J";

Nota que esto no significa que myStr no pueda ser reasignado. La única manera de cambia el valor de myStr sería asignándole un nuevo valor, como en el siguiente ejemplo:

let myStr = "Bob";
myStr = "Job";


## Utilizar la notación de corchetes para encontrar el enésimo carácter en una cadena.


También podemos usar *notación de corchetes* para obtener el carácter en otras posiciones dentro de una cadena.

Ejemplo:

```js
const firstName = "Ada";
const secondLetterOfFirstName = firstName[1];
```

`secondLetterOfFirstName` tendrá una cadena con valor `d`.


## Utilizar la notación de corchetes para encontrar el último carácter en una cadena.


Con el fin de obtener la última letra de una cadena, puedes restar uno a la longitud del texto.

Por ejemplo, sí const FirstName = "Ada", puedes obtener el valor de la última letra de la cadena usando firstName[firstName.length - 1].

Ejemplo:

```js
const firstName = "Ada";
const lastLetter = firstName[firstName.length -1]
```

`lastLetter` tendrá una cadena con valor `a`.


## Utilizar la notación de corchetes para encontrar el carácter enésimo final en una cadena.


Puedes usar el mismo principio que acabamos de usar para recuperar el último carácter de una cadena para recuperar el carácter enésimo final.

Por ejemplo, puedes obtener el valor de la antepenúltima letra de la cadena const firstName = "Augusta" usando firstName[firstName.length -3]

Ejemplo:

```js
const firstName = "Augusta";
const thirdToLastLetter = firstName[firstName.length -3];
```

`thirdToLastLetter` tendrá una cadena con valor `s`.



## Palabra en blanco.


Se te proporcionan oraciones con algunas palabras faltantes, como sustantivos, verbos, adjetivos y adverbios. Luego, completa las piezas que faltan con palabras de tu elección de una manera que la oración completa tenga sentido.

Considera esta oración: It was really \__, and we __ ourselves__. Esta oración tiene tres piezas faltantes: un adjetivo, un verbo y un adverbio, y podemos añadir palabras de nuestra elección para completarla. Luego podemos asignar la oración completa a una variable de la siguiente manera;

```js
const sentence = "It was really " + "hot" + ", and we " + "laughed" + " ourselves " + "silly" + ".";
```


## Pasar la cadena a minúsculas.


[Documentación oficial](https://developer.mozilla.org/es/docs/Web/JavaScript/Reference/Global_Objects/String/toLowerCase)

El método `toLowerCase()` devuelve el valor **en minúsculas** de la cadena que realiza la llamada.


### Sintaxis.


```js
cadena.toLowerCase()
```


## Pasar la cadena a mayúsculas.

[Documentación oficial](https://developer.mozilla.org/es/docs/Web/JavaScript/Reference/Global_Objects/String/toUpperCase)

El método `toUpperCase()` devuelve el valor convertido __en mayúsculas__ de la cadena que realiza la llamada.


### Sintaxis.


```js
cadena.toUpperCase()
```


## charCodeAt()


[Documentación oficial](https://developer.mozilla.org/es/docs/Web/JavaScript/Reference/Global_Objects/String/charCodeAt)

El `charCodeAt()` método devuelve un número indicando el valor Unicode del carácter en el índice proporcionado.


### Ejemplo.


El siguiente ejemplo devuelve 65, el valor Unicode para A.

```js
"ABC".charCodeAt(0); // returns 65
```


## charAt()


[Documentación oficial](https://developer.mozilla.org/es/docs/Web/JavaScript/Reference/Global_Objects/String/charAt)

El método `charAt()` de String devuelve en un nuevo String el carácter UTF-16 de una cadena.


### Ejemplo.


```js
var cualquierCadena = "Brave new world";

console.log{
  "El carácter en el índice 0 es '" + cualquierCadena.charAt() + "'",
};
console.log{
  "El carácter en el índice 1 es '" + cualquierCadena.charAt(1) + "'",
};
console.log{
  "El carácter en el índice 2 es '" + cualquierCadena.charAt(2) + "'",
};
console.log{
  "El carácter en el índice 3 es '" + cualquierCadena.charAt(3) + "'",
};
console.log{
  "El carácter en el índice 4 es '" + cualquierCadena.charAt(4) + "'",
};
console.log{
  "El carácter en el índice 999 es '" + cualquierCadena.charAt(999) + "'",
};
```

Estas líneas muestran lo siguiente:

```js
El carácter en el índice 0 es 'B'
El carácter en el índice 1 es 'r'
El carácter en el índice 2 es 'a'
El carácter en el índice 3 es 'v'
El carácter en el índice 4 es 'e'
El carácter en el índice 999 es ''
```


