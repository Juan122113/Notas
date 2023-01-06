# Custom properties.

[Documentación oficial.](https://developer.mozilla.org/en-US/docs/Web/CSS/Using_CSS_custom_properties)
[Ejemplos.](https://github.com/Juan122113/CursoCSS/tree/main/14-Custom-properties)

También llamadas variables en CSS. Nos permiten almacenar valores permitidos en las propiedades de CSS. Es decir, en estas variables vamos a poder almacenar cualquier valor permitido en las propiedades de CSS, por ejemplo royalblue, block, 20px 0. Es como cualquier propiedad de CSS, solamente que nosotros vamos a definir el nombre de esa propiedad y esa propiedad va a guardar un valor para posteriormente reutilizarlo. Las propiedades personalizadas normalmente se declaran en la pseudo clase root. La pseudo clase root es similar al selector HTML, solamente que root tiene mayor especificidad. Al usar root estamos definiendo que las custom properties se van a declarar en la raíz del documento, es decir, en el HTML y esto hará que todos los elementos que se encuentren dentro del HTML van a poder acceder a las custom properties o variables personalizadas.

Las custom properties son válidas también para los hijos

## Nombramiento.

Son personalizadas porque tu vas a definir el nombre y para definir una custom propertie se ponen primero dos guiones medios "--" y el nombre que se quiera. Si se usan más de una palabra no se pueden poner espacios, en vez de eso se usan un guion medio o un guion bajo.  

## Selección.

Para llamar (usar) a una custom properties, su usa, después de la propiedad, **var()**, y dentro de el paréntesis el nombre de la custom propertie. Ejemplo:

:root{

--bordes: 1px  solid  #000;

}

.title{

border: var(--bordes);

}

También se pueden poner valores de repuesto o fallbacks poniendo una coma después del primer valor dentro del __var()__. Ejemplo:




