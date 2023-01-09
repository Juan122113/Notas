# Transformaciones y Transiciones en CSS (Transform y Transition).

[Ejemplos.](https://github.com/Juan122113/CursoCSS/tree/main/18-transformaciones-transiciones)

## Transform.

[Documentación oficial.](https://developer.mozilla.org/es/docs/Web/CSS/transform)

Esta propiedad nos permite agregar transformaciones en CSS que permiten escalar, rotar, sesgar y trasladar a un elemento con distintos métodos.

### translate()

[Documentación oficial.](https://developer.mozilla.org/en-US/docs/Web/CSS/transform-function/translate)

Este método permite trasladar a un elemento por medio de coordenadas x e y. Por ejemplo, con un valor positivo de 100px traslada a ese elemento 100px hacia la derecha, con un valor negativo lo traslada hacia la izquierda. Esto es lo mismo que utilizar:

position: relative;
left: 100px;

Entonces, ¿por qué usamos transform? Las transformaciones, en este caso, **translate**, se utilizan para evitar usar position relative y las propiedades offset (top, left, right y bottom). __Translate__ reemplaza a las propiedades offset cuando usamos animaciones debido a que usar las propiedades offset en animaciones, consume más recursos que usar **translate**. Entonces la propiedad transform se va a usar mayormente cuando usamos animaciones y transiciones, es el único escenario en el que es mejor usar transform que la propiedad position y sus propiedades offset. 

Si se escribe solo un valor, ese valor es para x, si se escriben dos valores, el primero es para x y el segundo para y:

transform: translate(100px, 100px);

También se pueden usar porcentajes. Por ejemplo, si se escribe un valor del 100%, ese 100% es referente al 100% del ancho, por ejemplo width: 200px, entonces se mueve 200px hacia la derecha. También, en este caso, se pueden usar dos valores, para x y para y. En el caso de y en porcentaje toma el valor del alto. 

#### translateX()

[Documentación oficial.](https://developer.mozilla.org/en-US/docs/Web/CSS/transform-function/translateX)

Translate es el shorthand de __translateX__, que permite mover un elemento en x. Si se utiliza un valor positivo lo mueve hacia la derecha y si es negativo hacia la izquierda.

#### translateY()

[Documentación oficial.](https://developer.mozilla.org/es/docs/Web/CSS/transform-function/translateY)

Permite mover a un elemento en el eje y. Si se escribe un valor positivo mueve al elemento hacia abajo y si es un valor negativo lo mueve hacia arriba.

Se puede usar **translateX** y __translateY__ al mismo tiempo.

### rotate()

[Documentación oficial.](https://developer.mozilla.org/es/docs/Web/CSS/transform-function/rotate)

Define una transformación que gira un elemento alrededor de un punto fijo en un plano 2D sin deformarlo. Aquí se usan valores angulares. Tenemos:
+ Grados que van de 0 a 360 y se indican con "deg".
+ Radiales que van de 0 a 400 y se indican con "grad".
+ Radianes que van de 0 a 6.28319 y se indican con "rap".
+ Vueltas que van de 0 a 1 y se indican con "turn".

### scale()

[Documentación oficial.](https://developer.mozilla.org/es/docs/Web/CSS/transform-function/scale)

Usar propiedades como width y height en animaciones y transiciones es muy costoso, entonces para eso está otro método de transform, **scale** permite escalar, es decir, aumentar o decrementar el valor de un elemento a través de este método aceptando valores positivos, negativos y decimales. No se puede escribir, por ejemplo, que lo escale 30px, debemos usar unidades enteras, por ejemplo, el valor por defecto es 1, que indica que no se va a incrementar.

__Scale__ es un shorthand de **scaleX** y __scaleY__. Si solo se escribe un valor en **scale** será tanto para el eje x como el eje y, si se escriben dos valores será el primero para el eje x y el segundo para el y.

### skew()

[Documentación oficial.](https://developer.mozilla.org/en-US/docs/Web/CSS/transform-function/skew)

Sirve para sesgar a un elemento. Solamente acepta valores angulares como con rotate. Aunque la MDN nos comenta que __skew__ ya no debería usarse sino los métodos individuales: skewX y skewY.

### transform-origin.

[Documentación oficial.](https://developer.mozilla.org/es/docs/Web/CSS/transform-origin#browser_compatibility)

Esta es una tecnología experimental. Antes de usarla en producción hay que comprobar la tabla de compatibilidad de navegadores.

La propiedad CSS __transform-origin__ permite modificar el origen de las transformaciones de un elemento. Por ejemplo:

transform-origin: left  top;

En este caso está indicando que la transformación empiece desde arriba a la izquierda.

### Combinación de métodos.

Si queremos combinar los métodos vistos, se deben escribir en la misma línea de transform, si no se sobreescriben por la cascada. Por ejemplo:

transform: skewX(0deg) skewY(30deg) rotate(80deg);

### Orden de los métodos.

Hay que tener en cuenta de que el orden de los métodos altera el valor final. Por ejemplo:

transform: rotate(80deg) translate(100%, 100%) scale(1.3);

En este caso el elemento no finalizará su animación en el mismo lugar que en el ejemplo visto anteriormente, esto es porque se lo rota en primera instancia y genera un cambio de direcciones a los ejes. Los métodos se suceden en el mismo orden en el que están escritos, en este caso: primero se rota, después se traslada y por último se escala.

## Transition.

[Documentación oficial.](https://developer.mozilla.org/es/docs/Web/CSS/transition)

Esta es una tecnología experimental. Antes de usarla en producción hay que comprobar la tabla de compatibilidad de navegadores.

Transition es un paso, o cambio de un estado a otro. En CSS, las transiciones son la primera forma de animar a un elemento y nos permiten animar cambios de un estado a otro, haciendo que esto pase de manera no instantánea, creando una animación.

Normalmente, la propiedad transform y la opacidad se crearon para las animaciones y transiciones.

Por lo general, las transiciones requieren un disparador, en este caso son las pseudoclases como hover, active, target, focus y checked.

No todos los valores pueden ser animados. Esta es una [lista](https://www.google.com/url?sa=t&rct=j&q=&esrc=s&source=web&cd=&cad=rja&uact=8&ved=2ahUKEwji8eXLya77AhUYopUCHX4RAtIQFnoECBMQAQ&url=https%3A%2F%2Fdeveloper.mozilla.org%2Fen-US%2Fdocs%2FWeb%2FCSS%2FCSS_animated_properties&usg=AOvVaw08q1qGwtGx6ew8Do3dX5YZ) de todas las propiedades animables en CSS.

### Shorthand.

Transition es un shorthand. En este caso no importa el orden de las propiedades a diferencia del shorthand de margin o padding, salvo en el caso de la duración de la animación con la duración del tiempo de espera para que una animación se ejecute (transition-delay), en este caso siempre va primero el valor de la duración de la animación.

### Transition-property.

[Documentación oficial.](https://developer.mozilla.org/es/docs/Web/CSS/transition-property)

Especifica la propiedad o propiedades que tendrá la transición, Las propiedades que se definan aquí van a sufrir una transición y una vez que las declares, cuando esas propiedades cambien de valor, no lo harán de manera instantánea, sino con una transición o animación, siempre y cuando la propiedad que mencionas sea animable. 

#### Valores.

**All** es su valor por defecto, lo que significa que todas las propiedades van a ser animables. La contra de usar este valor es que consume muchos recursos del navegador. Lo recomendable es usar solamente las propiedades que se quieran animar, como transform, background-color, opacity, esto se hace poniendo una como entre ellas:

transition-property: background-color, transform, opacity;

### Transition-duration.

[Documentación oficial.](https://developer.mozilla.org/es/docs/Web/CSS/transition-duration)

Define la duración de la transición. Por defecto se usan valores de tiempo, como segundos (s) o milisegundos (ms). Su valor por defecto son 0 s.

### Transition-timing-function.

[Documentación oficial.](https://developer.mozilla.org/en-US/docs/Web/CSS/transition-timing-function)

Define la curva de aceleración de la transición entre el estado inicial y final, es decir, cómo se comporta la transición. 

#### Valores.

+ __ease__ -> es su valor por defecto. Aumenta la velocidad hacia la mitad de la transición y disminuye al final.
+ **ease-in** -> comienza lentamente, pero después aumenta la velocidad.
+ __ease-in-out__ -> la animación comienza lentamente, acelera y al final disminuye.
+ **ease-out** -> comienza la animación rápidamente, pero cuando pasa el tiempo disminuye la velocidad.
+ __linear__ -> es una velocidad uniforme

### Transition-delay.

[Documentación oficial.](https://developer.mozilla.org/es/docs/Web/CSS/transition-delay)

Define el tiempo de espera para que una transición se ejecute. Al igual que transition-duration requiere unidades de tiempo, por defecto es 0 s

### Problemas de fluidez con animaciones.

En este ejemplo no se despliega bien la animación:

transform: translate(100%, 100%) scale(1.3) rotate(80deg);

Esto es porque se debe de seguir al elemento con el puntero del ratón para que la transición ocurra. Entonces, para que se vea bien, se crea un contenedor para el elemento:

~~~
<div  class="container">

<div  class="element"></div>

</div>
~~~

Y se indica que cuando se pase el mouse sobre el container, su hijo, element se va a modificar:

.container:hover  .element{

transform: translate(100%, 100%) scale(1.3) rotate(80deg);

}

Y ahora cuando se pase el mouse sobre el container la transición fluye sin problemas.


