# Diseño adaptable a dispositivos móviles.

## Mediaqueris.

[Documentación oficial.](https://developer.mozilla.org/es/docs/Web/CSS/Media_Queries/Using_media_queries)
[Ejemplos.](https://github.com/Juan122113/CursoCSS/tree/main/11-MediaQueris)

Nos permiten modificar nuestra página web en función del tipo de dispositivo, la orientación de la pantalla o el ancho del viewport y también nos permite controlar otros casos.

Las mediaqueris son un tipo de condicional en las que podemos declarar estilos, donde esos estilos solo se aplicarán en caso de que la mediaquery cumpla la condición y para eso está max width y min width.

### Max width.

En un mediaquery indica cual será el valor máximo que debe tener el viewport para que se aplique el CSS que está dentro del mediaquery. Por ejemplo, si tenemos un valor de max width de 600px significa que ese mediaquert solamente aplicará los estilos que tiene dentro cuando el viewport sea menor a 600px, porque max width define el tamaño máximo para que se cumpla la condición.

### Min width.

En un mediaquery indica cual será el valor mínimo que debe tener el viewport para que se aplique el CSS que se encuentra dentro de el mediaquery. Por ejemplo, si tenemos un min width de 600px significa que el mediaquery solamente entrará cuando el viewport sea mayor a 600px, porque min width define el tamaño mínimo que necesita la mediaquery para que se cumpla la condición.

### Reglas de escritura.

Se recomienda poner las mediaqueris al final de todos los estilos que se hayan escrito.

Se pueden escribir más de un mediaquery en CSS, pero siempre hay formas para esto, por ejemplo si se crean dos mediaqueris que sean de ancho máximo, y el primero sea a 800px y el segundo a 600px y que cada uno tenga un color diferente, se van a ver bien ya que el max width de mayor valor está escrito antes que el de menor valor; en el caso de que estuvieran escritos al revés solo se vería el color del mayor valor. Por ende, la mejor manera de escribir más de un mediaquery cuando usas max width es poner siempre el valor mayor al principio y de ahí en cascada. Pero esto es al revés cuando se usa min width, en este caso primero se deben colocar los valores con menor valor y así en cascada.

## Mobile first vs Desktop first.

Estas son dos técnicas de diseño adaptable. Adaptar nuestras páginas a cualquier dispositivo se ha vuelto imprescindible en una época de diversos dispositivos con acceso a internet.

### Desktop first.

La técnica desktop first se basa en maquetar primero el sitio o nuestra página pensando en un tamaño grande, es decir, en un tamaño de escritorio para después adaptarlo a tamaños más pequeños (mobile).

### Mobile first.

La técnica de mobile first se basa en maquetar primero el sitio pensando en dispositivos móviles, y posteriormente agregar media queris para adaptarlo a un tamaño más grande (Desktop). Esta es la mejor opción debido a que es más fácil adaptar un diseño de Mobile a Desktop, que de Desktop a Mobile.


