# Enlaces

Conocidos también por links popularmente. Su objetivo es conectar una página web con otra página web, con un recurso tanto interno como externo, o con otro sitio web.

Tienen el atributo obliatorio href, donde le especificamos la ruta del recurso o sitio que queremos obtener.

También tiene el atributo target, que configura cómo queremos visualizar el recurso o sitio que solicitamos.
**Ejemplo:** \<a  href="https://google.com"  target="_blank">Ir a google\</a>
[Documentación oficial.](https://developer.mozilla.org/es/docs/Web/HTML/Element/a) - [Ejemplo.](https://github.com/Juan122113/curso-html-2022/blob/main/web%20demo/index.html)

## Rutas absolutas

Tienen un protocolo, http o https y son únicas en la red. Se suelen utilizar para rutas externas. [Ejemplo.](https://github.com/Juan122113/curso-html-2022/blob/main/web%20demo/index.html)
**Ejemplo:** \<a  href="https://google.com">Ir a google\</a>

## Rutas relativas
 
Puden se realtivas al punto donde nos encontramos o relativas a la raiz del proyecto. 

No usan protocolo.

Si el recurso se encuentra al mismo nivel (en la misma carpeta) pondremos únicamente el nombre del archivo.

Si necesitamos salir de la carpeta actual usaremos ../ y se ponde uno por cada nivel (carpeta) de la que queramos salir. [Ejemplo 1.](https://github.com/Juan122113/curso-html-2022/blob/main/web%20demo/index.html) [Ejemplo 2.](https://github.com/Juan122113/curso-html-2022/blob/main/web%20demo/paginas/contacto.html)

**Ejemplos:** 
+ \<a  href="paginas/contacto.html">Ir a contacto\</a>
+ \<a  href="/index.html">Ir al inicio\</a> Al poner la barra se le pide que se valla al punto más alto que pueda y desde ahí que empiece a contar.
+ \<a  href="/">Ir al inicio\</a> se puede colocar de esta manera porque el archivo index.html es el archivo que por defecto van a intentar cargar los servidores y los navegadores al ingresar en un sitio web, por esto es muy importante que el archivo principal, el home, el punto de inicio se llame index.html y no de otra forma

## Atributos de los enlaces

**Target:** define donde se abrirá el recurso solicitado. Por norma general siempre que useis rutas absolutas pondreis como valor **"_blank"**, esto hace que la página se abra en otra pestaña. Al ingresar __"_self"__ (el valor por defecto, es como no poner nada) el enlace no se abre en una nueva pestaña. [Ejemplo.](https://github.com/Juan122113/curso-html-2022/blob/main/web%20demo/index.html)

**Download:** Atributo booleano, sirve para descargar el recurso solicitado. 
IMPORTANTE, el recurso debe estar en tu mismo servidor. [Ejemplo.](https://github.com/Juan122113/curso-html-2022/blob/main/web%20demo/index.html)

## Enlaces a puntos específicos.

[Ejemplo.](https://github.com/Juan122113/curso-html-2022/blob/main/web%20demo/paginas/blog.html)

\<nav>

\<p>\<a  href="#post-1">Post 1\</a>\</p>

\<p>\<a  href="#post-2">Post 2\</a>\</p>

\<p>\<a  href="#post-3">Post 3\</a>\</p>

\<p>\<a  href="#post-4">Post 4\</a>\</p>

\<p>\<a  href="#post-5">Post 5\</a>\</p>

\</nav>

**van hacia:**

\<article  id="post-1">

\<h2>Post 1\</h2>

\<p>

Lorem ipsum dolor sit amet consectetur adipisicing elit. Dicta porro sequi quisquam deleniti, in maxime quos aliquid corporis velit necessitatibus soluta a, inventore, praesentium quod dolore dolorem dignissimos ab officiis!

\</p>
\</article>

\<article  id="post-2">

\<h2>Post 2</h2>

\<p>

Lorem ipsum dolor sit amet consectetur adipisicing elit. Facere hic corrupti ducimus consectetur beatae, neque optio, dicta eius nesciunt voluptatibus maiores itaque labore? Possimus necessitatibus exercitationem culpa architecto earum enim.

\</p>
\</article>

Y así con los demás post.

Es importante recordad el sino de # en el enlace.
