# **SECCION 9 BLOG CAFE. CREANDO UN PROYECTO CON HTML Y CSS**

## **81. Añadiendo CSS global**
Estos son algunos elementos de código **css** que se **necesitan** para **realizar** (casi) cualquier página web.
<!---->
### **81.1 box-Sizing border-box**
Con este nos ayudara a que nuestros `border`, `padding`, etc. No afecte las **medidas** del **ancho** de nuestro **elemento**.
```css
html {
  box-sizing: border-box;
}
*, *:before, *:after {
  box-sizing: inherit;
}
```
<!---->
### **81.2 Rem(font-size)**
Para que podamos **manipular** de una forma más fácil el **tamaño** de cualquier elemento y poder utilizar `rem` se tiene que aplicar lo siguiente en el **html**.
```css
html{
    font-size: 62.5%;
}
```
Con esto el valor de `1rem` será **igual** a `10px`.
<!---->
### **81.3 Enlaces (text-decoration)**
Para quitar el **interlineado** a los **enlaces** es muy fácil y se aplica la siguiente sintaxis.
```css
a{
    text-decoration: none; 
}
```
### **81.4 Utilidades**
En nuestro proyecto muchas veces necesitaremos **quitar** o colocar **elementos** que están por **defecto**. Las **utilidades** nos ayudaran a **ahorrarnos** líneas de código y establecer una `clase` para estas posibles **variables** de nuestros elementos y **agregarlas** a nuestro **index**. Algunos ejemplos son los siguientes.
```css
.no-margin{ /*clase para quitar el margen*/
    margin: 0;
}
.no-padding{
    padding: 0;
}
.centrar-texto{
    text-align: center;
}
```

## **82. Creando el Header**

### **82.1 Imagen fluida (center center)**
Al colocar los valores `center center` en un `background- position` esto hara que nuestra imagen mantenga una **fluides** para que se vea bien en **diferentes tamaños**. Cuando utilizamos un `background-size: cover;` normalmente se utiliza un `center center`. Lo puedes **manipular** colocando **variables** como `left center` o `right center`, etc. También se pueden usar **porcentajes** pero ya son valores más **complicados** y en muchos casos **no** son **útiles**. 

## **83. CSS al Header**
<!--1-->
### **83.1 Span**
El contenedor `span` servirá para aplicar **estilo** a un texto en concreto. Este tiene etiquetas de **abrir** y **cerrar**. Un ejemplo con sintaxis seria lo siguiente.
```css
<h1 class="logo__nombre">Black<span class="logo__bold">&Pink</span> </h1>
```
<!--2-->
### **83.2 Recapitulo (alineacion de elementos)**
`justify-content` alineara elementos **horizontalmente**.
`align-items` alineara elementos **verticalmente**.
<!--3-->
### **83.2 Recapitulo (block & inline)**
`display: block;` Los elementos se colocarán uno de **bajo** del **otro**.
`display: inline;` Los elementos se colocarán uno a la **derecha** del **otro**.

## **85. Finalizando el Blog**
### **85.1 Last of type**
`:last-of-type ` Es una **pseudo clase** que seleccionara el **último elemento** de una **clase** con el **mismo nombre**.
<!--1-->
### **85.2 Mayusculas (uppercase)**
La variable `uppercase` nos ayudara a cambiar todas las letras a **mayúscula** de nuestro elemento deseado y se realizara con la siguiente sintaxis: `text-transform: uppercase;`
<!--2-->
### **85.3 Inline-Block**
Al colocar un `display inline` por alguna razón, este **no** tomara en cuenta ni los `margin` ni los `width`. Para poder **cambiar** eso y que nuestro elemento siga siendo `inline` lo que tenemos que hacer es **colocar** un `inline-block`. Esto para que nuestro `inline` siga siendo un **elemento** `inline` pero tome en cuenta las **propiedades** que por default no se podrían utilizar con un `inlne`. Esto se ha estado **utilizando menos** gracias a a **flexbox**.

## **86. Creando la barra lateral**
<!---->
### **86.1 Listas en el HTML (ul ol)**
Para realizar **listas no ordenadas** se utiliza `ul`. La sintaxis seria la siguiente.
```html
<ul>
    <li>HTML5</li>
    <li>CSS</li>
</ul>
```
Para las **listas ordenadas** se usa `ol`. Así se vería la sintaxis.
```html
<ol>
    <li>HTML5</li>
    <li>CSS</li>
</ol>
```
<!--1-->
### **86.2 Banderas en las clases (--)**
Los dos guiones **" -- "** van a indicar las **banderas** dentro de nuestra **clase**. Esto quiere decir que esos dos guiones se refieren a que van a **heredar** las **características** de **otra clase**, **pero** en algo va a **cambiar**.
```css
.boton--secundario{
    background-color: var(--primario);
}
```
<!--2-->
### **86.3 Quitar viñetas (list style)**
Para **quitar** las **viñetas** de nuestro `ul` se hace con `list-style`. Así se aplicaría con sintaxis.
```css
.cursos{
    list-style: none;
}
```

## **87. Creando el Footer**

### **87.1 Contenedor(width min)**
La forma **tradicional** para que nuestra página fuera **responsive** era hacer lo siguiente.
```css
.contenedor{
    max-width: 120rem; 
    width: 90%;
    margin: 0 auto; /*centrar contenido en la pantalla*/
}
```
El `width` tomara el `90%` de la **página** para que ese sea el espacio en el **contenido**. El `max-width` es para que en **pantallas** más **grandes** tome `1200px` de la página del total.
La forma nueva es la siguiente.
```css
.contenedor{
    width: min(90%, 120rem);
}
```
El código se **leerá** de la siguiente manera. De los siguientes valores, **aplica** el que sea el **menor** (`min`) de los **dos**. El `90%` del **tamaño** de la **página** o `1200px`.

## **91. HTML para la página de Contacto**

### **91.1 Accecibilidad Web (for)**
La **accesibilidad web** se refiere a que nuestra página pueda ser accesible a **cualquier** tipo de **personas**, ya sean *ciegas* o con problemas en la *movilidad* de la mano. En los **formularios** para ayudar en esto, tenemos que poner el atributo `for=""` en nuestra etiqueta `<label>`. Para que esto funcione tenemos que poner en nuestro `<input>` un `id=""`. Así sería un ejemplo con sintaxis.
```html
<label for="nombre">Nombre</label>
<input type="text" placeholder="Tu Nombre" id="nombre">
```
#### ***Recordatorio.*** Los `id` solo se pueden utilizar una vez por página.

## **92. CSS al Formulario de Contacto**

### **Margin negativo**
Cuando utilizamos un margin y le asignamos una cantidad de pixeles negativa, esta nos moverá nuestro contenido hacia arriba (margin-top), abajo(margin-bottom), etc. Esto sería un ejemplo con sintaxis.
```css
.formulario{
    background-color: var(--blanco);
    margin: -5rem auto 0 auto;
    width: 95%;
    padding: 5rem;
}
```

## **93. Mejorando el Performance con Lazy Loading**
Lo que hará este performance es que al colocar un `loading="lazy"` en una etiqueta `img` y/o un `iframe`, esta ira cargando poco a poco el contenido a medida que vamos recorriendo la página. Esto es muy útil cuando tenemos muchas de estas etiquetas, y servirá para que no se nos sobrecargue la página.   

## **94. Mejorando el Performance con Preload** 
`Preload` va a cargar inmediatamente los elementos que consideres necesarios tenerlos lo más pronto posible.
Estos son algunos ejemplos de cómo se tienen que escribir.
Como hoja de estilos se utilizará un `style`.
```html
<link rel="preload" href="css/styles.css" as="style">
<link rel="stylesheet" href="css/styles.css">
```
Cuando se tiene una librería externa se utiliza un `crossorigin` y al ser una fuente será con `font`
```html
<link rel="preload" href="https://fonts.googleapis.com/css2?family=Open+Sans&family=PT+Sans:wght@400;700&display=swap" crossorigin="crossorigin" as="font" >
<link href="https://fonts.googleapis.com/css2?family=Open+Sans&family=PT+Sans:wght@400;700&display=swap" rel="stylesheet">
```
Incluso se pueden descargar audios, imágenes, videos, `iframes`, etc. En una imagen se colocaría con un `image`.
```html
<link rel="preload" href="img/blog1.jpg" as="image">
```

En el preload de fonts ocurre un problema en la consoloa, asi que por el momento utilizaremos la siguiente sintaxis.
```html
<link rel="preload" href="https://fonts.googleapis.com/css2?family=Open+Sans&family=PT+Sans:wght@400;700&display=swap" as="style">
```

## **95. Mejorando el Performance con Prefetch**
La función de **Prefetch** servirá para cargar la siguiente página que esperamos que el usuario visite, esto para mejorar la experiencia de usuario y sea más rápido. La sintaxis quedaría de la siguiente manera.
```html
<link rel="prefetch" href="cursos.html" as="document">
```
Primero configuramos nuestro `link` como Prefetch, después la dirección del enlace de la página y lo definimos como `document` ya que es un archivo html.

El prefetch solo se utilizara en la página que nuestros usuarios visiten más, estos datos se obtienen desde [Google Analytics](https://analytics.google.com/analytics/web/provision/#/provision).

## **96. Mejorando el Performance con Imagenes Webp**
Las imágenes en las páginas web suelen ser muy pesadas. Así que por eso mismo tenemos que buscar otros formatos de img para poder resolver esto, una de esas es `webp`.
webp a comparación del formato tradicional jpg, su tamaño será mucho menos de la mitad que este. No siempre podemos colocar imágenes en formato webp, ya que no todos los navegadores tendrán soporte a este, así que lo que tenemos que hacer va a ser lo siguiente.

Usaremos una etiqueta llamada `picture`, esta etiqueta servirá como contenedor para establecer etiquetas source e img. Esta sería la sintaxis con ejemplo.
```html
<picture>
    <source loading="lazy" srcset="img/blog1.webp" type="image/webp">
    <img loading="lazy" src="img/blog1.jpg" alt="imagen blog">
</picture>  
```

## ****

## ****

## ****

## ****

## ****
