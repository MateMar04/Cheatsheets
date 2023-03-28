# JavaScript
JavaScript es un lenguaje interpretado o compilado just-in-time. Es conocido como un lenguaje de scripting para páginas web y usado en muchos entornos fuera del navegador. 
Es un lenguaje basado en programación de prototipos, con soporte para programación orientada a objetos.
Un lenguaje basado en prototipos utiliza herencia prototípica para la creación de nuevos objetos. Es una manera de crear nuevos objetos clonando objetos ya existentes en vez de emplear clases para definir la estructura del mismo.
El objeto es definido como una colección de pares key-value, en el que las keys son strings y los valores pueden ser cualquier tipo de dato, incluyendo otros objetos.
Cuando un objeto nuevo es creado, se inicializa clonando un objeto existente, modificándose para cumplir las necesidades del programa. El nuevo objeto hereda todas las propiedades y métodos de su prototipo y puede a su vez añadir nuevas propiedades y métodos o modificar los existentes.

Para más información, visite la documentación oficial de JavaScript: https://developer.mozilla.org/en-US/docs/Web/JavaScript

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

Los strings se comportan como listas, se puede acceder a cada carácter como si fuera un elemento de un ```Array```

También existen las secuencias de escape que sirven para representar determinados caracteres reservados en un string
```
\' ----> Comilla simple
\" ----> Comilla doble
\\ ----> Barra invertida
\n ----> Nueva linea
\r ----> Retorno de carro
\t ----> Tabulacion
\f ----> Salto de pagina
```



### Boolean
Es usado para representar valores lógicos (```true``` o ```false```)

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

Para acceder a las propiedades de un objeto se pueden usar dos métodos:

- La notación de punto:
```
console.log(myObj.prop1);
```

- Notación de corchetes:
```
console.log(myObj["prop1"]);
```


Las propiedades de estos también se pueden modificar de las dos formas anteriores

```
myObj.prop1 = 10;
myObj["prop2"] = "hello";
```

<hr>

JavaScript también tiene dos tipos de datos más que son técnicamente objetos:

### Array
Representa una lista ordenada de valores

```
var myArray = [1, 2, 3, 4, 5, 6, 7, 8, 9];
```

Los principales métodos de este objeto son:

```.push()```: sirve para agregar elementos a un ```Array``` al final del mismo.
```.pop()```: sirve para eliminar y retornar el último elemento de un ```Array```.
```.shift()```: sirve para eliminar y retornar el primer elemento de un ```Array```.
```.unshift()```: sirve para agregar elementos al inicio de un ```Array```.


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
Es un bloque de codigo que intenta (```try```) ejecutar código y si este“tira” una excepción, el ```catch```  lo “agarra”.
También existe el bloque ```finally``` que se ejecuta siempre, ya sea que se agarre la excepción o no.

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

Los loops son una manera fácil y rápida de hacer algo repetidamente.

### for
Un loop ```for``` se repite hasta que determinada condición se evalúe como ```false```
Cuando un ```for``` se ejecuta sucede lo siguiente:
1. Se ejecuta la expresión de inicialización, si es que hay alguna. Esta expresión inicializa generalmente contadores, pero la sintaxis permite una expresión de cualquier nivel de complejidad. Esta expresión también puede declarar variables.
2. La condición es evaluada, si es ```true``` el loop se ejecuta, de lo contrario se termina
3. Se ejecuta el codigo dentro del bloque ```for```
4. Si está presente se ejecuta la expresión ```afterthought```
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

También se ejecuta iterando determinada variable enumerable

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
Este loop se ejecuta hasta que determinada condición se evalúe como ```false```
la declaración siempre se ejecuta una vez antes de comprobar la condición, si esta se evalúa como ```true``` la declaración se vuelve a ejecutar hasta que la condición se evalúe como ```false```

```
do
  statement
while (condition);
```


### while
este loop se ejecuta si determinada condición se evalúa como ```true```

```
while (condition)
  statement
```

## Funciones
Las funciones en JavaScript son una parte fundamental del lenguaje, se usan para encapsular codigo reutilizable y realizar tareas específicas. Las funciones se pueden definir de varias maneras como declaraciones de función, expresiones de función, arrow functions, y Immediately Invoked Function Expressions (IIFEs).

### Declaración de función

```
function greet(name) {
  console.log('Hello, ' + name + '!');
}
```

La función llamada ```greet``` toma un parámetro llamado ```name```. Cuando esta es llamada mostrara un mensaje en consola con el parámetro ```name```

### Expresión de función

```
const greet = function(name) {
  console.log('Hello, ' + name + '!');
};
```

Esta función es similar a la anterior, pero se define usando una asignación a una variable. La variable llamada ```greet``` tiene una función anónima que toma ```name``` como parámetro.

### Arrow functions

```
const greet = (name) => console.log('Hello, ' + name + '!');
```

Este codigo es equivalente al anterior, nada más que esta usa la sintaxis de una ```arrow function```

### IIFEs

```
(function() {
  console.log('This code is self-contained and runs immediately!');
})();
```

Esta función es definida e inmediatamente llamada usando paréntesis al final de la declaración. Esto puede ser útil para crear variables privadas y funciones que no son accesibles desde él ```global scope```

<hr>

Las funciones también pueden “retornar” valores utilizando la keyword ```return```, y pueden tomar múltiples parámetros. Las funciones pueden ser también argumentos de otras funciones, también ser asignadas a variables y “pasarlas” como cualquier otro tipo de dato.



## Parámetros de funciones
Los parámetros se utilizan para pasarle valores a las funciones. Están definidos en la declaración de la función y pueden utilizarse como variables adentro de la función.
Hay dos tipos de sintaxis de parámetros:

### Parámetros Default

```
function addNumbers(num1, num2) {
  return num1 + num2;
}
```


Esta función tiene un parámetro con un valor predeterminado
```
function greet(name = 'friend') {
  console.log('Hello, ' + name + '!');
}
```


### Parámetros Rest
Este tipo de sintaxis sirve para tomar cualquier número de argumentos.

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

## Operadores
Expresión que se resuelve a un valor

### Asignación
Estos son los operadores de asignación más comunes:

```
x = f()      // Significa x = f()
x += f()     // Significa x = x + f()
x -= f()     // Significa x = x - f()
x *= f()     // Significa x = x * f()
x /= f()     // Significa x = x / f()
x %= f()     // Significa x = x % f()
x **= f()    // Significa x = x ** f()
```



### Operadores de Comparación
Un operador de comparación compara los operandos y devuelve un valor lógico basado si la comparación es ```true``` o ```false```


Teniendo en cuenta que:
```
const var1 = 3;
const var2 = 4;
```


#### Igual
El operador igual (```==```) devuelve ```true``` si los operandos son iguales 

Valores que devuelven ```true```:
```
3 == var1
"3" == var1
3 == '3'
```

#### No es Igual
El operador no igual (```!=```) devuelve ```true``` si los operandos no son iguales

Valores que devuelven ```true```:
```
var1 != 4  
var2 != "3"
```

#### Igual Estricto
El operador igual estricto (```===```) devuelve ```true``` si los operandos son iguales y del mismo tipo 

Valores que devuelven ```true```:
```
3 === var1
```

#### No es Igual Estricto
El operador no es igual estricto (```!==```) devuelve ```true``` si los operandos no son del mismo tipo o si son del mismo tipo pero distinto valor. 

Valores que devuelven ```true```:
```
var1 !== "3"  
3 !== '3'
```

#### Mayor
El operador mayor que (```>```) devuelve ```true``` si el operando de la izquierda es mayor que el de la derecha

Valores que devuelven ```true```:
```
var2 > var1  
"12" > 2
```

#### Mayor o igual
El operador mayor o igual que (```>=```) devuelve ```true``` si el operando de la izquierda es mayor o igual que el de la derecha

Valores que devuelven ```true```:
```
var2 >= var1  
var1 >= 3
```

#### Menor
El operador menor que (```<```) devuelve ```true``` si el operando de la izquierda es menor que el de la derecha

Valores que devuelven ```true```:
```
var1 < var2  
"2" < 12
```

#### Menor o Igual
El operador menor o igual que (```<=```) devuelve ```true``` si el operando de la izquierda es menor o igual que el de la derecha

Valores que devuelven ```true```:
```
var1 <= var2  
var2 <= 5
```



### Operadores Aritméticos
Los operadores toman valores numéricos y retornan un solo número. Los operadores aritméticos  estándar son la suma (```+```), resta (```-```), multiplicación (```*```) y división (```/```). Nota: la división por cero produce ```Infinity```.

#### Resto
Retorna el valor entero entre la división de dos operandos.
Ejemplo: 12 % 5 retorna 2.

#### Exponencial
Calcula la base elevado al exponente
Ejemplo: 2 ** 3 devuelve 8.

#### Incremento
Añade uno al operando.
Ejemplo: Si `x` es 3, entonces `++x` le añade uno y devuelve 4, pero `x++` devuelve 3 y luego le añade uno.

#### Decremento
Resta uno al operando
Ejemplo: Si `x` es 3, entonces `--x` le resta uno y devuelve 2, pero `x--` devuelve 3 y luego le resta uno.



### Operadores Lógicos
Estos operadores son comúnmente usados con valores booleanos

#### AND
```
const a1 = true && true; // t && t returns true
const a2 = true && false; // t && f returns false
const a3 = false && true; // f && t returns false
```

#### OR
```
const o1 = true || true; // t || t returns true
const o2 = false || true; // f || t returns true
const o3 = true || false; // t || f returns true
```

#### NOT
```
const n1 = !true; // !t returns false
const n2 = !false; // !f returns true
```



### String Operators

```
console.log("my " + "string"); // console logs the string "my string".
```

```
let mystring = "alpha";
mystring += "bet"; // evaluates to "alphabet" and assigns this value to mystring.
```

### Operadores Ternarios
Son operadores que toman tres operandos.

```
condition ? val1 : val2
```

Si la condición es ```true``` el valor es ```val1```, si es ```false``` es el valor ```val2```

```
const status = age >= 18 ? "adult" : "minor";
```