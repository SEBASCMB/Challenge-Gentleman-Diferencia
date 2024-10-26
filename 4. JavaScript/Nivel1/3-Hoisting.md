### ¿Qué es el Hoisting?

**Hoisting** es un comportamiento de JavaScript que mueve las declaraciones de variables y funciones a la parte superior de su contexto antes de que el código se ejecute. Imagina que cuando JavaScript empieza a leer tu código, primero sube todas las declaraciones de variables y funciones a la parte superior, como si estuviera organizando su espacio de trabajo.

### ¿Cómo Funciona?

1. **Variables**:
    
    - Cuando declaras una variable usando `var`, `let` o `const`, JavaScript "sube" la declaración (pero no la inicialización) a la parte superior.
    - Con `var`, la variable se inicializa con `undefined`.
    - Con `let` y `const`, el hoisting se aplica de manera diferente y no puedes usar la variable antes de su declaración.
2. **Funciones**:
    
    - Las declaraciones de funciones (por ejemplo, `function nombreFunc() {}`) son completamente hoisted, lo que significa que puedes llamarlas antes de su declaración en el código.

### Ejemplos de Hoisting

#### 1. Hoisting con `var`

```js
console.log(nombre); // Resultado: undefined
var nombre = "Juan";
console.log(nombre); // Resultado: "Juan"
```

**Explicación**:

- La declaración `var nombre` es hoisted, así que JavaScript lo mueve a la parte superior. Pero como no se ha inicializado aún, el primer `console.log` muestra `undefined`.

El código se comporta como si fuera:

```js
var nombre; // Declaración hoisted
console.log(nombre); // undefined
nombre = "Juan"; // Inicialización
console.log(nombre); // "Juan"
```

2. Hoisting con `let` y `const`

```js
console.log(edad); // Error: Cannot access 'edad' before initialization
let edad = 10;
```

**Explicación**:

- Con `let` y `const`, aunque la declaración es hoisted, no puedes acceder a la variable antes de su declaración debido a que se encuentra en un estado de "temporal dead zone" (zona muerta temporal) hasta que se inicializa.

#### 3. Hoisting con Funciones

```js
saludar(); // Resultado: "¡Hola!"

function saludar() {
    console.log("¡Hola!");
}
```

**Explicación**:

- Aquí, la función `saludar` se puede llamar antes de ser declarada porque la declaración de funciones es completamente hoisted.

### Resumen de Hoisting

- **Variables**:
    
    - Las declaraciones de variables (`var`) son hoisted y se inicializan como `undefined`.
    - Las declaraciones con `let` y `const` son hoisted pero no se pueden usar antes de su declaración.
- **Funciones**:
    
    - Las declaraciones de funciones son completamente hoisted y se pueden llamar en cualquier lugar antes de su declaración.

### Mejores Prácticas y Consejos

1. **Declara las Variables al Inicio**: Es buena práctica declarar todas las variables al inicio de su ámbito para evitar confusiones con el hoisting.
    
2. **Evita Usar Variables Antes de Declararlas**: Siempre inicializa las variables antes de usarlas para que no obtengas resultados inesperados (como `undefined` o errores).
    
3. **Usa Funciones de Expresión**: Si deseas evitar el hoisting con funciones, considera usar funciones de expresión (asignar una función a una variable), que no son hoisted.

```js
const saludar = function() {
    console.log("¡Hola!");
};
```


