# Animaciones (Animation).

[Documentación oficial.](https://developer.mozilla.org/es/docs/Web/CSS/animation)
[Ejemplos.](https://github.com/Juan122113/CursoCSS/tree/main/21-Animaciones)

Es la segunda manera de animar en CSS. Se distingue de transition porque no requiere un disparador o un trigger para generar la animación. De igual manera permite cambiar o permite animar el cambio de un estado a otro a demás de que se pueden animar distintos estilos a la vez y puedes controlar todo el flujo de la animación.

Animation es un shorthand de todos los animation que se verán a continuación. Así como con transition, no importa el orden de estos, solamente los valores de tiempo llevan un orden: primero va animation-duration y segundo animation-delay. Ejemplo:

animation: cambiar-color 2s  1s  linear  infinite  alternate  both  running;

## @keyframes

[Documentación oficial.](https://developer.mozilla.org/es/docs/Web/CSS/@keyframes)

Esta tecnología es experimental.

Esta regla permite a los autores controlar los pasos intermedios en una secuencia de animación CSS mediante el establecimiento de keyframes (o puntos de trayectoria) a lo largo de la secuencia de animación que debe ser alcanzado por determinados puntos durante la animación.

Ayudan a controlar el flujo de toda la animación en la propiedad animation. Básicamente un keyframe permite controlar y declarar los pasos de una animación y cada keyframe tendrá un nombre en específico, el que uno quiera. Los keyframe tienen dos palabras clave la palabra from y la palabra to. Lo que indicamos en from es donde empieza la animación, es decir, con qué estilos va a empezar.

Se escribe primero poniendo un arroba "@" y la palabra keyframes seguido de un espacio más el nombre del keyframe, puede ser cualquier nombre.

@keyframes  cambiar-color{

from{

  

}

to{

}

}

Los keyframes tienen dos palabras clave from y to. Es como un mediaquery pero en vez de tener selectores tenemos la palabra from y la palabra to.

Lo que decimos en from es donde empieza la animación, es decir, con qué estilos va a empezar. Y con to se le indica donde termina la animación. Por ejemplo:

@keyframes  cambiar-color{

from{

width: 250px;

background-color: #000;

}

to{

width: 300px;

background-color: purple;

}

Al hacer esto estoy creando una animación o un keyframe que puedo reutilizar. Esto se hace escribiendo dentro del selector del elemento que queremos modificar la propiedad animation-name.

From y to pueden ser representados con porcentajes. From sería un porcentaje del 0% y to un porcentaje del 100%. Ejemplo:

~~~
@keyframes  cambiar-color{

0%{

width: 250px;

background-color: #000;

}

100%{

width: 300px;

background-color: purple;

}

}
~~~

Esto es lo mismo que el ejemplo anterior.

En las animaciones, dentro del keyframe, podemos declarar más de una propiedad para su cambio, pero solo se pueden animar [las propiedades animables](https://www.google.com/url?sa=t&rct=j&q=&esrc=s&source=web&cd=&cad=rja&uact=8&ved=2ahUKEwji8eXLya77AhUYopUCHX4RAtIQFnoECBMQAQ&url=https%3A%2F%2Fdeveloper.mozilla.org%2Fen-US%2Fdocs%2FWeb%2FCSS%2FCSS_animated_properties&usg=AOvVaw08q1qGwtGx6ew8Do3dX5YZ).

También podemos controlar el flujo de la animación, esto es gracias a los porcentajes que funcionan como selectores:

~~~
@keyframes  cambiar-color{

0%{

transform: scaleY(1);

}

20%{

transform: scaleY(1.2);

}

33%{

transform: scaleY(2);

}

57%{

transform: scaleY(1.5);

}

100%{

transform: scaleY(2.3);

}

}
~~~

## Animation-name.

[Documentación oficial.](/https://developer.mozilla.org/es/docs/Web/CSS/animation-name)

Esta es una tecnología experimental.

Animation-name referencia al keyframe que va a tener el selector seleccionado.

Solo con esta propiedad no se verá nada en la página, falta agregar la duración de la animación.

## Animation-duration.

[Documentación oficial.](https://developer.mozilla.org/es/docs/Web/CSS/animation-duration)

Esta es una tecnología experimental.

Define la duración de la animación- Al igual que transition-duration es una propiedad que acepta segundos.

## Animation-timing-function.

[Documentación oficial.](https://developer.mozilla.org/es/docs/Web/CSS/animation-timing-function)

Esta es una tecnología experimental.

Especifica la curva de aceleración de la animación.

Es muy similar a transition-timing-function. Sus valores son:

+ **ease** -> es su valor por defecto, aumenta la velocidad hacia la mitad de la animación disminuyendo la velocidad al final
+ __ease-in__ -> comienza lentamente pero poco a poco va aumentando la velocidad de la animación.
+ **ease-in-out** -> comienza lentamente, acelera y al final disminuye.
+ __ease-out__ -> comienza la animación rápidamente pero disminuye la velocidad con el tiempo.
+ **linear** -> hace que la animación tenga una velocidad uniforme.

## Animation-iteration-count.

[Documentación oficial.](https://developer.mozilla.org/es/docs/Web/CSS/animation-iteration-count)

Esta es una tecnología experimental.

Define cuantas veces se va a repetir la animación. Su valor por defecto es 1. También acepta el valor _infinite_ que hace que no pare la animación.

## Animation-direction.

[Documentación oficial.](https://developer.mozilla.org/es/docs/Web/CSS/animation-direction)

Esta es una tecnología experimental.

Indica o define desde qué punto parte la animación, hablando del keyframe. Sus valores son:

+ **normal** -> es su valor por defecto, es decir partimos del 0% al 100%.
+ __reverse__ -> en este caso parte del 100% al 0%.
+ **alternate** -> este valor dice que una vez que lleguemos al 100% vamos a regresar al 0% pero con una animación.
+ __alternate-reverse__ -> indica que vamos a empezar del 100% al 0%, una vez que lleguemos al 0% vamos a regresar al 100% pero no de golpe sino con una animación.

## Animation-fill-mode.

[Documentación oficial.](https://developer.mozilla.org/es/docs/Web/CSS/animation-fill-mode)

Esta es una tecnología experimental.

Define lo que sucede antes y después de que una animación se ejecute, se encarga de decirle al navegador si los estilos de la animación se aplican después de que termine o antes de que empiece. Sus valores:

+ **none** -> es su valor por defecto , que es el estado original.
+ __forward__ -> indica que los estilos de la animación se van a aplicar aunque esta termine, es decir, cuando termina la animación se queda con los estilos con los que terminó, no vuelve a su estado original.
+ **backwards** -> nos dice que la animación tendrá los estilos antes de que empiece la animación, es decir, al escribir backwards el elemento seleccionado tendrá los estilos del keyframe cuando empieza antes de que empiece la animación. Para poder apreciar esto es conveniente poner un delay.
+ __both__ -> indica que tendrá forward y backwards, es la combinación. Antes de que empiece la animación va a tomar los primeros estilos del keyframe y una vez que termine se va a quedar con los estilos con los que finaliza.

## Animation-delay.

[Documentación oficial.](https://developer.mozilla.org/es/docs/Web/CSS/animation-delay)

Esta es una tecnología experimental.

Al igual que animation-duration requiere un valor en segundos, esto es para especificar cuánto tiempo va a demorar la animación en ejecutarse. Su valor por defecto es 0.

## Animation-play-state.

[Documentación oficial.](https://developer.mozilla.org/es/docs/Web/CSS/animation-play-state)

Esta es una tecnología experimental.

Determina si una animación está en ejecución o en pausa.

+ **running** -> es su valor por defecto que indica que la animación está corriendo.
+ __pause__ -> pausa la animación.


