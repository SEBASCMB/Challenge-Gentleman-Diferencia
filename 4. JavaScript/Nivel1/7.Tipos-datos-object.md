### Tipos de Datos en JavaScript

En JavaScript, los tipos de datos se dividen en dos categorías principales: **tipos primitivos** y **objetos**. Los tipos primitivos incluyen `string`, `number`, `boolean`, `undefined`, `null`, `bigint`, y `symbol`. Los objetos, por otro lado, son más complejos y permiten almacenar colecciones de datos y funcionalidades.

### Objetos

#### 1. Object (Objeto)

- **Descripción**: Un objeto es una colección de propiedades, donde cada propiedad tiene una clave (nombre) y un valor. Los valores pueden ser de cualquier tipo, incluidos otros objetos, arreglos y funciones (que se llaman métodos cuando son parte de un objeto).
- **Creación de Objetos**: Puedes crear objetos usando dos métodos comunes:
    - **Literal de objeto**: Usando llaves (`{}`).
    - **Constructor Object**: Usando la palabra clave `new Object()`.

#### Ejemplo:

```js
// Creación de un objeto utilizando la sintaxis literal
let coche = {
    marca: "Toyota",
    modelo: "Corolla",
    anio: 2020,
    mostrarInfo: function() {
        console.log(`Coche: ${this.marca} ${this.modelo}, Año: ${this.anio}`);
    }
};

// Accediendo a las propiedades del objeto
console.log(coche.marca); // Resultado: "Toyota"
console.log(coche["modelo"]); // Resultado: "Corolla"

// Llamando al método del objeto
coche.mostrarInfo(); // Resultado: "Coche: Toyota Corolla, Año: 2020"
```

#### 2. typeof Operator (Operador typeof)

- **Descripción**: El operador `typeof` se usa para determinar el tipo de un valor. Devuelve una cadena que representa el tipo del operando.

#### Ejemplo:

```js
let numero = 100;
let texto = "Hola";
let objeto = { nombre: "Ana" };
let arreglo = [1, 2, 3];
let indefinido;

console.log(typeof numero); // Resultado: "number"
console.log(typeof texto); // Resultado: "string"
console.log(typeof objeto); // Resultado: "object"
console.log(typeof arreglo); // Resultado: "object" (los arreglos son considerados objetos)
console.log(typeof indefinido); // Resultado: "undefined"
```

### 3. Built-in Objects (Objetos Integrados)

JavaScript incluye varios **objetos integrados** que proporcionan funcionalidades y métodos útiles. Algunos ejemplos son:

- **Array**: Para almacenar listas de elementos.
- **Date**: Para trabajar con fechas y horas.
- **Math**: Para realizar cálculos matemáticos.
- **RegExp**: Para trabajar con expresiones regulares.

#### Ejemplo de Array:

```js
let frutas = ["manzana", "banana", "naranja"];
console.log(frutas.length); // Resultado: 3
console.log(frutas[0]); // Resultado: "manzana"
```

Ejemplo de Math:

```js
let maximo = Math.max(10, 20, 5); // Retorna el número más grande
console.log(maximo); // Resultado: 20
```

### 4. JSON (JavaScript Object Notation)

- **Descripción**: JSON es un formato ligero de intercambio de datos. Es fácil de leer y escribir para los humanos y fácil de analizar y generar para las máquinas. Se utiliza comúnmente para enviar datos entre un servidor y un cliente web.

#### Ejemplo de JSON:

Puedes convertir un objeto JavaScript a JSON y viceversa.

```js
let persona = {
    nombre: "Carlos",
    edad: 30,
    ciudad: "Medellín"
};

// Convertir objeto a JSON
let jsonPersona = JSON.stringify(persona);
console.log(jsonPersona); // Resultado: '{"nombre":"Carlos","edad":30,"ciudad":"Medellín"}'

// Convertir JSON a objeto
let objetoPersona = JSON.parse(jsonPersona);
console.log(objetoPersona.nombre); // Resultado: "Carlos"
```

### Resumen de Objetos en JavaScript

|**Concepto**|**Descripción**|**Ejemplo**|
|---|---|---|
|**Object**|Colección de propiedades (clave-valor).|`let obj = { key: "value" };`|
|**typeof Operator**|Obtiene el tipo de una variable o expresión.|`console.log(typeof obj); // "object"`|
|**Built-in Objects**|Objetos proporcionados por JavaScript (Array, Date, etc.).|`let arr = [1, 2, 3];`|
|**JSON**|Formato de texto para el intercambio de datos.|`JSON.stringify(obj); // Convierte a JSON`|

### Mejores Prácticas y Consejos

1. **Usa objetos para agrupar datos**: Organiza propiedades y métodos relacionados en objetos para que tu código sea más claro y mantenible.
    
2. **Utiliza JSON para intercambiar datos**: Al trabajar con APIs o almacenamiento de datos, JSON es un formato estándar y versátil.
    
3. **Evita la modificación directa de objetos**: Cuando necesites actualizar un objeto, considera usar métodos como `Object.assign()` o el operador de propagación (`...`) para crear una copia en lugar de modificar el original.
    
4. **Usa `const` para objetos inmutables**: Aunque puedes modificar las propiedades de un objeto declarado con `const`, impide que la variable sea reasignada accidentalmente.
