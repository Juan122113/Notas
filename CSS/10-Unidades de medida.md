# Unidades de medida.

[Documentación oficial.](https://developer.mozilla.org/es/docs/Learn/CSS/Building_blocks/Values_and_units)
[Ejemplos.](https://github.com/Juan122113/CursoCSS/tree/main/09-Unidades%20de%20medida)

Hay dos tipos:

## Unidades absolutas.

Se llaman así porque tienen un valor definido y ese valor no depende de nada más, siempre será el mismo, nunca van a cambiar. Por eso se llaman absolutas.

.title{

font-size: 40px;

}

"40px" es una unidad absoluta y nunca va a cambiar. También se pueden usar en vez de pixeles (px) centímetros (cm), o puntos (pt), o milímetros (mm). Los píxeles son los que más se usan.

## Unidades de longitud relativa.

Se llaman así porque su tamaño depende de algo externo a ellas, esto significa que ese valor puede cambiar dependiendo el contexto.

### Rem.

La unidad __rem__ es relativa al tamaño de la fuente o al font size de la raíz del documento. La raíz del documento se puede visualizar con el selector HTML. Por defecto un **rem** es igual a 16px o al font size que tiene la raíz del documento que en la mayoría de casos el font size del HTML es 16px, pero puede llegar a variar dependiendo del tamaño de fuente o del tamaño de letra que agregues en tu navegador. Por defecto es normal, pero si lo pones más pequeño el font sizes del HTML será más pequeño o si lo pones en un tamaño de letra grande el font sizes será más grande. Esto nos ayuda a que si tenemos, por ejemplo, todos mis títulos con unidad de medida en __rem__ y si en algún punto el tamaño de la letra llega a cambiar también el tamaño de **rem**.
Ejemplo:

.title{

font-size: 3rem;

}

En este ejemplo sería 3 __rem__ igual a 48px, porque la medida estándar del font size de la raíz del documento es 16px, 3 x 16 = 48. 

### Em.

Es muy similar a rem, pero la diferencia es que rem se basa en el font size de la raíz del documento, pero **em** es relativo al tamaño de fuente del padre o de un ancestro superior que tenga declarado un font size, y si la usamos para propiedades como width o height va a tomar el __em__ igualmente del font size del padre, a menos que se esté usando un font size para el mismo elemento que se quiere modificar, en este caso entonces el __em__ de width o height va a ser de el resultado del **em** del font size, por ejemplo:

.container{

padding: 40px;

font-size: 10px;

}

.title{

font-size: 3em;

  

width: 5em;

}
 
En este caso container es padre de title, por ende el font size de title es igual a 30px (3 x 10px) y el width de title es de 150px (5 x 30px).

 Si no tiene padres entonces lo toma de la raíz del documento.

### Viewport.

Las unidades de **viewport** son relativas al __viewport__ del navegador. El **viewport** básicamente es el área visible que podemos observar en el navegador, por más de que haya un scroll el __viewport__ sigue siendo solamente el área visible del navegador. 

#### Viewport width.

Se escribe "v" de __viewport__  y "w" de **width** __vw__. 

width: 50vw;

Esto referencia al 50% del **viewport** y si tiene un valor de 30vw se refiere al 30%. Los valores van de 0 a 100vw.

Si se elige 100vw, en algunas ocasiones no ocupará el 100% del ancho, porque, si se le pone, por ejemplo, a body un alto mínimo de 1000px, también contaría al __viewport width__ como el scroll, osea, el scroll se cuenta como otra parte más del width; y a veces al poner 100vw estamos agregando también el tamaño del scroll, por eso en estos casos se desborda el elemento, por esto, la recomendación es, si se quiere ocupar el 100% de ancho, usar "100%" no 100vw.

#### Viewport height.

Se escribe "v" de __viewport__  y "h" de **height** __vh__. 

De igual manera que vw los valores van de 0 a 100. 100vh abarca toda el área visible, hablando del alto, en el navegador. En el ejemplo de tener un background-color, si se hace scroll hacia abajo, no le va a dar el color a toda la página, simplemente se lo da al área visible en ese momento del navegador.

### Porcentajes.

Son relativos al tamaño del padre del elemento al cual estamos dándole el porcentaje. Por defecto todos los elementos que son bloques tienen un width del 100%. 

\<Body> no tiene un height declarado porque como una página puede tener un montón de contenido no conviene que \<body> tenga un height definido.


