# JavaScript
JavaScript es un lenguaje interpretado o compilado just-in-time. Es conocido como un lenguaje de scripting para páginas web y usado en muchos entornos fuera del navegador. 
Es un lenguaje basado en programación de prototipos, con soporte para programación orientada a objetos.
Un lenguaje basado en prototipos utiliza herencia prototípica para la creación de nuevos objetos. Es una manera de crear nuevos objetos clonando objetos ya existentes en vez de emplear clases para definir la estructura del mismo.
El objeto es definido como una colección de pares key-value, en el que las keys son strings y los valores pueden ser cualquier tipo de dato, incluyendo otros objetos.
Cuando un objeto nuevo es creado, se inicializa clonando un objeto existente, modificándose para cumplir las necesidades del programa. El nuevo objeto hereda todas las propiedades y métodos de su prototipo y puede a su vez añadir nuevas propiedades y métodos o modificar los existentes.

## Sintaxis
- En JavaScript el naming por convención es camelCase. Cuando el nombre de una variable, función, objeto, etc. tiene más de una palabra, se escribe la primera palabra en minúscula y las siguientes palabras se escriben con la primera letra mayúscula.

	``` var numerosPares = [2, 4, 6, 8, 10]; ```

- Las declaraciones suelen estar terminadas con un punto y coma (;).
  ```var nombre = "Mateo";```
- Es un lenguaje "case-sensitive", lo que significa que ```miVariable``` y ```mivariable``` son distintas variables.
- Los comentarios en línea se agregan con ```//``` y los multilínea en medio de ```/**/```
- Las variables se pueden declarar sin un valor inicial.
  ```var nombre;```

## Tipos de Datos 

Estos son los principales tipos de datos en JavaScript

### Number
Es usado para representar números, incluyendo enteros y números de punto flotante

```
var myNumber = 10;
var myDecimalNumber = 1.2;
```

### String
Es usado para representar texto, se encierra el texto entre comillas simples ('') o comillas dobles ("")

```
var myString = "Hello World!";
var myNoun = 'Dog';
```

### Boolean
Es usado para representar valores lógicos (true o false)

```
var myBoolean = true;
```

### Null
Es usado para representar valores nulos o valores vacíos

```
var myNull = null;
```

### Undefined
Es usado para representar una variable a la que todavía no se le ha asignado un valor.

```
var x;
console.log(x); // Output: undefined
```

### Symbol
Es usado para representar un valor único e inmutable que puede ser usado como identificador para las propiedades de objeto

```
const obj = {};

const sym = Symbol('foo');
obj[sym] = 'bar';

console.log(obj[sym]); // 'bar'

```

### Object
Es una colección de pares key-value donde cada key es un string o symbol y el value puede ser cualquier tipo de dato, incluyendo también otro objeto.

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

JavaScript también tiene dos tipos de datos más que son técnicamente objetos:

### Array
Representa una lista ordenada de valores

```
var myArray = [1, 2, 3, 4, 5, 6, 7, 8, 9];
```

### Function
Representa un bloque de código reutilizable cada vez que se llama con distintos argumentos. (Argumentos != Parámetros)

```
function add(a, b) {
  return a + b;
};
```


## Variables

### Var
Es la forma original de declarar variables en JavaScript. Es una variable accesible desde la función definida, es decir, "function-scoped"

```
function example() {
  var x = 5;
  console.log(x);
}

example(); // Output: 5
console.log(x); // Throws a ReferenceError because x is not defined outside of the example function
```

Aun así, si definimos una variable dentro de un bloque, como por ejemplo un ```if``` la variable va a poder ser accesible desde las otras partes del código, ya que ```var``` es "function-scoped" y no "block-scoped" 

```
if (true) {
  var y = 10;
}

console.log(y); // Output: 10
```

### Let
Es una variable que puede ser accedida solo desde el bloque en el que fue declarada. Un bloque es la sección de código encerrado entre llaves ```{}```, tal como una función o un bucle.

```
function example() {
  let x = 1;
  if (true) {
    let x = 2;
    console.log(x); // 2
  }
  console.log(x); // 1
}
example();
```

### Const
Es utilizada para declarar una variable a las que no se les puede reasignar un valor una vez inicializadas. Al igual que ```let``` es una variable "block-scoped". Generalmente, estas variables se escriben en mayúsculas y las palabras están separadas por guiones bajos ```__``` para poder diferenciarlas de otras variables y para no intentar reasignarle valores a lo largo del código. 
Ej: ```MY_CONSTANT = 10;```

```
var x = 1; // function-scoped variable
let y = 2; // block-scoped variable
const Z = 3; // block-scoped constant

if (true) {
  var x = 4; // re-assigns the outer x variable
  let y = 5; // creates a new block-scoped y variable
  const Z = 6; // creates a new block-scoped z variable
  console.log(x, y, Z); // 4 5 6
}

console.log(x, y, Z); // 4 2 3 (x has been re-assigned, y and z are unchanged)
```

## Controladores de Flujo

### if...else

Se emplea para ejecutar un bloque de codigo segun si una condición lógica es ```true``` y si es ```false``` se usa el ```else```. También puede haber condiciones múltiples, en este caso se usa el ```else if``` y se pone la otra condición.

```
if (condition1) {
  statement1;
} else if (condition2) {
  statement2;
} else if (conditionN) {
  statementN;
} else {
  statementLast;
}
```

#### Falsy Values
Los siguientes valores se evalúan como ```false```
- false
- undefined
- null
- 0
- Nan
- empty string

Todos los otros valores se evalúan como ```true```

### switch
Permite evaluar una expresión e intentar coincidir la expresión a un valor de ```case```. Si la coincidencia no se encuentra, el programa ejecuta el código ```default```

- El programa busca una ```case``` que coincida con el valor de la expresión ejecutando el código asociado al mismo.
- Si no encuentra una coincidencia se ejecuta el caso ```default``` si existe, si no el programa continúa ejecutándose normalmente.

```
switch (fruitType) {
  case "Oranges":
    console.log("Oranges are $0.59 a pound.");
    break;
  case "Apples":
    console.log("Apples are $0.32 a pound.");
    break;
  case "Bananas":
    console.log("Bananas are $0.48 a pound.");
    break;
  case "Cherries":
    console.log("Cherries are $3.00 a pound.");
    break;
  case "Mangoes":
    console.log("Mangoes are $0.56 a pound.");
    break;
  case "Papayas":
    console.log("Mangoes and papayas are $2.79 a pound.");
    break;
  default:
    console.log(`Sorry, we are out of ${fruitType}.`);
}
console.log("Is there anything else you'd like?");
```

### throw
Se usa para “tirar” una excepción

```
throw "Error2"; // String type
throw 42; // Number type
throw true; // Boolean type
throw {
  toString() {
    return "I'm an object!";
  },
};
```

### try...catch
Es un bloque de codigo que intenta (```try```) ejecutar uncódigoo y si este“tira”" una excepción el ```catch```  lo "agarra".
Tambien existe el bloque ```finally``` que se ejecuta siempre, ya sea que se agarre la excepcion o no.

```
function f() {
  try {
    console.log(0);
    throw "bogus";
  } catch (e) {
    console.log(1);
    // This return statement is suspended
    // until finally block has completed
    return true;
    console.log(2); // not reachable
  } finally {
    console.log(3);
    return false; // overwrites the previous "return"
    console.log(4); // not reachable
  }
  // "return false" is executed now
  console.log(5); // not reachable
}
console.log(f()); // 0, 1, 3, false
```

## Loops

Los loops son una manera facil y rapida de hacer algo repetidamente.

### for
Un loop ```for``` se repite hasta que determinada condicion se evalue como ```false```
Cuando un ```for``` se ejecuta sucede lo siguiente:
1. Se ejecuta la expresion de inicializacion, si es que hay alguna. Esta expresion inicializa generalmente contadores, pero la sintaxis permite una expresion de cualquier nivel de complejidad. esta expresion tambien puede declarar variables.
2. La condicion es evaluada, si es ```true``` el loop se ejecuta, de lo contrario se termina
3. Se ejecuta el codigo dentro del bloque ```for```
4. Si esta presente se ejecuta la expresion ```afterthought```
5. Se vuelve al punto 2

```
for (initialization; condition; afterthought)
  statement

```

### for..in
Se ejecuta iterando determinada variable enumerable

```
for (variable in object)
  statement
```

Este for itera sobre las propiedades de un objeto

```
const person = { name: 'John', age: 30, address: '123 Main St' };

for (let prop in person) {
  console.log(prop + ': ' + person[prop]);
}

OUTPUT:
name: John
age: 30
address: 123 Main St
```

### for...of

Tambien e ejecuta iterando determinada variable enumerable

```
for (variable of object)
  statement
```

Este ```for``` itera sobre valor

```
const arr = [1, 2, 3];

for (let value of arr) {
  console.log(value);
}

OUTPUT:
1
2
3

```

### do...while
Este loop se ejecuta hasta que determinada condicion se evalue como ```false```
la declaracion siempre se ejecuta una vez antes de comprobar la condicion, si esta se evalua como ```true``` la declaracion se vuelve a ejecutar hasta que la condicion se evalue como ```false```

```
do
  statement
while (condition);
```


### while
este loop se ejecita si determinada condicion se evalua como ```true```

```
while (condition)
  statement
```

## Funciones
Las funciones en JavaScript son una parte fundamental del lenguaje, se usan para encapsular codigo reutilizable y realizar tareas especificas. Las funciones se pueden definir de varias maneras como declaraciones de funcion, expresiones de funcion, arrow functions, y Immediately Invoked Function Expressions (IIFEs).

### declaracion de funcion

```
function greet(name) {
  console.log('Hello, ' + name + '!');
}
```

La funcion llamada ```greet``` toma un parametro llamado ```name```. Cuando esta es llamada mostrara un mensaje en consola con el parametro ```name```

### expresion de funcion

```
const greet = function(name) {
  console.log('Hello, ' + name + '!');
};
```

Esta funcion es similar a la anterior, pero se define usando una asignacion a una variable. La variable llamada ```greet``` tiene una funcion anonima que toma ```name``` como parametro.

### Arrow functions

```
const greet = (name) => console.log('Hello, ' + name + '!');
```

Este codigo es equivalente al anterior, nada mas que esta usa la sintaxis de una ```arrow function```

### IIFEs

```
(function() {
  console.log('This code is self-contained and runs immediately!');
})();
```

Esta funcion es definida e inmediatamente llamada usando parentesis al final de la declaracion. Esto puede ser util para crear variables privadas y funciones que no son accesibles desde el ```global scope```

<hr>

Las funcoines tambien pueden "retornar" valores usando la keyword ```return```, y pueden tomar multiples parametros. Las funciones pueden ser tambien argumentos de otras funciones, tambien ser asignadas a variables y "pasarlas" como cualquier otro tipo de dato.



## Parametros de funciones
Los parametros se usan para pasarle valores a las funciones. Estan definidos en la declaracion de la funcion y pueden usarse como variables adentro de la funcion.
Hay dos tipos de sintaxis de parametros:

### Parametros Default

```
function addNumbers(num1, num2) {
  return num1 + num2;
}
```


Esta funcion tiene un parametro con un valor predeterminado
```
function greet(name = 'friend') {
  console.log('Hello, ' + name + '!');
}
```


### Parametros Rest
Este tipo de sintaxis sirve para tomar cualquier numero de argumentos.

```
function sumNumbers(...nums) {
  let sum = 0;
  for (let num of nums) {
    sum += num;
  }
  return sum;
}

const result1 = sumNumbers(1, 2, 3);
const result2 = sumNumbers(4, 5, 6, 7, 8);
console.log(result1); // output: 6
console.log(result2); // output: 30
```