## ¿Qué es HTML Semántico?

HTML semántico significa usar etiquetas que tienes un significado claro sobre el contenido que contienen. En lugar de usar etiquetas genéricas como `<div>` o `<span>` para todo, HTML semántico nos da etiquetas que describen mejor el **propósito** del contenido, lo que hace que el código sea más fácil de entender tanto para humanos con para las **máquinas** (como los navegadores y motores de búsqueda).

Piensa en HTML semántico como si estuvieras escribiendo un **libro** y estuvieras usando capítulos, títulos y subtítulos para organizar el contenido. si lo organizas bien, cualquiera puede entender mejor de qué se trata

#### ¿Por qué es importante?

1. **Mejor legibilidad:** Las etiquetas semánticas hacen que el código sea más fácil de leer y entender.

2. SEO (**Optimización para motores de  búsqueda**): Los motores de búsqueda (como Google) comprenden mejor la estructura de la página y pueden mostrarla mejor en los resultados de búsqueda

3. **Accesibilidad:** Ayuda a las tecnologías como los lectores de pantalla a interpretar mejor el contenido para personas con discapacidades visuales.

4. **Mantenimiento:** Si tu código es más claro, será más fácil de mantener y actualizar en el futuro.

## Diferencia entre etiquetas no semánticas y semánticas
**Etiquetas no semánticas:**
- Estas etiquetas no le dicen al navegador ni a los desarrolladores qué tipo de contenido tienen dentro
- Ejemplos `<div>` `<span>`

**Etiquetas semánticas:**
- Estas etiquetas describen el propósito del contenido
- Ejemplos: `<header>` `<footer>` `<article>` `<section>` `<nav>` `<aside>`

### Ejemplo: No semánticos vs semántico
**No semántico:**

```html
<di>
	<div>Mi encabezado</div>
	<div>Esto es un articulo de noticias</div>
	<div>Un enlace a algo</div>
</div>
```

Aquí no sabemos qué función tiene cada bloque de contenido. Solo vemos muchos `<div>` que no nos dicen mucho.

**Semántico:**

```html
<header> Mi encabezado</header>
<article> Esto es un articulo de noticias </article>
<nav> enlace a algo </nav>
```

En este caso, es mucho más fácil de entender qué es cada sección de la página: hay un **encabezado**, un articulo y una navegacion (los enlaces)

## Principales etiquetas semánticas en HTML5

1. `<header>` Es la parte superior de una página o sección. Suele contener el logo el titulo o el menu de navegación

```html
<header>
	<h1> Mi sitio web</h1>
	<nav>
		<a href="#"> Inicio </a>
		< a href="#"> Sobre mi </a>
	</nav>
</header>
```

2. `<nav>` Se usa para definir un conjunto de enlaces de navegación, normalmente un menú para moverte por el sitio web.

```html
<nav>
	<a href="#">Inicio</a>
	<a href="#">Articulos</a>
	<a href="#">Contacto</a>
</nav>
```

3. `<main>` Indica el contenido principal de la página. Solo debe haber un `<main>` por página:

```html
<main>
	<h2>Articulo principal</h2>
	<p>Este es el contenido principal del sitio web</p>
</main>
```

4. `<article>` Representa un contenido independiente, como un articulo de blog o una noticia, o una publicación

```html
<article>
	<h2>Cómo hacer una pagina web</h2>
	<p>Este articulo te enseña a hacer una página web</p>
</article>
```

5. `<section>` Se usa para agrupar secciones relacionas en una página. Es como si dijeras: "Este grupo de contenido está relacionado entre si".

```html
<section>
	<h2>Sección de noticias</h2>
	<p>Noticias recientes sobre tecnologia.</p>
</section>
```

6. `<footer>` Es la parte inferior de la página o sección. Aquí suele ir la información como el **copyright** los enlaces de contacto, o el mapa del sitio.

```html
<footer>
	<p>2024 Mi sitio web. todos los derechos reservados.
</footer>
```

7. `<aside>` Se usa para contenido relacionado, pero no parte del contenido principal como una barra lateral con anuncios o enlaces adicionales

```html
<aside>
	<h3>Publicidad</h3>
	<p>¡Compra nuestos productos ahora!</p>
</aside>
```

### Ejemplo completo de HTML semántico:

```html
<!DOCTYPE html>
<html lang="es">

<head>
  <!-- Metadatos importantes -->
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta name="description" content="Aprendiendo HTML">
  <meta name="keywords" content="Aprendizaje, HTML, 2024, Programacion">
  <meta name="author" content="Sebastian Marquez">

  <!-- T├¡tulo del sitio -->
  <title>SEBASCMB</title>

</head>

<body>
  <header>
    <h1>Mi sitio web</h1>
    <nav>
      <a href="#">Inicio</a>
      <a href="#">Articulos</a>
      <a href="#">Contacto</a>
    </nav>
  </header>

  <main>
    <h2>Articulo Principal</h2>
    <p>Este es el contenido principal del stio web</p>
  </main>


  <article>
    <h2>Como hacer una pagina web</h2>
    <p>Este articulo te ense├▒a a como crear una p├ígina web</p>
  </article>

  <section>
    <h2>Secci├│n de noticias</h2>
    <p>Noticias recientes sobre tecnologia</p>
  </section>

  <aside>
    <h3>Publicidad</h3>
    <p>┬íCompra nuestro productos ahora!</p>
  </aside>

  <footer>
    <p>&copy; 2024 Mi sitio Web. Todos los derechos reservados.</p>
  </footer>

</body>

</html>
```

## ¿Qué hemos aprendido?

- **HTML semántico** nos ayuda a organizar mejor el contenido de las páginas.
- Los navegadores y motores de búsqueda **entienden mejor** el propósito del contenido con etiquetas semánticas.
- Hace que el código sea más **fácil de leer** y **mantener**.
  
![Ejemplo](https://github.com/user-attachments/assets/e58ba138-98e5-4570-a21b-bc05959003f4)


