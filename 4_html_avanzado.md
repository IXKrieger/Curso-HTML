# 4. HTML avanzado

## 4.1 Citas y menciones
HTML ofrece diferentes elementos para citas y referencias:

```html
<!-- Cita en bloque -->
<blockquote cite="https://fuente.com">
    <p>Esta es una cita larga que ocupará un bloque independiente con sangría.</p>
    <footer>— Autor de la cita</footer>
</blockquote>

<!-- Cita en línea -->
<p>Como dijo alguien famoso: <q>Esta es una cita corta en línea</q></p>

<!-- Abreviaciones -->
<p>Usamos <abbr title="HyperText Markup Language">HTML</abbr> para crear páginas web.</p>
```

## 4.2 Mapas de imagen
Los mapas de imagen permiten crear áreas clicables en una imagen:

```html
<img src="mapa.jpg" alt="Navegación" usemap="#workmap">

<map name="workmap">
    <area shape="rect" coords="34,44,270,350" alt="Computadora" href="computer.htm">
    <area shape="rect" coords="290,172,333,250" alt="Teléfono" href="phone.htm">
    <area shape="circle" coords="337,300,44" alt="Taza de café" href="coffee.htm">
</map>
```

## 4.3 El elemento picture
`Picture` permite especificar diferentes imágenes para diferentes dispositivos/pantallas:

```html
<picture>
    <source media="(min-width: 650px)" srcset="img_large.jpg">
    <source media="(min-width: 465px)" srcset="img_medium.jpg">
    <img src="img_small.jpg" alt="Imagen responsive" style="width:auto;">
</picture>
```

## 4.4 Bloques y elementos en línea
La diferencia entre elementos de bloque y en línea:

```html
<!-- Elementos de bloque -->
<div style="border: 1px solid black">
    Este div ocupará toda la línea
</div>
<p>Los párrafos son elementos de bloque</p>

<!-- Elementos en línea -->
<span style="border: 1px solid red">Este span es en línea</span>
<a href="#">Los enlaces son en línea</a>
<strong>El texto en negrita es en línea</strong>
```

## 4.5 Iframes
Los iframes permiten incrustar contenido de otros sitios web:

```html
<!-- Iframe básico -->
<iframe src="https://www.ejemplo.com" width="500" height="300"></iframe>

<!-- Iframe con bordes y scrolling -->
<iframe 
    src="https://www.ejemplo.com" 
    width="500" 
    height="300"
    frameborder="0"
    scrolling="no">
</iframe>
```

## 4.6 Head
El elemento head contiene metadatos importantes:

```html
<!DOCTYPE html>
<html>
<head>
    <!-- Título de la página -->
    <title>Mi Página Web</title>
    
    <!-- Metadatos -->
    <meta charset="UTF-8">
    <meta name="description" content="Descripción de mi página">
    <meta name="keywords" content="HTML, CSS, JavaScript">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    
    <!-- Enlaces a recursos externos -->
    <link rel="stylesheet" href="styles.css">
    <link rel="icon" href="favicon.ico" type="image/x-icon">
    
    <!-- Scripts -->
    <script src="script.js"></script>
</head>
<body>
    <!-- Contenido de la página -->
</body>
</html>
```

## 4.7 Layouts
Estructuras modernas de layout usando elementos semánticos:

```html
<body>
    <header>
        <nav>
            <ul>
                <li><a href="#home">Inicio</a></li>
                <li><a href="#about">Acerca de</a></li>
            </ul>
        </nav>
    </header>

    <main>
        <article>
            <section>
                <h2>Sección Principal</h2>
                <p>Contenido principal...</p>
            </section>
        </article>

        <aside>
            <h3>Barra lateral</h3>
            <p>Contenido relacionado...</p>
        </aside>
    </main>

    <footer>
        <p>Pie de página © 2024</p>
    </footer>
</body>
```

## 4.8 Elementos de código
HTML tiene elementos especiales para mostrar código:

```html
<!-- Código en línea -->
<p>El elemento <code>div</code> es un contenedor.</p>

<!-- Bloque de código preformateado -->
<pre>
<code>
function saludar() {
    console.log("\u00a1Hola mundo!");
}
</code>
</pre>

<!-- Salida de computadora -->
<samp>Error 404: Página no encontrada</samp>

<!-- Entrada de teclado -->
<p>Presiona <kbd>Ctrl</kbd> + <kbd>C</kbd> para copiar</p>
```

## 4.9 Semántica
Elementos semánticos para mejor estructura y SEO:

```html
<article>
    <header>
        <h1>Título del Artículo</h1>
        <time datetime="2024-12-05">5 de Diciembre, 2024</time>
    </header>

    <section>
        <h2>Primera Sección</h2>
        <p>Contenido...</p>
    </section>

    <aside>
        <h3>Contenido Relacionado</h3>
        <p>Enlaces y referencias...</p>
    </aside>

    <footer>
        <p>Autor: Juan Pérez</p>
    </footer>
</article>
```

## 4.10 Entidades
Las entidades HTML permiten mostrar caracteres especiales:

```html
<!-- Espacios y símbolos -->
<p>Espacio&nbsp;fijo</p>
<p>Símbolo de copyright &copy;</p>
<p>Menor que &lt; y mayor que &gt;</p>
<p>Símbolo de euro &euro;</p>
<p>Comillas &quot;citadas&quot;</p>
```

## 4.11 Emojis
Los emojis se pueden insertar directamente o usando códigos:

```html
<!-- Emojis directos -->
<p>🌟 Estrella</p>
<p>👋 Saludo</p>
<p>❤️ Corazón</p>

<!-- Usando códigos -->
<p>&#128512; Cara sonriente</p>
<p>&#128151; Corazón</p>
```

## 4.12 Guía de estilo
Buenas prácticas para escribir HTML limpio y mantenible:

```html
<!-- Use indentación consistente -->
<div>
    <p>
        Texto indentado correctamente
    </p>
</div>

<!-- Use nombres descriptivos en minúsculas -->
<div class="user-profile">
    <img class="profile-image" src="avatar.jpg" alt="Foto de perfil">
</div>

<!-- Cierre todas las etiquetas -->
<p>Párrafo completo</p>

<!-- Use comillas dobles para atributos -->
<a href="página.html" class="link-principal">Enlace</a>

<!-- Incluya el alt en imágenes -->
<img src="foto.jpg" alt="Descripción de la imagen">
