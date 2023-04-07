# React
React es una biblioteca de JavaScript de código abierto para construir interfaces de usuario. Fue desarrollada por Facebook y ahora es mantenida por Facebook y una comunidad de desarrolladores individuales y empresas. React permite a los desarrolladores construir componentes de UI reutilizables y gestionar el estado de la aplicación de manera declarativa.

Una de las características clave de React es su capacidad para actualizar eficientemente la interfaz de usuario cuando cambia el estado de la aplicación. En lugar de manipular manualmente el DOM, React utiliza un DOM virtual para comparar los estados anterior y actual de la aplicación y luego actualizar solo las partes necesarias del DOM real de manera eficiente.

Se puede utilizar para construir una amplia variedad de aplicaciones, incluyendo aplicaciones de una sola página, aplicaciones móviles e incluso aplicaciones de renderización del lado del servidor.

React está escrito en JavaScript y se puede utilizar con una variedad de otras tecnologías front-end, como HTML, CSS y varios frameworks de estilo. Es ampliamente adoptado por desarrolladores y empresas de todo el mundo y tiene un gran ecosistema de bibliotecas y herramientas de terceros para ayudar a los desarrolladores a construir aplicaciones complejas de manera rápida y eficiente.

## Ventajas
1. **Reutilización de componentes:** React permite la creación de componentes reutilizables, lo que simplifica el proceso de desarrollo y mantenimiento de una aplicación.
2. **Virtual DOM:** React utiliza un DOM virtual para actualizar la interfaz de usuario de manera eficiente, lo que mejora el rendimiento de la aplicación y proporciona una mejor experiencia de usuario.
3. **Declarativo:** React se enfoca en la declaración de cómo debe verse la interfaz de usuario en lugar de cómo lograrlo, lo que hace que el código sea más legible y fácil de entender.
4. **Gran comunidad de desarrolladores:** React tiene una gran comunidad de desarrolladores que contribuyen al desarrollo de bibliotecas y herramientas, lo que hace que sea fácil encontrar soluciones y resolver problemas.
5. **Soporte de React Native:** React se integra bien con React Native, lo que permite a los desarrolladores crear aplicaciones móviles nativas para iOS y Android utilizando el mismo código base que su aplicación web.
6. **Modularidad:** React fomenta la modularidad del código, lo que permite que se pueda dividir en componentes más pequeños y fáciles de mantener.

Para más información, visite la documentación oficial de React: https://react.dev/ o la documentación desactualizada que también puede tener información útil https://legacy.reactjs.org/docs/getting-started.html

## Conceptos Básicos de React

### DOM 
 Significa Document Object Model y es una representación estructurada y jerárquica de un documento HTML o XML en forma de árbol. En otras palabras, el DOM es una interfaz de programación de aplicaciones (API) que permite a los desarrolladores acceder y manipular elementos HTML y XML en una página web. 
 Se compone de objetos que representan cada elemento del documento, se organizan en una jerarquía de padre-hijo, que refleja la estructura del documento.
 La manipulación del DOM permite a los desarrolladores cambiar el contenido y la apariencia de una página web dinámicamente, en respuesta a la interacción del usuario o cambios en los datos de la aplicación.
 Es importante tener en cuenta que la manipulación excesiva del DOM puede tener un impacto negativo en el rendimiento de una página web. La manipulación excesiva del DOM puede ser costosa en términos de memoria y tiempo de procesamiento, lo que puede hacer que una página web sea lenta o inestable. Por esta razón, las bibliotecas y frameworks como React utilizan técnicas como el Virtual DOM para minimizar la cantidad de manipulación del DOM y mejorar el rendimiento de la aplicación.

### Virtual DOM
Es una técnica utilizada en bibliotecas y frameworks de JavaScript como React para mejorar el rendimiento de las aplicaciones web. En lugar de actualizar directamente el DOM real (Document Object Model) cada vez que cambia el estado de la aplicación, React utiliza una copia en memoria del DOM, conocida como el Virtual DOM, para realizar estas actualizaciones.
El Virtual DOM es una representación en memoria del DOM real de una página web. Cuando se produce un cambio en el estado de la aplicación, React compara la versión anterior del Virtual DOM con la nueva versión y determina cuáles son los cambios que deben realizarse en el DOM real. Luego, actualiza solo los elementos que han cambiado, en lugar de actualizar la página completa.
Esta técnica permite que las actualizaciones del DOM sean más eficientes y rápidas, ya que solo se actualizan los elementos que han cambiado. Además, el Virtual DOM permite que los desarrolladores escriban código más limpio y simple, ya que no tienen que preocuparse por actualizar manualmente el DOM. En cambio, pueden centrarse en la lógica de la aplicación.
Es importante tener en cuenta que el Virtual DOM no es una tecnología en sí misma, sino una técnica utilizada en bibliotecas y frameworks

### Componente
Un componente de React puede ser una clase componente o un componente funcional. Los componentes de clase se definen utilizando la sintaxis de clase ES6 y deben heredar de la clase Componente de React.

#### Funcional
Un componente funcional de React es una forma de definir un componente utilizando una función en lugar de una clase. Los componentes funcionales son más simples y más concisos que los componentes de clase, y pueden ser una buena opción si el componente no necesita tener estado o métodos de ciclo de vida.

Para definir un componente funcional, se debe declarar una función que tome las props como argumento y devuelva el marcado JSX. Por ejemplo, un componente funcional que renderice un botón puede ser definido de la siguiente manera:

``` jsx
import React from 'react';

function Button(props) {
  return (
    <button onClick={props.onClick}>
      {props.label}
    </button>
  );
}
```

En este ejemplo, el componente `Button` es una función que toma las props como argumento y devuelve un elemento `button` que muestra el texto de la etiqueta y tiene un manejador `onClick`.

Los componentes funcionales de React también pueden aceptar props opcionales mediante el uso de valores predeterminados. Por ejemplo, si el componente `Button` debe tener un color de fondo predeterminado, se puede definir el prop opcional de la siguiente manera:

``` jsx
import React from 'react';

function Button(props) {
  const backgroundColor = props.backgroundColor || 'gray';
  return (
    <button onClick={props.onClick} style={{ backgroundColor }}>
      {props.label}
    </button>
  );
}
```

En este ejemplo, el componente `Button` utiliza el operador OR (`||`) para proporcionar un valor predeterminado al prop `backgroundColor` si no se proporciona uno. Luego, el color de fondo se establece en el elemento `button` utilizando la sintaxis de estilo de objeto de JavaScript.

#### De Clase
Un componente de clase de React es una forma de definir un componente utilizando una clase en lugar de una función. Los componentes de clase son más poderosos que los componentes funcionales porque pueden tener un estado interno y métodos de ciclo de vida, lo que les permite manejar mejor la interacción del usuario y actualizar dinámicamente la interfaz de usuario.

Para definir un componente de clase, se debe declarar una clase que herede de la clase base `React.Component` y tenga un método `render()` que devuelva el marcado JSX. Por ejemplo, un componente de clase que renderice un botón puede ser definido de la siguiente manera:

``` jsx
import React from 'react';

class Button extends React.Component {
  render() {
    return (
      <button onClick={this.props.onClick}>
        {this.props.label}
      </button>
    );
  }
}
```

En este ejemplo, el componente `Button` es una clase que hereda de `React.Component`. Tiene un método `render()` que devuelve un elemento `button` que muestra el texto de la etiqueta y tiene un manejador `onClick`. Los props se acceden a través de `this.props` en lugar de ser pasados como argumentos a una función.

Los componentes de clase de React también pueden tener un estado interno que se puede actualizar mediante la llamada al método `setState()`. Por ejemplo, si el componente `Button` debe tener un contador interno que se actualiza cuando se hace clic en el botón, se puede definir el estado y un método `handleClick()` que lo actualice:

``` jsx
import React from 'react';


class Button extends React.Component {
  constructor(props) {
    super(props);
    this.state = { count: 0 };
    this.handleClick = this.handleClick.bind(this);
  }

  handleClick() {
    this.setState({ count: this.state.count + 1 });
  }

  render() {
    return (
      <button onClick={this.handleClick}>
        Clicked {this.state.count} times
      </button>
    );
  }
}
```

En este ejemplo, el componente `Button` tiene un estado interno `count` que se inicializa en `0` en el constructor. El método `handleClick()` se llama cuando se hace clic en el botón y actualiza el estado interno mediante la llamada al método `setState()`. El método `handleClick()` también está vinculado al componente utilizando `bind()` en el constructor para garantizar que `this` se refiere al componente correcto.

En general, los componentes de clase de React son más adecuados para componentes que necesitan tener un estado interno o métodos de ciclo de vida complejos. Sin embargo, debido a que los componentes funcionales son más simples y más concisos, son una buena opción para componentes más simples que no necesitan estas características.

### Hooks
React Hooks es una característica que permite usar estado y otras características de React sin escribir un componente de clase. Con Hooks, se puede agregar estado y otras características.

- ```useState:``` Esto te permite agregar estado a tu componente de función. Puedes usarlo para almacenar y actualizar variables.
- ```useEffect:``` Esto te permite realizar efectos secundarios, como buscar datos o actualizar el DOM, en tu componente de función. Puedes usarlo para realizar acciones después de que se haya renderizado el componente.
- ```useContext:``` Esto te permite acceder al contexto en tu componente de función. Puedes usarlo para compartir datos entre componentes sin tener que pasar props hacia abajo en cada nivel de la jerarquía de componentes.
- ```useReducer:``` Esto te permite administrar el estado con una función reductora. Puedes usarlo para actualizar el estado en función del estado anterior, similar a cómo lo harías con Redux.
- ```useCallback:``` Esto te permite memorizar una función, lo que puede mejorar el rendimiento al evitar re-renderizaciones innecesarias de tu componente.
- ```useMemo:``` Esto te permite memorizar un valor, lo que puede mejorar el rendimiento al evitar recalculaciones innecesarias de un valor. 

Los Hooks proporciona una forma más concisa y legible de administrar el estado y realizar efectos secundarios en tus componentes de React.

### Props
React props (abreviatura de “propiedades”) son una forma de pasar datos desde un componente “padre” a un componente “hijo” en una aplicación de React.
Son valores inmutables que se pasan como argumentos a un componente de React en su invocación. Los componentes de React pueden aceptar cualquier cantidad de props. Puedes pasar cualquier tipo de dato como una prop, incluyendo cadenas de texto, números, booleanos, objetos y funciones.

``` jsx
function Greeting(props) {
  return <h1>Hello, {props.name}!</h1>;
}
```

### Estado
Un estado (state) es un objeto JavaScript que contiene información que puede cambiar durante la vida útil de un componente. Cada componente puede tener su propio estado, que se puede inicializar en su método constructor y luego actualizar con el método `setState()`.

El estado de un componente es privado y no se puede acceder o modificar directamente desde fuera del componente. En su lugar, se utiliza el método `setState()` para actualizar el estado. `setState()` es una función asíncrona que actualiza el estado del componente y provoca una nueva renderización del componente y de sus descendientes.

El estado es útil para almacenar datos que pueden cambiar durante la vida útil de un componente, como un campo de entrada de texto, un cuadro de selección o un contador. Por ejemplo, si tienes un componente `Counter` que muestra un número y un botón para incrementar ese número, puedes mantener el valor del número en el estado del componente.

``` jsx
import React, { Component } from 'react';

class Counter extends Component {
  constructor(props) {
    super(props);
    this.state = { count: 0 };
  }

  handleClick = () => {
    this.setState(prevState => ({ count: prevState.count + 1 }));
  }

  render() {
    return (
      <div>
        <p>Count: {this.state.count}</p>
        <button onClick={this.handleClick}>Increment</button>
      </div>
    );
  }
}
```

En este ejemplo, el componente `Counter` tiene un estado inicial de `{ count: 0 }`. Cuando el botón es clickeado, el método `handleClick` actualiza el estado con el método `setState()`, que utiliza la función `prevState` para actualizar el valor actual del estado. Finalmente, el valor del estado se muestra en el componente utilizando la sintaxis de llaves `{}`.

### Event Listeners
En React, los eventos (event listeners) son funciones que se activan cuando un usuario interactúa con un elemento en la interfaz de usuario. Los eventos en React son similares a los eventos en JavaScript, pero se manejan de manera ligeramente diferente.

En React, los eventos se nombran en camelCase en lugar de usar el nombre del evento en minúsculas. Por ejemplo, el evento onclick se llama onClick en React. Los eventos se agregan como atributos a los elementos de la interfaz de usuario, y el valor del atributo es la función que se ejecuta cuando se activa el evento.

``` jsx
import React, { Component } from 'react';

class Button extends Component {
  handleClick = () => {
    console.log('Button was clicked');
  }

  render() {
    return (
      <button onClick={this.handleClick}>Click me</button>
    );
  }
}
```

En este ejemplo, se ha creado un componente `Button` que muestra un botón en la interfaz de usuario. El botón tiene un evento `onClick` que se activa cuando el usuario hace clic en el botón. Cuando se activa el evento, se ejecuta la función `handleClick`, que simplemente imprime un mensaje en la consola.

En React, también puedes pasar argumentos a una función manejadora de eventos utilizando una función de flecha. Por ejemplo, si quieres pasar un valor a la función `handleClick` cuando se activa el evento, puedes hacerlo de la siguiente manera:

``` jsx
import React, { Component } from 'react';

class Button extends Component {
  handleClick = (value) => {
    console.log(`Button was clicked with value ${value}`);
  }

  render() {
    return (
      <button onClick={() => this.handleClick('foo')}>Click me</button>
    );
  }
}
```

En este ejemplo, se ha pasado el valor `'foo'` a la función `handleClick` utilizando una función de flecha en lugar de la función directamente.

### Elementos vs Componentes
Los elementos son los menores "bloques de construcción" en React, mientras que un componente es codigo reutilizable que encapsula uno o varios elementos y su comportamiento. 

Elemento:
``` jsx
const element = <h1>Hello, world!</h1>;
```

Componente:
``` jsx
import React from 'react';

function Greeting(props) {
  return <h1>Hello, {props.name}!</h1>;
}
```

### Crear un proyecto de React
1.  Instala Node.js y npm (Node Package Manager) en tu ordenador si aún no lo has hecho.
2.  Abre una ventana de terminal o de símbolo del sistema.
3.  Instala el paquete `create-react-app` globalmente ejecutando el siguiente comando: `npm install -g create-react-app`. Este paquete proporciona una manera conveniente de crear un nuevo proyecto de React con una configuración básica.
4.  Crea un nuevo proyecto de React ejecutando `create-react-app <nombre-del-proyecto>`. Reemplaza `<nombre-del-proyecto>` con el nombre que quieras darle a tu proyecto.
5.  Una vez que se haya creado el proyecto, navega hasta el directorio del proyecto ejecutando `cd <nombre-del-proyecto>`.
6.  Inicia el servidor de desarrollo ejecutando `npm start`. Esto abrirá una nueva pestaña en tu navegador por defecto que muestra tu aplicación de React.
7.  Puedes empezar a modificar el código en la carpeta `src` para construir tu aplicación de React.


### Estructura de un Proyecto React
La estructura de un proyecto de React puede variar en función de las necesidades del proyecto y las preferencias del desarrollador, pero aquí te muestro una estructura comúnmente utilizada:

```
my-react-app/
├── node_modules/
├── public/
│   ├── index.html
│   └── favicon.ico
├── src/
│   ├── index.js
│   ├── App.js
│   ├── components/
│   │   ├── Header.js
│   │   ├── Footer.js
│   │   └── ...
│   ├── pages/
│   │   ├── Home.js
│   │   ├── About.js
│   │   └── ...
│   ├── assets/
│   │   ├── images/
│   │   ├── styles/
│   │   └── ...
│   └── ...
├── package.json
├── package-lock.json
└── README.md
```

-   `node_modules/` es el directorio que contiene las dependencias de Node.js que necesita tu proyecto.
-   `public/` es el directorio que contiene archivos estáticos que se servirán a través del servidor. El archivo `index.html` es el punto de entrada de la aplicación y el `favicon.ico` es el icono que se muestra en la pestaña del navegador.
-   `src/` es el directorio que contiene el código fuente de la aplicación. `index.js` es el punto de entrada de la aplicación y es donde se renderiza el componente principal. `App.js` es el componente principal que se renderiza en el `index.js`. `components/` es el directorio que contiene los componentes reutilizables que se utilizan en la aplicación. `pages/` es el directorio que contiene los componentes que representan las diferentes páginas de la aplicación. `assets/` es el directorio que contiene los archivos estáticos como imágenes y estilos CSS.
-   `package.json` es el archivo que contiene la información sobre las dependencias del proyecto, scripts y otra información útil para el proyecto.
-   `package-lock.json` es el archivo que se genera automáticamente y contiene información sobre las versiones exactas de las dependencias instaladas.
-   `README.md` es el archivo que contiene información sobre el proyecto.