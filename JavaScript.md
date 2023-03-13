# JavaScript
Javascript es un lenguaje interpretado o compilado just-in-time. Es conocido como un lenguaje de scripting para paginas web y usado en muchos entornos fuera del navegador. 
Es un lenguaje basado en programacion de prototipos, con soporte para programacion orientada a objetos.
Un lenguaje basado en prototipos usa herencia prototipica para la creacion de nuevos objetos. Es una manera de crear nuevos objetos clonando objetos ya existentes en vez de usar clases para definir la estructura del mismo.
El objeto es definido como una coleccion de pares key-value, en el que las keys son strings y los valores pueden ser cualquier tipo de dato, icluyendo otros objetos.
Cuando un objeto nuevo es creado se inicializa clonando un objeto existente, modificandose para cumplir las necesidades del programa. El nuevo objeto hereda todas las propiedades y metodos de su prototipo y puede a su vez añadir nuevas propiedades y metodos o modificar los existentes.

## Sintaxis
- En JavaScript el naming por convencion es camelCase. Cuando el nombre de una variable, funcion, objeto, etc tiene mas de una palabra se escribe la primera palabra en minuscula y las siguientes palabras se escriben con la primera letra mayuscula.

	``` var numerosPares = [2, 4, 6, 8, 10]; ```

- Las declaraciones suelen estar terminadas con un punto y coma (;).
  ```var nombre = "Mateo";```
- Es un lenguaje case-sensitive, lo que significa que ```miVariable``` y ```mivariable``` son distintas variables.
- Los comentarios en linea se agregan con ```//``` y los multilinea en medio de ```/**/```
- Las variables se pueden declarar sin un valor inicial.
  ```var nombre;```

## Tipos de Datos 

Estos son los principales tipos de datos en JavaScript

### Number
Es usado para representar numeros, incluyendo enteros y numeros de punto flotante

```
var myNumber = 10;
var myDecimalNumber = 1.2;
```

### String
Es usado para reprecentar texto, se encierra el texto entre comillas simples ('') o comillas dobles ("")

```
var myString = "Hello World!";
var myNoun = 'Dog';
```

### Boolean
Es usado para reprecentar valores logicos (true o false)

```
var myBoolean = true;
```

### Null
Es usado para representar valores nulos o valores vacios

```
var myNull = null;
```

### Undefined
Es usado para representar una variable a la que todavia no se le ha asignado un valor.

```
var x;
console.log(x); // Output: undefined
```

### Symbol
Es usado para representar un valor unico e inmutable que puede ser usado como identificador para las propiedades de objeto

```
const obj = {};

const sym = Symbol('foo');
obj[sym] = 'bar';

console.log(obj[sym]); // 'bar'

```

### Object
Es una coleccion de pares key-value donde cada key es un string o symbol y el value puede ser cualquier tipo de dato, incluyendo tambien otro objeto.

```
var myObj = {
  prop1: 'value1',
  prop2: 42,
  prop3: true,
  prop4: {
    nestedProp: 'nestedValue'
  }
};
```

<hr>

JavaScript tambien tiene dos tipos de datos mas que son tecnicamente objetos:

### Array
Representa una lista ordenada de valores

```
var myArray = [1, 2, 3, 4, 5, 6, 7, 8, 9];
```

### Function
Representa un bloque de codigo reutilizable cada vez que se llama con distintos argumentos. (Argumentos != Parametros)

```
function add(a, b) {
  return a + b;
};
```
