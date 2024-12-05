# 1. HTML Básico

## 1.1 Introducción a HTML
HTML (HyperText Markup Language) es el lenguaje estándar para crear páginas web. Es como el esqueleto de cualquier sitio web, proporcionando la estructura básica y el contenido.

Para empezar, todo documento HTML debe tener una estructura básica:

```html
<!DOCTYPE html>
<html>
<head>
    <title>Mi primera página web</title>
</head>
<body>
    <h1>¡Bienvenido a mi sitio!</h1>
    <p>Este es mi primer documento HTML.</p>
</body>
</html>
```

## 1.2 Ejemplos básicos
Veamos algunos ejemplos prácticos de elementos HTML básicos:

```html
<!-- Un párrafo simple -->
<p>Este es un párrafo de texto.</p>

<!-- Un encabezado con un párrafo -->
<h1>Mi título principal</h1>
<p>Este es el contenido debajo del título.</p>

<!-- Un enlace simple -->
<a href="https://www.ejemplo.com">Visita mi sitio web</a>
```

## 1.3 Elementos
Los elementos HTML son los bloques de construcción de una página web. Cada elemento se define mediante etiquetas de apertura y cierre:

```html
<!-- Estructura de un elemento -->
<etiqueta>Contenido</etiqueta>

<!-- Ejemplos prácticos -->
<p>Este es un párrafo</p>
<div>Este es un contenedor</div>
<span>Este es un texto en línea</span>
```

## 1.4 Atributos
Los atributos proporcionan información adicional o modifican el comportamiento de los elementos HTML:

```html
<!-- Estructura básica de atributos -->
<elemento atributo="valor">Contenido</elemento>

<!-- Ejemplos prácticos -->
<img src="imagen.jpg" alt="Mi imagen">
<a href="https://www.ejemplo.com" target="_blank">Abrir en nueva pestaña</a>
<p class="destacado">Texto importante</p>
```

## 1.5 Encabezados
HTML ofrece seis niveles de encabezados, desde `h1` hasta `h6`:

```html
<h1>Encabezado principal</h1>
<h2>Subtítulo importante</h2>
<h3>Título de sección</h3>
<h4>Subtítulo menor</h4>
<h5>Título pequeño</h5>
<h6>El encabezado más pequeño</h6>
```

## 1.6 Párrafos
Los párrafos son fundamentales para organizar el texto:

```html
<p>Este es un párrafo normal. Puede contener mucho texto y se ajustará automáticamente al ancho del contenedor.</p>

<p>Los párrafos crean automáticamente
    espacios entre ellos, sin importar
    los saltos de línea en el código.</p>

<!-- Forzar salto de línea -->
<p>Primera línea<br>Segunda línea</p>
```

## 1.7 Formato de texto
HTML permite dar formato al texto de diferentes maneras:

```html
<p><strong>Texto en negrita</strong></p>
<p><em>Texto en cursiva</em></p>
<p><mark>Texto resaltado</mark></p>
<p><sub>Subíndice</sub> y <sup>Superíndice</sup></p>
<p><u>Texto subrayado</u></p>
<p><del>Texto tachado</del></p>
```

## 1.8 Comentarios
Los comentarios son útiles para documentar el código:

```html
<!-- Esto es un comentario de una línea -->

<!--
    Este es un comentario
    de múltiples líneas
    que no se mostrará en el navegador
-->
```

## 1.9 Enlaces
Los enlaces son fundamentales para la navegación:

```html
<!-- Enlace básico -->
<a href="https://www.ejemplo.com">Visitar sitio</a>

<!-- Enlace que abre en nueva pestaña -->
<a href="https://www.ejemplo.com" target="_blank">Abrir en nueva pestaña</a>

<!-- Enlace a una sección de la misma página -->
<a href="#seccion1">Ir a sección 1</a>

<!-- Enlace a un correo electrónico -->
<a href="mailto:correo@ejemplo.com">Enviar email</a>
```

## 1.10 Imágenes
Las imágenes se insertan usando la etiqueta `img`:

```html
<!-- Imagen básica -->
<img src="foto.jpg" alt="Descripción de la imagen">

<!-- Imagen con dimensiones específicas -->
<img src="foto.jpg" alt="Descripción" width="300" height="200">

<!-- Imagen con título -->
<img src="foto.jpg" alt="Descripción" title="Título al pasar el mouse">
```

## 1.11 Tablas
Las tablas se utilizan para organizar datos en filas y columnas:

```html
<table border="1">
    <thead>
        <tr>
            <th>Encabezado 1</th>
            <th>Encabezado 2</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Celda 1</td>
            <td>Celda 2</td>
        </tr>
        <tr>
            <td>Celda 3</td>
            <td>Celda 4</td>
        </tr>
    </tbody>
</table>
```

## 1.12 Listas
HTML permite crear tres tipos de listas:

```html
<!-- Lista ordenada -->
<ol>
    <li>Primer elemento</li>
    <li>Segundo elemento</li>
    <li>Tercer elemento</li>
</ol>

<!-- Lista no ordenada -->
<ul>
    <li>Elemento</li>
    <li>Otro elemento</li>
    <li>Un elemento más</li>
</ul>

<!-- Lista de definición -->
<dl>
    <dt>Término</dt>
    <dd>Definición del término</dd>
    <dt>Otro término</dt>
    <dd>Su definición</dd>
</dl>
