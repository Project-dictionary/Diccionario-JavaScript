![](https://cdn-images-1.medium.com/max/800/0*PQAXDSSDNR2rddzL.png)

# Currying {#currying}

###### Una técnica que utiliza una evaluación parcial {#una-técnica-que-utiliza-una-evaluación-parcial}

Currying se refiere al proceso de tomar una función con **n **argumentos y transformarla en **n **funciones que cada una toma un solo argumento.

_Esencialmente crea una cadena de funciones parcialmente aplicadas que eventualmente se resuelve con un valor._

Ejemplo:

```js
"use strict";

multiply = function multiply(n, m) { 
 return n * m;
};

 multiply(3, 4) === 12; // true

//Currying 

curryedMultiply = function curryedMultiply(n) {
  return function(m) {
    return multiply(n, m);
  };
};

//Uso

triple = curryedMultiply(3);
triple(4) === 12;  // true
```

El currying es bastante fácil de entender; Si vemos detenidamente hay una función que recibe un parámetro y una segunda función que usa el parámetro enviado previamente que retorna el resultado de una multiplicación entre los parámetros anteriormente enviados.

Si bien es difícil encontrar un caso de uso en la vida real, es una forma de simplificar el uso de las funciones.

###### ¿Es posible revertir el curring? {#¿es-posible-revertir-el-curring}

Por supuesto

```js
"use strict";

curryedMultiply = function curryedMultiply(n) {
 return function(m) { 
  return n * m;
  };
};

curryedMultiply(3)(4) === 12;  // true
multiply = function multiply(n, m) { 
 return curryedMultiply(n)(m);
};

multiply(3, 4) === 12; // true
```



