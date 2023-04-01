# CSS
Cascading Style Sheets (CSS) es un lenguaje de estilos utilizado para describir la presentación de un documento HTML o XML, (incluyendo dialectos XML como SVG, MathML o XHTML). CSS describe como los elementos deberían ser renderizados en pantalla, en papel, etc.
En cuanto a sintaxis, generalmente se indenta con dos espacios y los comentarios se escriben de la siguiente manera ```/* MyComment */```
La meta básica este lenguaje es permitir al motor del navegador “pintar” elementos en la página con características específicas, como colores, posición o decoración. La sintaxis de CSS consiste en bloques que contienen una ```property```  (es un identificador, que es legible para el humano, que define que característica está siendo considerada) y un ```value``` (describe como la característica debe ser manejada por el motor. Cada propiedad tiene un conjunto de valores válidos).

Para más información, visite la documentación oficial de CSS: https://developer.mozilla.org/en-US/docs/Learn/CSS

Este codigo se puede escribir de 3 formas distintas:
- Inline: Se añade el pedazo de codigo directamente a la etiqueta de apertura del elemento en el documento HTML
- ```<style>```: Añadimos este elemento en el ```<head>``` del documento HTML, con la sintaxis en CSS dentro de este elemento.
- Archivo .css: Se crea un archivo con terminación ```.css``` con todos los estilos, luego este se importa en forma de 

## Declaraciones
Las declaraciones en bloque son declaraciones agrupadas en una estructura delimitada por llaves ```{}``` y tienen el elemento, clase o id a aplicar estos estilos. Cada línea tiene que terminar con un ```;```

``` css
p { 
  font-family: Arial, sans-serif; 
}

.title {
  text-align: center;
}

#perro {
  color: red;
}
```

El primer bloque le aplica una familia de fuentes a todos los elementos ```<p>```, el segundo bloque centra el texto a todos los elementos con la clase ```title``` y el último bloque le aplica el color rojo al elemento con id ```perro```.

## Selectores
Los selectores se utilizan para delimitar que elementos HTML de nuestro documento queremos aplicar determinado estilo.
Los selectores tienen determinada jerarquía, mientras más generales son menos jerarquía tienen. Por ejemplo, si tenemos un selector que delimite todos los párrafos del documento y después tenemos una clase que modifique solo algunos de los párrafos del texto, el navegador le dará prioridad a los estilos de la clase.

1. El selector con más jerarquía es el ```#id```
2. El selector con jerarquia intermedia es el de clase ```.class```
3. Y el que tiene menos jerarquía es el selector de elemento

Aun así, los estilos inline tienen prioridad ante todos estos. También si hay dos estilos con el mismo nivel de jerarquía, se le aplicará el último estilo, por ejemplo

``` css
p {
  color: red;
}

p {
  color: blue;
}
```

El ```<p>``` se renderizará de color azul.
También existe ```!important```, el motor priorizará este estilo sobre todas las cosas

``` css
p { 
  color: red !important; 
}
```

## Pseudoclases y pseudoelementos
Son selectores especiales que permitan seleccionar elementos basados en su estado o posición en el documento.
Algunas psudoclases comunes son:
```:hover```: selecciona un elemento cuando el cursor está sobre el mismo
```:active```: Selecciona un elemento que está siendo cliqueado o presionado
```:focus```: Selecciona un elemento cuando este tiene el foco (cuando el usuario lo cliquea o tabea hacia este elemento)

``` css
a {
  color: blue;
  text-decoration: none;
}

a:hover {
  color: red;
  text-decoration: underline;
}
  
button:active { 
  background-color: red; 
}

button:focus { 
  color: green; 
}
```


## Unidades Absolutas
Las unidades absolutas no son relativas y generalmente son siempre del mismo tamaño en todos lados.

<table>
  <thead>
    <tr>
      <th>Unidad</th>
      <th>Nombre</th>
      <th>Equivale a</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><code>cm</code></td>
      <td>Centímetros</td>
      <td>1cm = 96px/2,54</td>
    </tr>
    <tr>
      <td><code>mm</code></td>
      <td>Milímetros</td>
      <td>1mm = 1/10 de 1cm</td>
    </tr>
    <tr>
      <td><code>Q</code></td>
      <td>Cuartos de milímetros</td>
      <td>1Q = 1/40 de 1cm</td>
    </tr>
    <tr>
      <td><code>in</code></td>
      <td>Pulgadas</td>
      <td>1in = 2,54cm = 96px</td>
    </tr>
    <tr>
      <td><code>pc</code></td>
      <td>Picas</td>
      <td>1pc = 1/6 de 1in</td>
    </tr>
    <tr>
      <td><code>pt</code></td>
      <td>Puntos</td>
      <td>1pt = 1/72 de 1in</td>
    </tr>
    <tr>
      <td><code>px</code></td>
      <td>Píxeles</td>
      <td>1px = 1/96 de 1in</td>
    </tr>
  </tbody>
</table>

Generalmente, la medida más útil de las mencionadas anteriormente es él ```px```

## Unidades Relativas
Estas unidades son relativas a algo más, como por ejemplo el tamaño de letra del elemento principal o el tamaño de la ventana gráfica. La ventaja de usar estas unidades de medida es que con una planificación cuidadosa se puede lograr que el tamaño de los elementos se escalen en relación con todo lo demás de la página

<table>
  <thead>
    <tr>
      <th>Unidad</th>
      <th>Relativa a</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><code>em</code></td>
      <td>Tamaño de letra del elemento padre, en el caso de propiedades tipográficas como font-size y tamaño de la fuente del propio elemento en el caso de otras propiedades, como width.</td>
    </tr>
    <tr>
      <td><code>ex</code></td>
      <td>Altura x de la fuente del elemento.</td>
    </tr>
    <tr>
      <td><code>ch</code></td>
      <td>La medida de avance (ancho) del glifo "0" de la letra del elemento.</td>
    </tr>
    <tr>
      <td><code>rem</code></td>
      <td>Tamaño de la letra del elemento raíz.</td>
    </tr>
    <tr>
      <td><code>lh</code></td>
      <td>Altura de la línea del elemento.</td>
    </tr>
    <tr>
      <td><code>vw</code></td>
      <td>1% del ancho de la ventana gráfica.</td>
    </tr>
    <tr>
      <td><code>vh</code></td>
      <td>1% de la altura de la ventana gráfica.</td>
    </tr>
    <tr>
      <td><code>vmin</code></td>
      <td>1% de la dimensión más pequeña de la ventana gráfica.</td>
    </tr>
    <tr>
      <td><code>vmax</code></td>
      <td>1% de la dimensión más grande de la ventana gráfica.</td>
    </tr>
  </tbody>
</table>


## Colores
En CSS hay varias maneras de especificar los colores.
Se pueden representar con palabras clave como ```red```, ```green```, ```blue```, etc.

También se pueden representar con valores hexadecimales como ```#ffffff```. Los colores hexadecimales están formados por 6 dígitos del sistema hexadecimal, el primer par es para el valor del color rojo, el segundo par para el verde y el tercer para el azul. El valor mínimo sería ```00``` y el máximo ```ff```. Estos colores se pueden abreviar cuando los dos dígitos del par son iguales, por ejemplo ```#ffffff``` se puede abreviar como ```#fff```, ```#ff00ff``` como ```#f0f```, ```#55ff00``` como ```#5f0``` y así consecuentemente.

También se pueden representar con ```rgb()``` y ```rgba()```.
Los colores ```rgb()``` se representan con 3 valores separados por coma, cada uno de estos valores corresponde a rojo, verde y azul. El valor mínimo es 0 y el máximo 255, cuando se le quiere sumar transparencia, aparece otro valor llamado ```alpha``` que controla la opacidad, su valor mínimo es 0 y el máximo 1.


## Variables
Las variables o ```custom properties``` son una característica poderosa de CSS, que permite definir valores reutilizables a lo largo del codigo. Se declaran con ```--``` seguido del nombre de las variables, y luego el valor. Esta variable podrá ser utilizada en todos los elementos heredados de donde esta sea declarada. Una vez definida se puede acceder a la misma con la función ```var()``` que toma como primer argumento el nombre de la variable, y el segundo argumento como un valor default. Este valor se suele utilizar para ahorrar errores de acceso a la variable.

``` css
:root {
  --main-color: #0066cc;
}

h1 {
  color: var(--main-color, green);
}
```

El elemento ```:root``` hace referencia al elemento ```<html>``` por lo que toda la página podrá acceder a esta variable.

Vale aclarar que hay navegadores que no soportan las variables (Internet Explorer), pero la gran mayoría de navegadores modernos las soportan.

## Flexbox
Permite crear diseños flexibles y receptivos en una página web. Flexbox proporciona una forma de diseñar diseños complejos sin tener que recurrir a trucos como utilizar elementos flotantes o posiciones absolutas.
Con Flexbox, los elementos HTML se pueden organizar en filas o columnas, y se pueden ajustar dinámicamente para adaptarse a diferentes tamaños de pantalla y dispositivos. Se puede controlar el comportamiento de los elementos utilizando las propiedades de Flexbox, como "display", "flex-direction", "justify-content", "align-items" y "flex-grow".