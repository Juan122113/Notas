# Arreglos (Arrays).


[Documentación oficial.](https://developer.mozilla.org/es/docs/Web/JavaScript/Reference/Global_Objects/Array)


## Almacena múltiples valores en una variable utilizando los arreglos de JavaScript.


Con las variables de arreglos (array) de JavaScript, podemos almacenar varios datos en un solo lugar.

Inicias una declaración de arreglo con un corchete de apertura, lo terminas con un corchete de cierra, y pones una coma entre cada entrada, de esta forma:

```js
const sandwich = ["peanut butter", "jelly", "bread"];
```


## Anida un arreglo dentro de otro arreglo.


También puedes anidar arreglos dentro de otros arreglos, como a continuación:

```js
const teams = [["Bulls", 23], ["White sox", 45]];
```

Esto también es conocido como *arreglo multidimensional*.


## Accede a los datos de un arreglo con índices.


Los índices de los arreglos se escriben en la misma notación de corchetes que usan las cadenas de texto, con la excepción que en vez de especificar un carácter, se especifica una entrada en el arreglo. Así como las cadenas de texto, los arreglos usan indexación _empezando desde cero_, en donde el primer elemento de un arreglo tiene como índice 0.

**Ejemplo**

```js
const array = [50, 60, 70];
console.log(array[0];
const data = array[1];
```

console.log(array[0]) imprime 50, y data tiene el valor 60.


## Modifica los datos de un arreglo con índices.


A diferencia de las cadenas, las entradas de los arreglos son _mutables_ y pueden cambiarse libremente, incluso si el arreglo fue declarado con const.

**Ejemplo**

```js
const ourArray = [50, 40, 30];
ourArray[0] = 15;
```

ourArray ahora tiene el valor [15, 40, 30].

__Nota:__ No debe haber espacios entre el nombre del arreglo y los corchetes, como array[0]. Aunque JavaScript pueda procesar esto correctamente, puedes confundir a otros programadores al leer tu código.


## Accede a arreglos multidimensionales con índices.


Se puede pensar que un arreglo *multidimensional* es como un _arreglo de arreglos_. Cuando usas corchetes para acceder a un arreglo, el primer par de corchetes hace referencia a los elementos del arreglo más externo (el primer nivel), y cada para adicional va haciendo referencia a un nivel más interno.

**Ejemplo**

```js
const arr = [
[1, 2, 3],
[4, 5, 6],
[7, 8, 9],
[[10, 11, 12], 13, 14]
];

const subarray = arr[3];
const nestedSubarray = arr[3][0];
const element = arr[3][0][1];
```

En este ejemplo, subarray tiene el valor [[10, 11, 12], 13, 14], nestedSubarray tiene el valor [10, 11, 12], y element tien el valor 11.

__Nota:__ No debe haber ningún espacio entre el nombre del arreglo y los corchetes,  ni array [0][0] o array [0] [0] están permitidos. Aunque JavaScript pueda procesar esto correctamente, puedes confundir a otros programadores al leer tu código.


## Manipula arreglos con push().


Una forma fácil de añadir datos al final de un arreglo es a través de la función push().

.push() toma uno o más *parámetros* y los "empuja" al final del arreglo.

Ejemplos:

```js
const arr1 = [1, 2, 3];
arr1.push(4);

const arr2 = ["Stimpson", "J", "cat"];
arr2.push(["happy", "joy"]);
```

arr1 ahora tiene el valor [1, 2, 3, 4] y arr2 tiene el valor ["Stimpson", "J", "cat", ["happy ", "joy"]].


## Manipula arreglos con pop().


`.pop()` se utiliza para sacar un valor del final de un arreglo. Podemos almacenar este valor sacado asignándolo a una variable. En otras palabras pop() elimina el último elemento de un arreglo y devuelve ese elemento.

Cualquier tipo de entrada puede ser sacada de un arreglo: números, cadena, incluso arreglos anidados.

```js
const threeArr = [1, 4, 6];
const oneDown = threeArr.pop();
console.log(oneDown);
console.log(threeArr);
```

El primer console.log mostrará el valor 6 y el segundo mostrará el valor `[1, 4]`.


## Manipula arreglos con shift().


`pop()` siempre elimina el último elemento de un arreglo. Pero si quieres eliminar el primero ahí es donde entra .shift(). Funciona igual que .pop(), excepto que elimina el primer elemento en lugar del último.

Ejemplo:

```js
const ourArray = ["Stimpson", "J", ["cat"]];
const removedFromOurArray = ourArray.shift();
```

removedFromOurArray tendrá una cadena con valor Stimpson y ourArray tendrá ["J", ["cat"]].


## Manipula arreglos con unshift().


También puedes des-desplazar (unshift) elementos al comienzo de un arreglo. Por ejemplo añadir elementos delante del arreglo.

Ejemplo:

```js
const ourArray = ["Stimpson, "J", "cat"];
ourArray.shift();
ourArray.unshift("Happy");
```

Después del shift, ourArray tendrá el valor ["J", "cat"]. Después de unshift, ourArray tendrá el valor ["Happy", "J", "cat"].


## concat.


[Documentación oficial.](https://developer.mozilla.org/es/docs/Web/JavaScript/Reference/Global_Objects/Array/concat)

En JavaScript, "concat" es un método de la clase Array que se utiliza para combinar dos o más arrays en un único array. Por ejemplo, podrías usar concat para combinar dos arrays de números en un solo array:

```js
const numbers1 = [1, 2, 3];
const numbers2 = [4, 5, 6];
const combinedNumbers = numbers1.concat(numbers2);

console.log(combinedNumbers); // Output: [1, 2, 3, 4, 5, 6]
```

También puedes utilizar el método concat para combinar arrays con elementos de diferentes tipos, como cadenas de texto y números.


## Array.prototype.slice()


[Documentación oficial.](https://developer.mozilla.org/es/docs/Web/JavaScript/Reference/Global_Objects/Array/slice)

`El método slice()` devuelve una copia de una parte del array dentro de un nuevo array empezando por inicio hasta *fin* (*fin* no incluido). El array original no se modificará.


### Ejemplo.


```js
var nombre = ['Rita', 'Pedro', 'Miguel', 'Ana', 'Vanesa'];
var masculinos = nombres.slice(1, 3);

// masculinos contiene ['Pedro, 'Miguel']
```


## Array.prototype.toString()


[Documentación oficial](https://developer.mozilla.org/es/docs/Web/JavaScript/Reference/Global_Objects/Array/toString) 

El método `toString()` devuelve una cadena de caracteres representando el array especificado y sus elementos.


### Ejemplo.


```js
const array1 = [1, 2, 'a', '1a'];

console.log(array1.toString());
// Expected output: "1,2,a,1a"
```


## flat()


[Documentación oficial](https://developer.mozilla.org/es/docs/Web/JavaScript/Reference/Global_Objects/Array/flat)

El método `flat()` crea una nueva matriz con todos los elementos del sub-array concatenados recursivamente hasta la profundidad especificada.


### Sintaxis.


```js
var newArray = arr.flat([depth]);
```


#### Parámetros.


- `depth` (Opcional): El nivel de profundidad que especifica qué tan profunda debe aplanarse una estructura de matriz anidada. El valor predeterminado es 1.


### Ejemplos.


```js
var arr1 = [1, 2, [3, 4]];
arr.flat();
// [1, 2, 3, 4]

var arr2 = [1, 2, [3, 4, [5, 6]]];
arr.flat();
// [1, 2, 3, 4, [5, 6]]

var arr3 = [1, 2, [3, 4, [5, 6]]];
arr3.flat(2);
// [1, 2, 3, 4, 5, 6]
```
