## ¿Qué es HTML?

HTML es un *lenguaje de marcado*, lo que significa que usamos "etiquetas" para decirle al navegador cómo mostrar el contenido. Estas etiquetas están rodeadas por símbolos `<` y `>` y vienen en *pares*. Por ejemplo:

```html
<p>Hola, soy un párrafo.</p>
```

Aquí, `<p>` es una etiqueta que le dice al navegador: "Esto es un párrafo". La etiqueta de cierre es `</p>`, que le dice al navegador que **termine** el párrafo

### Estructura básica de una página HTML

Todas las páginas HTML siguen una estructura básica. Piensa en esto como la base de una página web:

```html
<!DOCTYPE html>
<html lang="es">
   <head>
     <meta charset="UTF-8">
     <meta name="viewport" content="width=device-width, initial-scale=1.0">
     <title> Mi primera página</title>
   </head>
   <body>
     <h1>Hola</h1>
     <p>Esta es mi primera página web</p>
   </body>
</html>
```

## ¿Que significa cada parte?

- **`<!DOCTYPE html>`**: Le dice al navegador que estamos usando **HTML5**, la versión más moderna de HTML.
- **`<html lang="es">`**: Esta es la etiqueta principal que envuelve todo el contenido de la página. Le dice al navegador que el idioma de la página es español (`lang="es"`).
- **`<head>`**: Aquí va la **información** sobre la página, como el título y las configuraciones que el usuario no ve directamente en la página.
    - **`<meta charset="UTF-8">`**: Define el **tipo de caracteres** que usamos. UTF-8 es para que todos los caracteres (letras, símbolos) se muestren bien.
    - **`<meta name="viewport" content="width=device-width, initial-scale=1.0">`**: Esto ayuda a que la página se vea bien en dispositivos móviles, ajustando el ancho a la pantalla del dispositivo.
    - **`<title>Mi primera página</title>`**: Esto le da un **nombre** a la pestaña de la página en el navegador.
- **`<body>`**: Aquí es donde va todo el **contenido visible** de la página. Cosas como texto, imágenes, videos, etc.


### Alguna etiquetas HTML básicas

1. **Encabezados (`<h1>` a `<h2>`)**

Los encabezados se usan para títulos. Van desde `<h1>` (el mas grande) hasta `<h6>` (el más pequeño). Aquí un ejemplo:

```html
<h1>Titulo principal</h1>
<h2>Subtitulo</h2>
<h3>Sub-Subtitulo</h3>
```

2. **Párrafos (`<p>`)**

Usamos `<p>` para escribir párrafos de texto. Ejemplo:

```html
<p>Este es un párrafo de ejemplo.</p>
```

3. **Enlaces (`<a>`)**

Los enlaces permiten ir a otras páginas web. Usamos la etiqueta `<a>` con un atributo `href` para definir la dirección a la que llevará el enlace. Ejemplo:

```html
<a href="https://www.google.com">Ir a Google</a>
```

4. **Imágenes** (`<img>`)

Para mostrar imágenes, usamos la etiqueta `<img>`. El atributo `src` define la ubicación de la imagen, y `alt` es un texto alternativo que se muestra si la imagen no carga. Ejemplo:

```html
<img src="https://via.placeholder.com/150" alt="Ejemplo de imagen">
```

5. **Listas** (`<ul>`, `<ol>`, `<li>`)

- Las listas desordenadas (`<ul>`) son listas con **viñetas**.
- Las listas ordenadas (`<ol>`) son listas con **números**.

Ambas usan `<li>` para los elementos de la lista. Ejemplo:

```html
<ul>
	<li>Manzanas</li>
	<li>Plátanos</li>
	<li>Fresas</li>
</ul>

<ol>
	<li>Primero</li>
	<li>Segundo</li>
	<li>Tercero</li>
</ol>
```

6. **Divisiones (`<div>`)**

La etiqueta `<div>` se usa para agrupar secciones de una página. Piensa en `<div>` como una caja contenedora que puedes usar para organizar el contenido. No tiene un significado visual por si misma, pero es útil para aplicar estilos o organizar.

```html
<di>
	<h2>Seccion 1</h2>
	<p>Contenido de la sección 1.</p>
</div>
```

7. **Botones (`<button>`)**

Los botones en HTML se crean usando la etiqueta `<button>`:

```html
<button>Haz clic aqui</button>
```

## Atributos en HTML

Las etiquetas pueden tener **atributos**. Estos son como extras que dan más información a las etiquetas. Por ejemplo:

- En los enlaces(`<a>`), usamos `href` para definir a dónde va el enlace
- En la imágenes (`<img>`), usamos `src` para definir de dónde viene la imagen

Ejemplo con un enlace:

```html
<a href="https://www.google.com" target="_blank">Abrir Google en una nueva pestaña</a>
```

El atributo `target="_blank"` le dice al navegador que abra el enlace en una nueva pestaña

### ¡Un ejemplo competo de página web!

Aquí una página web muy simple con todo lo que hemos aprendido hasta ahora:

```html
<!DOCTYPE html>
<html lang="es">
	<head>
		<meta chartset="UTF-8">
		<meta name="viewport" content="width=device-width, initial-scale=1.0">
		<title> Mi Página Web</title>
	</head>
	<body>
		<h1> Bienvenido a mi página web</h1>
		<p>Esta es mi primera página web hecha con HTML.</p>
		<h2>Mis frutas favoritas</h2>
		<ul>
			<li>Manzanas</li>
			<li>Plátanos</li>
			<li>fresas</li>
		</ul>
		<h2> Ir a otros sitios web</h2>
		<p>Visita <a href="https://www.google.com" target="_blank">Google</a> o <a href="https://www.wikipedia.org" target="_blank">Wikipedia</a>.</p>
		<h2>Una imagen ejemplo</h2>
		<img src="https://via.placeholder.com/150" alt="Ejemplo de imagen">
		<button> Haz clic aqui</button>
	</body>
</html>
```

Este ejemplo incluye:

- Un título principal (`<h1>`).
- Un párrafo (`<p>`).
- Una lista de frutas (`<ul>`, `<li>`).
- Enlaces a otros sitios web (`<a>`).
- Una imagen (`<img>`).
- Un botón (`<button>`).


