# HTML
HTML proviene de HyperText Markup Language. Es un lenguaje de markup estándar utilizado para crear páginas web y otra información que puede ser mostrada en un navegador web. HTML usa varias etiquetas y atributos para describir la estructura y contenido de una página web, incluyendo encabezados, párrafos, listas, links, imágenes y otros tipos de elementos multimedia.
HTML es el bloque de construcción básico para el desarrollo web, y es esencial para crear páginas web estáticas y dinámicas. Puede ser utilizado en conjunto con CSS (Cascading Style Sheets) y JavaScript para crear páginas más interactivas y reactivas.

## Etiquetas
Las etiquetas se usan para definir estructuras y contenido en una página web. Están encerradas entre ```<>``` y usualmente vienen en pares, el ```opening tag``` indicando el inicio de una sección de contenido y el ```closing tag``` indicando el final de la sección.

## Atributos
Proveen a los elementos información adicional, se agregan en el ```opening tag``` del elemento

### ```<!DOCTYPE>```
Está al principio del documento HTML, especifica la versión de HTML que se está usando y ayuda al navegador a interpretar correctamente el codigo

```<!DOCTYPE html>``` 

Esta declaración se usa para documentos HTML5


### ```<html>```
Este ```tag``` es el elemento raíz de un documento HTML. Especifica que el documento es de tipo HTML 


### ```<head>```
Se utiliza para definir una sección del documento HTML. Esta sección provee metadata sobre el documento, tales como título, links a las hojas de estilo, scripts, y otra información que no se muestra en la página. Este tag puede contener varios otros:

#### ```<title>```
Contiene el título con el que se mostrara la página

#### ```<meta>```
Especifica la codificación de caracteres del documento

#### ```<link>```
Linkeea recursos externos, generalmente hojas de estilos (stylesheets)

#### ```<script>```
Linkeea recursos externos, generalmente scripts en JS

Podemos ver el siguiente ejemplo:
```
<!DOCTYPE html>
<html>
  <head>
    <title>My Web Page</title>
    <meta charset="UTF-8">
    <link rel="stylesheet" href="styles.css">
    <script src="script.js"></script>
  </head>
  <body>
    <h1>Welcome to my web page</h1>
    <p>This is my first web page.</p>
  </body>
</html>
```


### ```<body>```
Se utiliza para definir la sección ```body``` del documento HTML. Contiene todo el contenido visible de la página web, tales como títulos, párrafos, imágenes, links y otros elementos.

Podemos ver el siguiente ejemplo:

```
<!DOCTYPE html>
<html>
  <head>
    <title>My Web Page</title>
  </head>
  <body>
    <h1>Welcome to my web page</h1>
    <p>This is my first web page.</p>
    <img src="image.jpg" alt="An image">
    <a href="https://www.example.com">Click here</a> to go to example.com.
  </body>
</html>
```

### ```<h1>, <h2>, ... <h6>```
Se utilizan para definir títulos. Tienen 6 niveles, mientras más grande es el número que acompaña la h el título es menos importante.

Ejemplo:
```
<h1>Welcome to my web page</h1>
<h2>Welcome to my web page</h2>
<h3>Welcome to my web page</h3>
<h4>Welcome to my web page</h4>
<h5>Welcome to my web page</h5>
<h6>Welcome to my web page</h6>
```


### ```<p>```
Se utiliza para definir un párrafo de texto.

```
<p>This is a paragraph of text.</p>
```

### ```<img>```
Se utiliza para insertar imágenes en la página web, no necesita ```tag``` de cierre. Utiliza atributos para especificar la fuente, ancho, alto, etc. de la imagen.

```
<img src="image.jpg" alt="A picture of a cat">
```


### ```<a>```
Este tag se utiliza para crear hipervínculos o ```anchor links```.

```
<a href="https://www.example.com">Click here</a>
```

En este ejemplo el atributo ```href``` especifica una URL, al hacer clic en el anchor te redirija a la URL especificada

```
<a href="#section2">Go to section 2</a>
```

En este ejemplo el anchor te lleva a la sección 2 del documento HTML.

### ```<ul>```
Este tag se utiliza para hacer una lista no ordenada, proviene de "unorderd list".
Este tag si o si tiene que ir acomañado del tag ```<li>``` "list item" que representa cada elemento de la lista.

```
<ul>
  <li>Elemento 1</li>
  <li>Elemento 2</li>
  <li>Elemento 3</li>
</ul>
```

### ```<ol>```
Este tag se utiliza para hacer lisstas ordenadas, proviene de "ordered list". al igual que el tag ```<ul>``` esta acompañado del tag ```<li>```.

```
<ol>
  <li>Elemento 1</li>
  <li>Elemento 2</li>
  <li>Elemento 3</li>
</ol>
```

### ```<strong>```
Sirve para darle enfasis a un texto. Este texto se mostrara en negrita.

```
<p>This sentence contains some <strong>important information</strong>.</p>
```

### ```<em>```
Al igual que el tag ```<strong>``` sirve para dar enfasis. Por defeto el texto se mostrara en italica.

```
<p>This sentence contains some <em>emphasized text</em>.</p>
```

### ```<s>```
Se usa para indicar que el texto tiene un strikethrough. Generalemte sirve para indicar que algo se elimino o no es relevante pero sigue estando visible para la referencia.

```
<p>This is some <s>strikethrough</s> text.</p>
```

### ```<small>```
Se usa para indicar que el texto que contiene es mas pequeño.

```
<p>This is some <small>smaller text</small> in a paragraph.</p>
```

### ```<hr>```
Es un ```self closing tag``` que se usa para crear una "regla horizontal"  o una linea horizontal que separa contenido visualmente

```
<p>This is some content.</p>
<hr>
<p>This is some more content.</p>
```