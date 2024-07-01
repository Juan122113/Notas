# Operadores.


[Expresiones y operadores](https://developer.mozilla.org/es/docs/Web/JavaScript/Guide/Expressions_and_Operators)
[Matemáticas básicas en JavaScript — números y operadores](https://developer.mozilla.org/es/docs/Learn/JavaScript/First_steps/Math)


## Suma dos números.


Number (número) [(Documentación oficial)](https://developer.mozilla.org/es/docs/Web/JavaScript/Reference/Global_Objects/Number) es un tipo de datos en JavaScript que representa datos numéricos.

JavaScript utiliza el símbolo + como operador de adición [(Documentación oficial)](https://developer.mozilla.org/es/docs/Web/JavaScript/Reference/Operators/Addition) cuando se coloca entre dos números.

**Ejemplo:**

```js
const myVar = 5 + 10;
```

myVar ahora tiene valor de 15.


## Resta un número de otro.


También podemos restar un número de otro.

JavaScript utiliza el símbolo - para restar [(Documentación oficial)](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Subtraction).

__Ejemplo:__

```js
const myVar = 12 - 6;
```

myVar tendrá el valor de 6.


## Multiplica dos números.


También podemos multiplicar un número por otro [(Documentación oficial)](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Multiplication).

JavaScript utiliza el símbolo * para multiplicar dos números.

**Ejemplo:**

```js
const myVar = 13 * 13;
```

myVar ahora tendrá valor de 169.


## División de un número entero con otro.


JavaScript utiliza el símbolo / para la división [(Documentación oficial)](https://developer.mozilla.org/es/docs/Web/JavaScript/Reference/Operators/Division).

__Ejemplo:__

```js
const myVar = 16 / 2;
```

myVar ahora tiene valor de 8.


## Incrementar un número.


Se puede *incrementar* o sumar uno a una variable con el operador ++.

```js
i++;
```

es equivalente a

```js
i = i + 1;
```

__Nota:__ Toda la línea se convierte en i++; , eliminando la necesidad del signo de igualdad.


## Decrementa un número.


Se puede *decrementar* o disminuir una variable por uno utilizando el operador --.

```js
i--;
```

es el equivalente de

```js
i = i - 1;
```

__Nota:__ La línea se convierte en i--; , eliminando la necesidad del signo igual.


## Crear números decimales.


También podemos almacenar números decimales en variables. Los números decimales a veces se denominan números de *coma flotante* o _flotantes_.


## Multiplicar dos números decimales.


En JavaScript, también se pueden realizar cálculos con números decimales, al igual que con números enteros.

```js
const product =  2.0  *  2.5;
```


## Dividir un decimal entre otro.


```js
const quotient =  4.4  /  2.0;
```


## Encontrar un resto.


El operador de resto % [(Documentación oficial)](https://developer.mozilla.org/es/docs/Web/JavaScript/Reference/Operators/Remainder) entrega el resto de la división entre dos números.

**Ejemplo:**

```js
5 % 2 = 1 porque
Math.floor(5 / 2) = 2 (Cociente)
2 * 2 = 4
5 - 4 = 1 (Resto)
```

__Uso__
En matemáticas, un número se puede comprobar para saber si es par o impar revisando el resto de la división del número por 2.

```js
17 % 2 = 1 (17 es impar)
48 % 2 = 0 (48 es par)
```

**Nota:** El operador de _resto_ es a veces incorrectamente referido como el operador módulo. Es muy similar al módulo, pero no funciona adecuadamente con números negativos.


## Asignación compuesta con adición aumentada.


En la programación, es común utilizar asignaciones para modificar el contenido de una variable. Recuerda que todo lo que está a la derecha del signo de igualdad se evalúa primero, así que debemos decir:

```js
myVar = myVar + 5;
```

para sumar 5 a myVar. Dado que se trata de un patrón tan común, hay operadores que hacen tanto la operación matemática como la asignación en un solo paso.

Uno de estos operadores es el operador +=.

```js
let myVar = 1;
myVar += 5;
console.log(myVar);
```

Se mostrará un 6 en la consola.


## Asignación compuesta con resta aumentada.


Al igual que el operador +=, -= resta un número de una variable.

```js
myVar = myVar -5;
```

le restará 5 de myVar. Esto se puede reescribir como:

```js
myVar -= 5;
```


## Asignación compuesta con multiplicación aumentada.


El operador *= multiplica una variable por un número.

```js
myVar = myVar * 5;
```

se multiplicará myVar por 5. Esto se puede reescribir como:

```js
myVar *= 5;
```


## Asignación compuesta con división aumentada.


El operador /= divide una variable entre otro número.

```js
myVar = myVar / 5;
```

Esto se puede reescribir como:

```js
myVar /= 5;
```

