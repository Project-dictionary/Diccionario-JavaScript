# _**Funciones**_

Las funciones en `JavaScript` son un `objeto`, heredan sus propiedades de la clase padre `object.`Son bloques de código ejecutable, le podemos pasar parámetros y operar con ellos. Podemos modular nuestros programas y estructurar en bloque que realicen una tarea en concreto.

Las funciones al terminar su ejecución devuelven un valor que obtenemos con el parámetro `return`. Pueden llevar un nombre para ser invocadas más adelante o pueden no tener nombre y son llamadas`funciones anónimas`. Para evitar que el valor `undefined`  nos provoque errores y no poder controlarlo, podemos usar uno de los operadores `booleanos`.

`OR  -- ||` podemos usarlo para asignar un valor por default si no está definido.

`Let nombre = nombre || "Juan"`

_**Funciones Anidadas:**_ Pueden tener otras funciones dentro de ellas, ocasionando nuevos ámbitos para las `variables`definidas dentro de cada función. Para acceder a las funciones fuera de ellas tenemos que usar el operador doble paréntesis`()()`

**Arrow Functions: **Es la nueva forma de crear funciones que viene con las especificacines EcmaScript 5.

Su sintaxis es la siguiente:

```js
const crearUsuario = () =>{...}
```

En las Arrow Functions se omite la palabra function y se agrega un igual y un signo de menor después de los argumentos \(en forma de flecha\).

**Async/Await: **Async/Await es una nueva forma de manejar promesas en Javascript. Disponemos de dós métodos para trabajar con este tipo de funciones, async y await. Su uso es bastante sencillo, utilizaremos async para declarar las funciones asíncronas, y dentro de estas funciones utilizaremos await para suspender la ejecución hasta que la expresión que le sigue devuelva un valor. Veamos un ejemplo sencillo.

```js
async function asyncFunction () {
  const foo = await asyncOperation()
  return foo
}
```

**Callback: **Es la manera mas comun de controlar la asincronía en JavaScript, Es una funcion que se establece para realizar una llamada de vuelta en un momento del tiempo indeterminado, usada como parametro de funcion en algun evento o funcion que presente asincronía.

**Closures: **Los closures o funciones de cierre, son un patrón de diseño muy utilizado en`JavaScript.`Es una función que encapsula`variables`y definiciones`locales`, únicamente accesibles si son devueltas con el operador`return`, este patrón hace posible modularizar nuestro código.

```js
function foo(lenguaje) {
  const nombretrans = 'Babel'
  return function(){
    console.log(lenguaje+' es un lenguaje de programacion y '+nombretrans+' un transpilador poderoso')
  }
}

let bar = foo('Javascript')//foo devuelve una funcion que es almacenada en bar 
bar() //Debido a que cuando foo fue llamada su parametro 
      //era 'Javascript' entonces recuerda ese mismo valor
let baz = foo('JS')
baz()//Aca recuerda JS, Babel siempre se mantiene ya que es una constante en la funcion

//Lo importante es que una function interna recuerda 
//las variables de una funcion externa aun cuando la externa
//no se esta ejecutando.
```

**Generadores: **Es un objeto que sirve para decirle a`JavaScript`que nuestra función en un generador y se debe indicar con un asterisco de la siguiente forma:

```js
function* generador() { 
   yield 1;
   yield 2;
   yield 3;
}

var g = generador(); // "Generador { }"
```

Si creamos un generador debemos colocar la palabra clave`yield`la cual indica que cuando llamemos a la función después de la primera vez, esta iniciara en la linea después de`yield`. El generador convierte en objeto la función.

**Immediately Invoked Function Expressions \(IIFEs\): **Existe un tipo de funcion llamado IIFEs, usadas comunente patrones de diseño de software como module pattern , factory pattern etc... IIFEs tiene diferentes implementaciones

```js
// Classic
(function(){})();

// Crockford's favorite
(function(){}());

// Unary versions
+function(){}();

// Facebook version
!function(){}();

// Crazy version
!1%-+~function(){}();
```



