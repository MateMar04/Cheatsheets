# HTML
HTML proviene de HyperText Markup Language. Es un lenguaje de markup standard utilizado para crear paginas web y otra informacion que puede ser mostrada en un navegador web. HTML usa varias etiquetas y atributos para describir la estructura y contenido de una pagina web, icluyendo encabezados, parrafos, listas, links, imagens y otros tipos de elementos multimedia.
HTML es el bloque de construccion basico para el desarrollo web, y es escencial para crear paginas web estaticas y dinamicas. Puede ser usado en conjunto con CSS (Cascading Style Sheets) y JavaScript para crear paginas mas interactivas y reactivas.

## Etiquetas
Las estiquetas se isan para definir estructuras y contenido en una pagina web. Estan encerradas entre ```<>``` y usualmente vienen en pares, el ```opening tag``` indicando el inicio de una seccion de contenido y el ```closing tag``` indicando el final de la seccion.

## Atributos
Proveen a los elementos informacion adicional, se agregan en el ```opening tag``` del elemento

### ```<!DOCTYPE>```
Esta al principio del documento html, especifica la version de html que se esta usando y ayuda al navegador a interpretar correctamente el codigo

```<!DOCTYPE html>``` 

Esta declaracion se usa para documentos HTML5


### ```<html>```
Este ```tag``` es el elemento raiz de un documento HTML. Especifica que el documento es de tipo HTML 


### ```<head>```
Se usa para deefinir una seccion del documento HTML. Esta seccion provee metadata sobre el documento, tales como titulo, links a las hojas de estilo, scripts, y otra informacion que no se muestra en la pagina. Este tag puede conterener varios otros:

#### ```<title>```
Contiene el titulo con el que se mostrara la pagina

#### ```<meta>```
Especifica la codificacion de caracteres del documento

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


### \<body>
Se usa para definir la seccion ```body``` del documento HTML. Contiene todo el contenido visible de la pagina web, tales como titulos, parrafos, iamgenes, links y otros elementos.

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
Se usan para definir titulos. Tienen 6 niveles, mientras mas grande es el numero que acompaña la h el titulo es menos importante.

Ejemplo:
```
<!DOCTYPE html>
<html>
  <head>
    <title>My Web Page</title>
  </head>
  <body>
    <h1>Welcome to my web page</h1>
    <h2>Welcome to my web page</h2>
    <h3>Welcome to my web page</h3>
    <h4>Welcome to my web page</h4>
    <h5>Welcome to my web page</h5>
    <h6>Welcome to my web page</h6>
  </body>
</html>
```



