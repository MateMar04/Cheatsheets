# CSS
Cascading Style Sheets (CSS) es un lenguaje de estilos utilizado para describir la presentacion de un documento HTML o XML, (incluyendo dialectos XML com SVG, MathML o XHTML). CSS describe como los elementos deberian ser renderizados en pantalla, en papel, etc.
En cuanto a sintaxis generalmente se indenta con dos espacios y los comentarios se escriben de la siguiente manera ```/* MyComment */```
La meta basica este lenguaje es permitir al motor del navegador "pintar" elementos en la pagina con caracteristicas especificas, como colores, poscicion o decoracion. La sintaxis de CSS consiste en bloques que contienen una ```property```  (es un identificador, que es legible para el humano, que define que caracteristica esta siendo considerada) y un ```value``` (describe como la caracteristica debe ser manejada por el motor. Cada propiedad tiene un conjunto de valores validos).
Este codigo se puede escribir de 3 formas distintas:
- Inline: Se añade el pedazo de codigo directamente a la etiqueta de apertura del elemento en el documento HTML
- ```<style>```: Añadimos este elemento en el ```<head>``` del documento HTML, con la sintaxis en CSS dentro de este elemento.
- Archivo .css: Se crea un archivo con terminacion ```.css``` con todos los estilos, luego este se importa en forma de 

## Declaraciones
Las declaraciones en bloque son declaraciones agrupadas en una estructura delimitada por llaves ```{}``` y tienen el elemento, clase o id a aplicar estos estilos. Cada linea tiene que terminar con un ```;```

```
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

El primer bloque le aplica una familia de fuente a todos los elementos ```<p>```, el segundo bloque centra el texto a todos los elementos con la clase ```title``` y el ultimo bloque le aplica el color rojo a el elemento con id ```perro```.

## Selectores
Los selectores se utilizan para delimitar que elementos HTML de nuestro documento queremos aplicar determinado estilo.
Los selectores tienen determinada jerarquia, mientras mas generales son menos jerarquia tienen. Por ejemplo si tenemos un selector que delimite todos los parrafos del documento y despues tenemos una clase que modifique solo algunos de los parrafos del texto, el navegador le dara prioridad a los estilos de la clase.

1. El selector con mas jerarquia es el ```#id```
2. El selector con jerarquia intermedia es el de clase ```.class```
3. Y el que tiene menos jerarquia es el selector de elemento

Aun asi, los estilos inline tienen prioridad ante todos estos. Tambien si hay dos estilos con el mismo nivel de jerarquia, se le aplicara el ultimo estilo, por ejemplo

```
p {
  color: red;
}

p {
  color: blue;
}
```

El ```<p>``` se renderizara de color azul.
Tambien existe ```!important```, el motor priorizara este estilo sobre todas las cosas

```
p { 
  color: red !important; 
}
```

## Pseudoclases y pseudoelementos
Son selectores especiales que permitan seleccionar elementos basados en su estado o posicion en el documento.
Algunas psudoclases coomunes son:
```:hover```: selecciona un elecmento cuando el cursor esta sobre el mismo
```:active```: Selecciona un elemento que esta siendo cliqueado o presionado
```:focus```: Selecciona un elemento cuando este tiene el foco (cuando el usuario lo cliquea o tabea hacia este elemento)

```
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

Generalmente la medida mas util de las mencionadas anteriormente es el ```px```

## Unidades Relativas
Estas unidades son relativas a algo mas, como por ejemplo el tamaño de letra del elemento principal o el tamaño de la ventana grafica. La ventaja de usar estas unidades de medida es que con una planificacion cuidadosa se puede lograr que el tamaño de los elementos se escalen en relacion con todo lo demas de la pagina

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
