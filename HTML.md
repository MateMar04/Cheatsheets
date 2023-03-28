HTML proviene de HyperText Markup Language. Es un lenguaje de markup estándar utilizado para crear páginas web y otra información que puede ser mostrada en un navegador web. HTML usa varias etiquetas y atributos para describir la estructura y contenido de una página web, incluyendo encabezados, párrafos, listas, links, imágenes y otros tipos de elementos multimedia.
HTML es el bloque de construcción básico para el desarrollo web, y es esencial para crear páginas web estáticas y dinámicas. Puede ser utilizado en conjunto con CSS (Cascading Style Sheets) y JavaScript para crear páginas más interactivas y reactivas.
En cuanto a sintaxis, generalmente se indenta con dos espacios.

Para más información, visite la documentación oficial de HTML: https://developer.mozilla.org/en-US/docs/Web/HTML


## Etiquetas
Las etiquetas se usan para definir estructuras y contenido en una página web. Están encerradas entre ```<>``` y usualmente vienen en pares, el ```opening tag```  (```<>```) indicando el inicio de una sección de contenido y el ```closing tag``` (```</>```) indicando el final de la sección.
Hay etiquetas que no necesitan ```closing tag```, estas se llaman ```self closing tags```
Los comentarios tienen la siguiente sintaxis ```<!-- myComent -->```. Esta sintaxis se usa para comentarios de una sola línea o comentarios multilínea. 


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
Se utiliza para insertar imágenes en la página web, no necesita ```tag``` de cierre. Utiliza atributos para especificar la fuente, ancho, alto, etc. de la imagen. Esta es una ```self closing tag```

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
Este tag si o si tiene que ir acompañado del tag ```<li>``` "list item" que representa cada elemento de la lista.

```
<ul>
  <li>Elemento 1</li>
  <li>Elemento 2</li>
  <li>Elemento 3</li>
</ul>
```


### ```<ol>```
Este tag se utiliza para hacer listas ordenadas, proviene de "ordered list". Al igual que el tag ```<ul>``` está acompañado del tag ```<li>```.

```
<ol>
  <li>Elemento 1</li>
  <li>Elemento 2</li>
  <li>Elemento 3</li>
</ol>
```


### ```<strong>```
Sirve para darle énfasis a un texto. Este texto se mostrará en negrita.

```
<p>This sentence contains some <strong>important information</strong>.</p>
```


### ```<em>```
Al igual que el tag ```<strong>``` sirve para dar énfasis. Por defecto, el texto se mostrará en itálica.

```
<p>This sentence contains some <em>emphasized text</em>.</p>
```


### ```<s>```
Se usa para indicar que el texto tiene un strikethrough. Generalmente, sirve para indicar que algo se eliminó o no es relevante, pero sigue estando visible para la referencia.

```
<p>This is some <s>strikethrough</s> text.</p>
```


### ```<small>```
Se usa para indicar que el texto que contiene es más pequeño.

```
<p>This is some <small>smaller text</small> in a paragraph.</p>
```


### ```<hr>```
Es un ```self closing tag``` que se usa para crear una "regla horizontal"  o una línea horizontal que separa contenido visualmente

```
<p>This is some content.</p>
<hr>
<p>This is some more content.</p>
```


### ```<br>```
Es un ```self closing tag``` que se usa para crear un salto de línea

```
<p>This is some content.<br>This is some more content on a new line.</p>
```


### ```<form>```
Es un elemento que se utiliza para crear un formulario que el usuario tenga que completar. Se pueden agregar distintos tipos de campos con el tag ```<input>```, como campos de texto, radiobuttons, checkboxes, dropdowns, botones, etc

```
<form action="/submit-form" method="POST">
  <label for="name">Name:</label>
  <input type="text" id="name" name="name"><br><br>
  <input type="submit" value="Submit">
</form>
```

En este ejemplo el atributo ```action``` especifica la URL donde la información será enviada. y el atributo ```method``` especifica el ```HTTP request method``` que puede ser ```POST```, ```GET```, entre otros.


### ```<div>```
Es un elemento que se utiliza para agrupar otros elementos y aplicar estilos colectivamente. Es un contenedor genérico que no tiene ni especifica, sentido o propósito. Estos tags se pueden anidar para crear una jerarquía


### ```<nav>```
Se usa para definir una "navbar", una sección de la página que generalmente suele ser el menú y contiene links a otras páginas o secciones

```
<nav>
  <ul>
    <li><a href="/">Home</a></li>
    <li><a href="/about">About Us</a></li>
    <li><a href="/contact">Contact Us</a></li>
  </ul>
</nav>
```


### ```<footer>```
Se utiliza para definir un "footer", una sección de la página. Generalmente, esta contiene información sobre el autor, copyright, fuentes, medios de contacto, links, etc.

```
<footer>
  <p>&copy; 2023 My Website. All rights reserved.</p>
  <nav>
    <ul>
      <li><a href="#">Home</a></li>
      <li><a href="#">About</a></li>
      <li><a href="#">Contact</a></li>
    </ul>
  </nav>
</footer>
```




## Atributos Globales

### accesskey
Se usa para proveer un atajo de teclado para acceder a un elemento particular

```
<button accesskey="s">Save</button>
```


### class
Especifica una o más clases para un elemento. Esto sirve para manipular el estilo mediante CSS o JavaScript.

```
<button class="success">Save</button>
```


### contenteditable
Se usa para hacer que un elemento sea editable por el usuario

```
<div contenteditable="true">
  This text can be edited by the user.
</div>
```


### hidden
Se usa para esconder un elemento del usuario en una página web 

```
<div hidden>
  This content is hidden from the user.
</div>
```


### id
Especifica un identificador único para un elemento, se puede utilizar para manipular el elemento mediante CSS o JavaScript.

```
<button id="success">Save</button>
```


### href
Especifica la URL de un hipervínculo

```
<button href="youtube.com">Save</button>
```


### style
Específica estilos CSS en línea para un elemento

```
<div style="background-color: blue; color: white; padding: 10px;">
  This text has a blue background and white text.
</div>
```


### title
Específica información adicional sobre un elemento, generalmente se muestra como información.

```
<a href="https://www.example.com" title="Visit Example.com">Example</a>
```


## Otros atributos

### accept
Este atributo toma valores separados por una “coma” los tipos de archivos que están aceptados en ese campo.

```
<input type="file"
       name="poster"
       accept="image/png, image/jpeg">
```


### autocomplete
Se usa para controlar si el campo del formulario tendría que tener el valor automáticamente completado por el navegador o no.

```
<form>
  <label for="username">Username:</label>
  <input type="text" id="username" name="username" autocomplete="on">
  <br>
  <label for="password">Password:</label>
  <input type="password" id="password" name="password" autocomplete="off">
</form>
```

### alt
Se utiliza para proveer texto a una imagen, en caso de que la imagen no pueda ser mostrada por alguna razón.

```
<img src="image.jpg" alt="A red sports car">
```


### disabled
Sirve para deshabilitar un elemento input, tal como un botón, campo de texto, etc.

```
<button type="button" disabled>Click me</button>
```


### maxlength
Sirve para poner un límite máximo de caracteres en un campo de texto.

```
<input type="text" name="username" maxlength="20">
```


### readonly
Sirve para hacer que un campo de texto sea solo apto para la lectura. Aun así el texto dentro de este campo puede ser copiado.

```
<input type="text" name="username" value="johndoe" readonly>
```


### required
Se usa para indicar que un campo debe ser completado obligatoriamente

```
<input type="text" name="username" required>
```


### rel
Se usa para especificar la relación entre el documento actual y el documento linkeado en un "anchor"

```
<a href="https://example.com" rel="noopener noreferrer">Example</a>
```

En este ejemplo, él ```noopener noreferrer``` sirve para que la página linkeada no tenga información sobre el documento actual, ya que esto puede ser usado maliciosamente.


### target
Se utiliza para especificar el contexto de búsqueda.

```
<a href="https://example.com" target="_blank">Example</a>
```

Los más comunes son:
```_self```, se abre en la misma tab
```_blank``` se abre en una tab nueva


### src
Atributo que se utiliza para especificar la fuente de multimedia o un archivo que se mostrara en la página web. Se puede usar en los tags ```<img>```, ```<audio>```, ```<video>``` y ```<script>```

```
<img src="image.jpg" alt="Image description">
<script src="script.js"></script>
```


### value
Sirve para especificar el valor de un elemento de entrada (`<input>`), como un campo de texto, un botón o un elemento de selección.

Por ejemplo, en un campo de entrada de texto, el atributo `value` se utiliza para establecer el texto predeterminado que se mostrará en el campo antes de que el usuario lo modifique.

```
<input type="radio" name="genero" value="masculino"> Masculino
<input type="radio" name="genero" value="femenino"> Femenino
<input type="radio" name="genero" value="otro"> Otro
```



## ```<input>``` types

Estos son los tipos más comunes. Para verlos todos visite la documentación de HTML.

`text`: Crea un campo de entrada de texto en el que se puede ingresar texto. 

`password`: Crea un campo de entrada de contraseña en el que los caracteres ingresados se ocultan.

`number`: Crea un campo de entrada para números.

`checkbox`: Crea una casilla de verificación que se puede marcar o desmarcar.

`radio`: Crea un botón de opción que permite seleccionar una opción de un conjunto de opciones mutuamente excluyentes.

`submit`: Crea un botón para enviar el formulario.

`reset`: Crea un botón para restablecer los valores del formulario a su estado original.

`file`: Crea un campo de entrada para seleccionar un archivo del sistema.

`date`: Crea un campo de entrada para fechas.

`email`: Crea un campo de entrada para direcciones de correo electrónico.