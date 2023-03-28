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