# Funciones.


[Documentación oficial.](https://developer.mozilla.org/es/docs/Web/JavaScript/Reference/Functions)


## Escribe JavaScript reutilizable utilizando funciones.


En JavaScript, podemos dividir nuestro código en partes reutilizables llamadas *funciones*.

Este es un ejemplo de una función:

```js
function functionName() {
   console.log("Hello World");
   }
```
   
Puedes llamar o _invocar_ esta función usando su nombre seguido por paréntesis, así: functionName();. Cada vez que se llame la función se imprimirá el mensaje Hello World en la consola de desarrollo. Todo el código entre las llaves se ejecutará cada vez que se llame la función.


## Pasa valores a las funciones utilizando argumentos.


Los _parámetros_ [(Documentación oficial)](https://developer.mozilla.org/es/docs/Web/JavaScript/Reference/Functions/Default_parameters) son variables que actúan como marcadores de posición para los valores que deben ser introducidos en una función cuando se llama. Cuando se define una función, se define típicamente junto con uno o más parámetros. Los valores reales que son introducidos (o "pasados") a una función cuando se llama son conocidos con *argumentos* [(Documentación oficial)](https://developer.mozilla.org/es/docs/Web/JavaScript/Reference/Functions/arguments).

Esta es una función con dos parámetros, param1 y param2:

```js
function testFun(param1, param2) {
console.log(param1, param2);
}
```

Entonces podemos llamar a testFun así: testFun("Hello", "World");. Hemos pasado dos argumentos de cadena, Hello y World. Dentro de la función, param1 será igual a la cadena Hello y param2 será igual a la cadena World. Ten en cuenta que podrías llamar a testFun otra vez con diferente argumentos y los parámetros tomarían el valor de los nuevos argumentos.


## Devuelve un valor de una función utilizando "Return".


[Documentación oficial.](https://developer.mozilla.org/es/docs/Web/JavaScript/Reference/Statements/return)

Podemos pasar valores a una función con *argumentos*. Puedes utilizar una declaración de devolución (return) para enviar un valor fuera de una función.

__Ejemplo__

```js
function plusThree(num) {
  return num +3;
}

const answer = plusThree(5);
```

answer tiene el valor 8.

plusThree toma un *argumento* para num y devuelve un valor igual a num + 3.


## Ámbito global y funciones.


En JavaScript, el *ámbito* se refiere a la visibilidad de las variables. Las variables definidas fuera de un bloque de función tienen un ámbito _Global_. Esto significa que pueden ser observadas desde cualquier lugar en tu código JavaScript.

Las variables que se declaran sin las palabras clave let o const se crean automáticamente en el ámbito global. Esto puede crear consecuencias no intencionadas en cualquier lugar de tu código o al volver a ejecutar una función. Siempre debes declarar tus variables con let o const.


## Ámbito local y funciones.


Las variables que se declaran dentro de una función, así como los parámetros de la función tienen un ámbito *local*. Esto significa que solo son visibles dentro de esa función.

Esta es una función myTest con una variable llamada loc.

```js
function myTest() {
  const loc = "foo";
  console.log(loc);
}

myTest();
console.log(loc);
```

La llamada a la función myTest() mostrará la cadena foo en la consola. La línea `console.log(loc)` (fuera de la función myTest) lanzará un error, ya que loc no está definido fuera de la función.


## Ámbito global vs local en funciones.


Es posible tener variables _locales_ y *globales* con el mismo nombre. Cuando haces esto, la variable local tiene precedencia sobre la variable global.

En este ejemplo:

```js
const someVar= "Hat";

function myFun() {
  const someVar = "Head";
  return someVar;
}
```

La función myFun devolverá la cadena Head porque está presente la versión local de la variable.


## Comprendiendo el valor indefinido devuelto por una función.


[Documentación oficial](https://developer.mozilla.org/es/docs/Web/JavaScript/Reference/Global_Objects/undefined)

Una función puede incluir la declaración de devolución (return) pero no tiene por qué hacerlo. En el caso de que la función no tenga una declaración de devolución, cuando la llames, la función procesa el código interno, pero el valor devuelto es undefined (indefinido).

**Ejemplo**

```js
let sum = 0;

function addSum(num) {
  sum = sum + num;
}

addSum(3);
```

addSum es una función sin una declaración de devolución (return). La función cambiará la variable global sum pero el valor devuelto de la función es undefined.


## Asignación con un valor devuelto.


Si recuerda, todo lo que está a la derecha del signo de igualdad se resuelve antes de asignar el valor. Esto significa que podemos tomar el valor devuelto de una función y asignarlo a una variable.

Supongamos que hemos predefinido una función sum que suma dos números juntos, entonces:

```js
ourSum = sum(5, 12);
```

llamará a la función sum, que devuelve un valor de 17 y lo asigna a la variable ourSum.


## Permanece en línea.


En informática una _cola_ (queue) es una estructura de datos *abstracta* donde los elementos se mantienen en orden. Los nuevos elementos se pueden añadir en la parte posterior de la cola y los elementos antiguos se retiran de la parte delantera de la cola.

**Ejemplo**

Aquí tenemos una función `nextInLine` que toma un arreglo (`arr`) y un número (`item`) como argumentos.

Se agrega el número al final del arreglo, luego se elimina el primer elemento del arreglo.

La función `nextInLine` entonces devuelve el elemento que fue removido.

```js
function nextInLine(arr, item)  {

	arr.push(item);

	return arr.shift();

}

let testArr =  [1,  2,  3,  4,  5];


console.log("Before: "  +  JSON.stringify(testArr));

console.log(nextInLine(testArr,  6));

console.log("After: "  +  JSON.stringify(testArr));

// salida de consola
Before: [1,2,3,4,5]
1
After: [2,3,4,5,6]
```


## Comprende los valores booleanos.


[Documentación oficial](https://developer.mozilla.org/es/docs/Web/JavaScript/Reference/Global_Objects/Boolean)

Otro tipo de datos es _Booleano_. Los booleanos solo pueden ser uno de dos valores: true (verdadero) o false (falso). Básicamente son pequeños interruptores de encendido, donde true es encendido y false es apagado. Estos dos estados se excluyen mutuamente.

**Nota** Los valores del tipo booleano nunca se escriben con comillas. Las cadenas "true" y "false" no son booleanos y no tienen ningún significado especial en JavaScript.


## Devuelve valores booleanos desde funciones.


Todo los operadores de comparación devuelven un valor booleano `true` o `false`.

A veces la gente usa una sentencia `if/else` para hacer una comparación, como esta:

```js
function isEqual(a, b) {
  if (a === b) {
    return true;
  } else {
    return false;
  }
}
```

Pero hay una mejor manera de hacer esto. Puesto `===` devuelve `true` o `false`, podemos devolver el resultado de la comparación:

```js
function isEqual(a, b) {
  return a === b;
}
```


## Patrón de devolución anticipado para funciones.


Cuando se alcanza una sentencia `return`, la ejecución de función actual se detiene y el control se devuelve a la ubicación de la llamada.

**Ejemplo**

```js
function myFun() {
  console.log("Hello");
  return "World";
  console.log("byebye")
}
myFun();
```

Lo anterior mostrará la cadena `Hello` en la consola y devolverá la cadena `World`. La cadena `byebye` nunca se mostrará en la consola, porque la función termina en la sentencia `return`. 


## This


[Documentación oficial](https://developer.mozilla.org/es/docs/Web/JavaScript/Reference/Operators/this)

`this` es una palabra clave en JavaScript que se refiere al objeto que está siendo tratado por la función o el método en el que se encuentra. En otras palabras, `this` hace referencia al contexto actual en el que se está ejecutando una función o método. El valor `this` puede variar dependiendo del contexto en el que se utiliza.

**Ejemplo:**

```js
const obj = {
  name: 'John',
  greet: function() {
  console.log('Hello, my name is ${this.name}');
  }
};

obj.greet(); // Output: "Hello, my name is John"
```


## El objeto arguments.


[Documentación oficial](https://developer.mozilla.org/es/docs/Web/JavaScript/Reference/Functions/arguments)

`arguments` es un objeto similar a `array` accesible dentro de funciones, que no sean flecha, que contiene los valores de los argumentos pasados a esa función.


### Ejemplo.


```js
function func1(a, b, c) {
  console.log(arguments[0]);
  // Expected output: 1

  console.log(arguments[1]);
  // Expected output: 2

  console.log(arguments[2]);
  // Expected output: 3
}

func1(1, 2, 3);
```










