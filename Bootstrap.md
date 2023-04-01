# Bootstrap
Bootstrap es un popular framework de front-end utilizado para diseñar y desarrollar sitios web responsivos y móviles.
Bootstrap proporciona un conjunto de componentes preconstruidos en HTML, CSS y JavaScript, como formularios, botones, modales, barras de navegación y carruseles, que los desarrolladores pueden usar para construir páginas web rápida y fácilmente. El framework también incluye un sistema de rejilla que permite a los desarrolladores crear diseños responsivos para sus sitios web que se adaptan a diferentes tamaños de pantalla y dispositivos. 
Uno de los principales beneficios de usar Bootstrap es que simplifica el proceso de desarrollo web al proporcionar un conjunto estándar de componentes de interfaz de usuario y estilos que se pueden personalizar fácilmente para satisfacer requisitos de diseño específicos.
Para incluir bootstrap en nuestro proyecto se deben pegar las siguientes líneas en el ```<head>``` del documento HTML:
``` html
<link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha2/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-aFq/bzH65dt+w6FI2ooMVUpc+21e0SRygnTpmBvdBgSdnuTN7QbdgL+OapgHtvPp" crossorigin="anonymous">
<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha2/dist/js/bootstrap.bundle.min.js" integrity="sha384-qKXV1j0HvMUeCBQ+QVp7JcfGl760yU08IQ+GpUo5hlbpg51QRiuqHAJz8+BrxE/N" crossorigin="anonymous"></script>
```

Para más información, visite la documentación oficial de Bootstrap: https://getbootstrap.com/docs/5.3/getting-started/introduction/

## Elementos de Bootstrap

### Grid
Bootstrap Grid es un sistema de diseño flexible utilizado en la construcción de sitios web responsivos. Se compone de filas y columnas que se pueden ajustar para adaptarse a diferentes tamaños de pantalla y dispositivos. La estructura de la cuadrícula es una de las características más importantes de Bootstrap y permite una organización eficiente del contenido en la página.

En Bootstrap Grid, una fila se define como un contenedor horizontal que contiene una o más columnas. Cada columna es un contenedor vertical que se puede ajustar para ocupar un número determinado de columnas dentro de la fila. La cuadrícula se divide en doce columnas, lo que significa que una columna puede ocupar una o varias columnas en función de sus necesidades.

Utiliza clases CSS para definir el ancho de las columnas y las filas, lo que hace que sea fácil de implementar en cualquier sitio web. Las clases se utilizan para establecer el ancho de la columna en función del número de columnas que se desee que ocupe. Por ejemplo, si se desea que una columna ocupe todo el ancho de la fila, se puede utilizar la clase "col-12".

#### Container
es un elemento de diseño que se utiliza para envolver y centrar el contenido en una página web. Se utiliza para crear un área limitada en la página web que mantiene el contenido organizado y fácil de leer.
El contenedor en Bootstrap se crea utilizando el elemento HTML "div" con una clase "container" o "container-fluid". La clase "container" se utiliza para crear un contenedor con un ancho fijo que se ajusta automáticamente a los diferentes tamaños de pantalla, mientras que la clase "container-fluid" se utiliza para crear un contenedor que ocupa todo el ancho de la pantalla.
Dentro del contenedor, se pueden colocar elementos como filas, columnas, texto, imágenes y otros elementos de diseño. Es importante recordar que cualquier elemento que se coloque dentro del contenedor se ajustará automáticamente para adaptarse al ancho del contenedor.

#### Row
Es un elemento básico del sistema de cuadrícula de Bootstrap, que se utiliza para organizar el contenido en filas horizontales, se crean mediante el uso del elemento HTML "div" con la clase "row".
Cada una de ellas consta de doce columnas, por lo que es importante recordar que todas las columnas dentro de la row deben sumar un máximo de doce columnas.
Son responsivas por diseño, lo que significa que se ajustan automáticamente para adaptarse al ancho de la pantalla y al dispositivo del usuario.

#### Col
Las columnas en Bootstrap se crean mediante el uso del elemento HTML "div" con una clase de tamaño de columna específica.
Las columnas en Bootstrap siempre se deben colocar dentro de una fila, que se crea utilizando el elemento "div" con la clase "row". Es importante recordar que la suma de las clases de tamaño de columna en una fila nunca debe exceder 12, ya que Bootstrap utiliza una cuadrícula de 12 columnas.

-   col-xxs-* (Extra extra pequeño): Ancho máximo de 576 píxeles
-   col-xs-* (Extra pequeño): Ancho máximo de 576 píxeles
-   col-sm-* (Pequeño): Ancho máximo de 768 píxeles
-   col-md-* (Mediano): Ancho máximo de 992 píxeles
-   col-lg-* (Grande): Ancho máximo de 1200 píxeles
-   col-xl-* (Extra grande): Ancho máximo de 1400 píxeles

## Componentes
Bootstrap proporciona una amplia variedad de componentes de interfaz de usuario (UI) preconstruidos. Se pueden utilizar para crear fácilmente sitios web y aplicaciones web receptivas y atractivas.
Algunos ejemplos son:
Navbars, Buttons, Carousels, Forms, Cards, Alerts, entre muchos otros.

## Iconos
es una biblioteca de iconos de fuente de código abierto diseñada específicamente para su uso con Bootstrap. Ofrece una gran variedad de iconos vectoriales escalables, lo que significa que se pueden ajustar a cualquier tamaño sin perder calidad. Se proporciona en formato SVG.
Para importar estos iconos es necesario pegar lo siguiente en el ```<head>``` del documento HTML:

``` html 
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap-icons@1.10.3/font/bootstrap-icons.css">
```


## Flexbox
Bootstrap ofrece una serie de clases predefinidas que utilizan las propiedades de Flexbox para controlar el comportamiento de los elementos HTML.

-   "d-flex": se utiliza para indicar que un elemento debe utilizar Flexbox para organizar su contenido.
-   "flex-row": se utiliza para crear una fila de elementos organizados en Flexbox.
-   "flex-column": se utiliza para crear una columna de elementos organizados en Flexbox.
-   "justify-content-*": se utiliza para alinear los elementos horizontalmente en un contenedor utilizando diferentes opciones, como "start", "end", "center", "between" y "around".
-   "align-items-*": se utiliza para alinear los elementos verticalmente en un contenedor utilizando diferentes opciones, como "start", "end", "center" y "stretch".
-   "flex-grow-*": se utiliza para indicar cuánto espacio adicional se debe asignar a un elemento en un contenedor
-   "flex-nowrap": indica que los elementos deben ajustarse a una sola fila o columna y no se deben envolver.
-   "flex-wrap": indica que los elementos deben ajustarse a una sola fila o columna, pero pueden envolverse si no caben en el espacio disponible.
-   "flex-wrap-reverse": indica que los elementos deben ajustarse a una sola fila o columna, pero si se envuelven, deben comenzar en el extremo opuesto del contenedor.