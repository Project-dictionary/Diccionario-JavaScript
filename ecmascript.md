# **Novedades de ECMAScript 2105 \(ES6\)** {#novedades-de-ecmascript-2105-es6}

### ECMAScript {#ecmascript}

ECMAScript se refiere a las nuevas características del estándar ECMA-262 conocidos como JavaScript, introducido después de ECMAScript 2015. Las nuevas versiones de las especificaciones ECMAScript se liberan anualmente, ES2016 será liberado y el ES2017 es el proyecto actual ECMAScript.

### Definición de variables {#definición-de-variables}

Para solventar las deficiencias de las variables declaradas con \_var, \_hay dos nuevas palabras reservadas: \_let \_para declarar variables que cambian de valor y \_const \_para constantes. También se pueden declarar símbolos que son identificadores de tipos únicos e inmutables.

El problema de las variables declaradas con \_var \_está en que tienen ámbito de función con \_let \_no existe hasta que es declarada. Las variables con \_var \_son declaradas al principio del ámbito de la función o en el ámbito global.

### Interpolación de variables en cadenas {#interpolación-de-variables-en-cadenas}

La interpolación de variables en cadena facilita la construcción de strings y hace el código más legible. Los strings se hacen con las comillas invertidas o francesas \( \` \)

    const now = newDate(Date.now());

    const message = `¡Hola ${now.getFullYear()}!`;

    console.log(message);  // ¡Hola 2016!

### Desestructuración {#desestructuración}

Se ha incorporado la asignación desestructurada pudiendo hacer cosas como las siguientes en las asignaciones y en las llamadas a las funciones:

    // Arrays

    const array = [1, 2];

    const [a, b] = array;

    console.log(`${a}, ${b}`); // 1, 2

    // Objects

    constobject = { name: 'Jhon', age: 30};

    const {name, age} = object;

      console.log(`${name}, ${age}`);  // Jhon, 30 

    // Functions

    function whois({displayName: displayName, fullName: { firstName: name }}){

      console.log(`${displayName} is ${name}`);

    }


    var user = {

      id: 42,

      displayName: "jdoe",

      fullName: {

          firstName: "Jhon",

          lastName: "Doe"
        }
    };

    whois(user);  // Jhon Doe is jdoe

### Operador _spread_ {#operador-spread}

El operador spread permite a una expresión sea expandida en lugares donde se esperan múltiples argumentos como en llamadas a funciones, múltiples elementos para literales de \_arrays \_o múltiples variables para asignación desestructurada.

    const array1 = [1, 2, 3];

    const array2 = [...array1, 4, 5, 6]

      console.log(array2);  // Array [ 1, 2, 3, 4, 5, 6 ]

    function func(x, y, z) {

      console.log(`${x}, ${y}, ${z}`);

    }

    func(...array1);  // 1, 2, 3

### Clases {#bucles-con-in-y-of}

Anteriormente en JavaScript ya se podían definir clases haciendo uso de la propiedad p_rototype \_aunque su sintaxis ahora se ha simplificado y hecho más parecida a otros lenguajes además de definir propiedades con su método \_getter \_y \_setter._

```
class Vehiculo{

  constructor() {
  
    this._marca = 'Seat';
    
    this._color = 'rojo';
    
    this._kilometros = 100;
  
  }
  
  get color() {
    
    return this._color;
  }
  
  set color(c) {
  
    this._color = c;
    
  }
}


class Coche extends Vehiculo{

  get kilometros() {
    
  return this._kilometros;
  
}
  set kilometros(k) {
    
  this._kilometros = k;
  
  }
}


const coche = newCoche();

console.log(coche.color); // rojo
```

### y otros features como: {#y-otros-features-como}

* Objetos map y set
* Callback y promise
* Generadores
* Eventos

Para más información sobre ESMAScropt 6, vea el siguiente enlace: [http://es6-features.org/](http://es6-features.org/)

