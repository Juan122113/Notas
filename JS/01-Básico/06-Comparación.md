# Comparación.

[Documentación oficial.](https://developer.mozilla.org/es/docs/Web/JavaScript/Reference/Operators/Equality)
[Comparadores de igualdad e identidad](https://developer.mozilla.org/es/docs/Web/JavaScript/Equality_comparisons_and_sameness)

## Comparación con el operador de igualdad.

[Documentación oficial](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Equality)

Hay muchos operadores de *comparación* en JavaScript. Todos estos operadores devuelven un valor booleano.

El operador más básico es el de igualdad `==`. El operador de igualdad compara dos valores y devuelve `true` si son equivalentes o `false` si no los son. Ten en cuenta que una igualdad es diferente a una asignación (`=`), la cual asigna el valor a la derecha del operador a la variable de la izquierda.

```js
function equalityTest(myVal) {
  if (myVal == 10) {
    return "Equal";
  }
    return "Not Equal";
  }
```

Si `myVal` es igual a `10`, el operador de igualdad devuelve `true`, así que el código dentro de los corchetes se ejecutará y la función devolverá `Equal`. De lo contrario, la función devolverá `Not Equal`. Para que JavaScript compare dos _tipos de datos_ diferentes (por ejemplo, `numbers` y `strings`), tiene que convertir un tipo a otro.  Esto se conoce como coerción [(Documentación oficial)](https://developer.mozilla.org/es/docs/Glossary/Type_coercion) de Tipo. Sin embargo, una vez lo hace, puede comparar términos como se ve a continuación:

```js
1 == 1   // true
1 == 2   // false
1 == '1' // true
"3" == 3 // true
```

## Comparación con el operador de estricta igualdad.

[Documentación oficial](https://developer.mozilla.org/es/docs/Web/JavaScript/Reference/Operators/Strict_equality)

La estricta igualdad (`===`) es la contraparte del operador de igualdad (`==`). Sin embargo, a diferencia del operador de igualdad, el cual intenta convertir ambos valores comparados a un tipo común, el operador de estricta igualdad no realiza una conversión de tipo.

Si los valores que se comparan tienen diferentes tipo, se consideran desiguales, y el operador de estricta igualdad devolverá falso.

**Ejemplos**

~~~
3 === 3 // true
3 === '3' // false
~~~

En el segundo ejemplo, `3` es de tipo `Number` (número) y `'3'` es de tipo `String` (cadena).

**Nota:** En JavaScript, puedes determinar el tipo de una variable o un valor con el operador `typeof`, de la siguiente manera:

~~~
typeof 3
typeof '3'
~~~

`typeof 3` devuelve la cadena `number` y `typeof '3'` devuelve la cadena `string`.

## Comparación con el operador de desigualdad.

[Documentación oficial](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Inequality)

El operador de desigualdad (`!=`) es lo opuesto al operador de igualdad. Esto quiere decir que no es igual, y devuelve `false` cuando la comparación de igualdad devuelva `true` y _vice versa_. Al igual que el operador de igualdad, el operador de desigualdad convertirá los tipos de datos mientras los compara.

**Ejemplos**

~~~
1 != 2     // true
1 != "1"   // false
1 != '1'   // false
1 != true  // false
0 != false // false
~~~

## Comparación con el operador de estricta desigualdad.

[Documentación oficial](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Strict_inequality)

El operador de estricta desigualdad `!==` es el opuesto lógico del operador de estricta igualdad. Esto significa "Estrictamente Desigual", y devuelve `false` cuando la comparación de estricta igualdad devolvería `true` y _vice versa_. El operador de estricta desigualdad no convertirá los tipos de datos.

**Ejemplos**

~~~
3 !== 3   // false
3 !== '3' // true
4 !== 3   // true
~~~

## Comparación con el operador "mayor que".

[Documentación oficial](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Greater_than)

El operador mayor que (`>`) compara los valores de dos números. Si el número a la izquierda es mayor que el número a la derecha, devuelve `true`. De lo contrario, devuelve `false`.

Al igual que el operador de igualdad, el operador mayor que convertirá los tipos de datos de valores mientras los compara.

__Ejemplos__

~~~
5   >  3   // true
7   > '3' // true
2   > 3   // false
'1' > 9 // false
~~~

## Comparación con el operador "mayor o igual que".

[Documentación oficial](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Greater_than_or_equal)

El operador mayor o igual que (`<=`) compara el valor de dos números. Si el número de la izquierda es mayor o igual que el número de la derecha, devuelve `true`. De lo contrario, devuelve `false`.

Este operador también convertirá los tipos de datos mientras los compara.

~~~
6   >= 6   // true
7   >= '3' // true
2   >=  3  // false
'7' >=  9  // false
~~~

## Comparación con el operador "menor que".

[Documentación oficial](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Less_than)

El operador menor que (`<`) compara los valores de dos números. Si el número a la izquierda es menor que el número a la derecha, devuelve `true`. De lo contrario, devuelve `false`. Este operador también convertirá los tipos de dato mientras los compara.

**Ejemplos**

~~~
2   < 5 // true
'3' < 7 // true
5   < 5 // false
3   < 2 // false
'8' < 4 // false
~~~

## Comparación con el operador "menor o igual que".

[Documentación oficial](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Less_than_or_equal)

El operador menor o igual que (`<=`) compara el valor de dos números. Si el número de la izquierda es menor o igual que el número de la derecha, devuelve `true`. Si el número a la izquierda es mayor que el número a la derecha, devuelve `false`. Este operador también convertirá los tipos de dato mientras los compara.

__Ejemplo__

~~~
4   <= 5 //true
'7' <= 7 //true
5   <= 5 //true
3   <= 2 //false
'8' <= 4 //false
~~~

## Comparaciones con el operador lógico "and".

[Documentación oficial](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Logical_AND)

A veces tendrás que probar más de una cosa a la vez. El operador *lógico and* (`&&`) devuelve `true` si y solo si los _operandos_ a la izquierda y a la derecha son verdaderos.

El mismo efecto se podría lograr anidando una sentencia if dentro de otra sentencia if:

~~~
if (num > 5) {
if (num < 10) {
return "Yes";
}
}
return "No";
~~~

solo devolverá `Yes` si `num` es mayor que `5` y menor que `10`. La misma lógica se puede escribir como:

~~~
if (num > 5 && num < 10) {
 reurn "Yes";
 }
 return "No";
~~~

## Comparaciones con el operador lógico "or".

[Documentación oficial](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Logical_OR)

El operador *lógico or* (`||`) devuelve `true` si cualquiera de los _operandos_ es `true`. De lo contrario, devuelve `false`.

El operador *lógico or* se compone dos símbolos de barra vertical: (`||`). Este se puede encontrar normalmente entre las teclas de tabulación y escape.

El patrón de abajo debería parecer familiar desde los puntos de referencia anteriores:

~~~
if (num > 10) {
return "No";
}
if (num < 5) {
return "No";
}
return "Yes";
~~~

devolverá `Yes` sólo si `num`está entre `5` y `10` (5 y 10 incluidos). La misma lógica se puede escribir como:

~~~
if (num > 10 || num < 5) {
return "No";
}
return "Yes";
~~~
