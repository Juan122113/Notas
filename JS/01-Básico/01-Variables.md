# Variables.

[Documentación de Mozilla](https://developer.mozilla.org/es/docs/Learn/JavaScript/First_steps/Variables)

## Comentarios.

De una línea: //

De bloque: /* */

## Declarar variables.

En informática, los *datos* son cualquier cosa que tenga sentido para la computadora. JavaScript proporciona ocho _tipos de datos_ diferentes, los cuales son `undefined`([documentación oficial](https://developer.mozilla.org/es/docs/Web/JavaScript/Reference/Global_Objects/undefined)), `null` ([documentación oficial](https://developer.mozilla.org/es/docs/Web/JavaScript/Reference/Operators/null)), `boolean` ([documentación oficial](https://developer.mozilla.org/es/docs/Web/JavaScript/Reference/Global_Objects/Boolean)), `string` ([documentación oficial](https://developer.mozilla.org/es/docs/Web/JavaScript/Reference/Global_Objects/String)), `symbol` ([documentación oficial](https://developer.mozilla.org/es/docs/Web/JavaScript/Reference/Global_Objects/Symbol)), `bigint` ([documentación oficial](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/BigInt)), `number` ([documentación oficial](https://developer.mozilla.org/es/docs/Web/JavaScript/Reference/Global_Objects/Number)) y `object` ([documentación oficial](https://developer.mozilla.org/es/docs/Web/JavaScript/Reference/Global_Objects/Object)).

Por ejemplo, las computadoras distinguen entre números, como el número `12` y cadenas (`strings`), tales como `"12"`, `"dog"` o `"123 cats"`, que son colecciones de caracteres. Las computadoras pueden realizar operaciones matemáticas en un número, pero no en una cadena.

Las *variables* permiten a los ordenadores almacenar y manipular datos de forma dinámica. Hacen esto usando una "etiqueta" para apuntar los datos en lugar de usar los datos en sí. Cualquiera de los ocho tipos de dato puede almacenarse en una variable.

Las variables son un nombre simple para representar los datos a los que queremos hacer referencia.

Le decimos a JavaScript que cree o _declare_ una variable poniendo la palabra clave var [(Documentación oficial)](https://developer.mozilla.org/es/docs/Web/JavaScript/Reference/Statements/var) delante de ella, así:

~~~
var ourName;
~~~

crea una variable llamada `ourName`. En JavaScript terminamos las sentencias con punto y coma. Los nombres de las variables pueden estar formados por números, letras y `$` o `_`, pero no pueden contener espacios ni empezar con un número.

## Almacenar valores con el operador de asignación.

En JavaScript, puedes almacenar un valor en una variable con el operador de *asignación* (`=`) [(Documentación oficial)](https://developer.mozilla.org/es/docs/Web/JavaScript/Reference/Operators/Assignment).

~~~
myVariable = 5;
~~~

Esto asigna el valor numérico (`Number`) `5` a `myVariable`.

Si hay algunos cálculos a la derecha del operador `=`, se realizan antes de que el valor se asigne a la variable a la izquierda del operador.

~~~
var myVar;
myVar = 5;
~~~

Primero, este código crea una variable llamada `myVar`. Luego, el código asigna `5` a `myVar`. Ahora, si `myVar` aparece de nuevo en el código, el programa lo tratará como si fuera `5`.

## Asignar el valor de una variable a otra variable.

Después de asignar un valor a una variable usando el operador de *asignación*, puedes asignar el valor de esa variable a otra variable usando el mismo operador de _asignación_.

~~~
var myVar;
myVar = 5;
var myNum;
myNum = myVar;
~~~

## Inicializar variables con el operador de asignación.

Es común *inicializar* una variable a un valor inicial en la misma línea que es declarada.

~~~
var myVar = 0;
~~~

## Declarar variables de cadena.

También se puede declarar una variable de cadena como esta:

~~~
var myName = "your name";
~~~

`"your name"` es llamada una *cadena literal*. Una cadena literal o cadena es una serie de ceros o más caracteres encerrados en comillas simples o dobles.

## Variables no inicializadas.

Cuando las variables de JavaScript son declaradas, tienen un valor inicial de `undefined` (indefinido). Si haces una operación matemática en una variable `undefined`, tu resultado será `NaN` [(Documentación oficial)](https://developer.mozilla.org/es/docs/Web/JavaScript/Reference/Global_Objects/NaN#:~:text=NaN%20es%20una%20propiedad%20del,NaN%20.) lo que significa "_Not a Number_" (no es un número). Si concatenas una cadena con una variable `undefined`, obtendrás una *cadena* de `undefined`.

## Mayúsculas en las variables.

En JavaScript todas las variables y nombres de función son sensibles a mayúsculas y minúsculas.

Es posible tener múltiples variables distintas con el mismo nombre pero diferente capitalización. Igualmente, no es recomendable este uso.

### Buena práctica.

Escribe los nombres de las variables en JavaScript en *camelCase*. En _camelCase_, los nombres de variables de múltiples palabras tienen la primera palabra en minúsculas y la primera letra de cada palabra posterior en mayúsculas.

#### Ejemplos:

var someVariable,
var anotherVariableName;
var thisVariableNameIsSoLong;

## Diferencias entre las palabras claves var y let.

Uno de los mayores problemas con la declaración de variables utilizando la palabra clave var es que se puede fácilmente sobrescribir declaraciones de variables.

var camper = "James";
var camper = "David";
console.log(camper);

En el código anterior, la variable camper se declara originalmente como James, y se anula para ser David. La consola después muestra la cadena de texto David.

Esto puede generar problemas, especialmente cuando el código base se hace más grande. Debido a que este comportamiento no causa un error, la búsqueda y corrección de errores se vuelve más difícil.

Una palabra clave llamada let [(Documentación oficial)](https://developer.mozilla.org/es/docs/Web/JavaScript/Reference/Statements/let#:~:text=expresi%C3%B3n%20legal%20JavaScript.-,Descripci%C3%B3n,importar%20el%20%C3%A1mbito%20del%20bloque.) fue introducida en ES6, una actualización importante para JavaScript, para resolver este problema potencial con la palabra clave var.

Si reemplazas var por let en el código anterior resultará en un error:

let camper = "James";
let camper = "David";

Así que a diferencia de var, al usar let, una variable con el mismo nombre solo puede declararse una vez.

## Variable de solo lectura: la palabra clave const [(Documentación oficial)](https://developer.mozilla.org/es/docs/Web/JavaScript/Reference/Statements/const).

En ES6, también se pueden declarar variables usando la palabra clave const.

const tiene todas las características increíbles que tiene let, con el bono añadido de que las variables declaradas usando const son de solo lectura. Son un valor constante, lo que significa que una vez que una variable es asignada con const, no se puede reasignar:

const FAV_PET = "Cats";
FAV_PET = "Dogs";

La consola mostrará un error debido a la reasignación del valor de FAV_PET.

Siempre se debe nombrar variables que no quieras reasignar usando la palabra clave const. Esto ayuda cuando se intenta reasignar accidentalmente una variable que está destinada a permanecer constante.

__Nota:__ Es común que los desarrolladores usen identificadores de variables en mayúsculas para valores inmutables y minúsculas o camelCase para valores mutables (objetos y arreglos).




