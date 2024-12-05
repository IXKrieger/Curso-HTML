# 7. Mejores Prácticas y Optimización (Extendido)

## 7.1 Optimización para SEO

### 7.1.1 Meta Tags Esenciales

```html
<head>
    <!-- Meta tags básicos -->
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    
    <!-- Meta tags para SEO -->
    <title>Título Único y Descriptivo | Nombre de Marca</title>
    <meta name="description" content="Descripción única y relevante de la página en 150-160 caracteres que incluya palabras clave importantes.">
    <meta name="keywords" content="palabra clave 1, palabra clave 2, palabra clave 3">
    
    <!-- Open Graph para redes sociales -->
    <meta property="og:title" content="Título para Compartir">
    <meta property="og:description" content="Descripción para redes sociales">
    <meta property="og:image" content="https://tudominio.com/imagen.jpg">
    <meta property="og:url" content="https://tudominio.com/pagina">
    
    <!-- Twitter Cards -->
    <meta name="twitter:card" content="summary_large_image">
    <meta name="twitter:title" content="Título para Twitter">
    <meta name="twitter:description" content="Descripción para Twitter">
    
    <!-- Canonical URL -->
    <link rel="canonical" href="https://tudominio.com/pagina-original">
</head>
```

### 7.1.2 Estructura de Encabezados

```html
<body>
    <!-- Correcto uso de la jerarquía de encabezados -->
    <h1>Título Principal (solo uno por página)</h1>
    
    <section>
        <h2>Subtítulo Principal</h2>
        <h3>Subtítulo Secundario</h3>
        <h4>Subtítulo Terciario</h4>
    </section>
    
    <section>
        <h2>Otro Subtítulo Principal</h2>
        <!-- Evitar saltar niveles de encabezado -->
    </section>
</body>
```

## 7.2 Optimización de Imágenes

### 7.2.1 Imágenes Responsivas

```html
<!-- Uso de srcset para diferentes resoluciones -->
<img 
    srcset="imagen-pequeña.jpg 300w,
            imagen-mediana.jpg 600w,
            imagen-grande.jpg 900w"
    sizes="(max-width: 320px) 280px,
           (max-width: 640px) 580px,
           800px"
    src="imagen-default.jpg"
    alt="Descripción detallada"
    loading="lazy">

<!-- Uso de picture para art direction -->
<picture>
    <source media="(min-width: 800px)" srcset="hero-desktop.jpg">
    <source media="(min-width: 400px)" srcset="hero-tablet.jpg">
    <img src="hero-mobile.jpg" alt="Imagen adaptativa">
</picture>
```

## 7.3 Optimización de Rendimiento

### 7.3.1 Carga de Recursos

```html
<!-- Preload de recursos críticos -->
<link rel="preload" href="fuente-principal.woff2" as="font" type="font/woff2" crossorigin>
<link rel="preload" href="estilos-criticos.css" as="style">

<!-- Prefetch para navegación futura -->
<link rel="prefetch" href="pagina-siguiente.html">

<!-- DNS Prefetch -->
<link rel="dns-prefetch" href="//api.terceros.com">
```

### 7.3.2 Scripts Optimizados

```html
<!-- Carga asíncrona de scripts -->
<script async src="analytics.js"></script>

<!-- Scripts diferidos -->
<script defer src="no-critico.js"></script>

<!-- Módulos ES6 -->
<script type="module" src="app.js"></script>
```

## 7.4 Accesibilidad Avanzada

### 7.4.1 ARIA Roles y Atributos

```html
<!-- Navegación principal -->
<nav role="navigation" aria-label="Navegación principal">
    <ul>
        <li><a href="#" aria-current="page">Inicio</a></li>
        <li><a href="#">Productos</a></li>
    </ul>
</nav>

<!-- Regiones importantes -->
<main role="main">
    <article role="article">
        <h1>Título Principal</h1>
        <!-- Contenido -->
    </article>
    
    <aside role="complementary" aria-label="Información relacionada">
        <!-- Contenido secundario -->
    </aside>
</main>

<!-- Elementos interactivos -->
<button aria-expanded="false" aria-controls="menu-content">
    Menú
    <span class="sr-only">Abrir menú de navegación</span>
</button>
```

### 7.4.2 Skip Links y Contenido Oculto

```html
<!-- Skip links -->
<a href="#main-content" class="skip-link">
    Saltar al contenido principal
</a>

<!-- Contenido solo para lectores de pantalla -->
<style>
    .sr-only {
        position: absolute;
        width: 1px;
        height: 1px;
        padding: 0;
        margin: -1px;
        overflow: hidden;
        clip: rect(0,0,0,0);
        border: 0;
    }
</style>
```

## 7.5 Estructura Semántica Avanzada

```html
<body>
    <header role="banner">
        <nav role="navigation">
            <!-- Navegación -->
        </nav>
    </header>

    <main role="main">
        <article>
            <header>
                <h1>Título del Artículo</h1>
                <time datetime="2024-12-05">5 de Diciembre, 2024</time>
            </header>

            <section>
                <!-- Contenido principal -->
            </section>

            <footer>
                <div class="author" itemscope itemtype="http://schema.org/Person">
                    <span itemprop="name">Nombre del Autor</span>
                </div>
            </footer>
        </article>
    </main>

    <aside role="complementary">
        <!-- Contenido relacionado -->
    </aside>

    <footer role="contentinfo">
        <!-- Pie de página -->
    </footer>
</body>
```

## 7.6 Microdata y Schema.org

```html
<!-- Ejemplo de producto -->
<div itemscope itemtype="http://schema.org/Product">
    <h1 itemprop="name">Nombre del Producto</h1>
    <img itemprop="image" src="producto.jpg" alt="Descripción">
    <div itemprop="description">Descripción del producto</div>
    
    <div itemprop="offers" itemscope itemtype="http://schema.org/Offer">
        <span itemprop="price">19.99</span>
        <meta itemprop="priceCurrency" content="EUR">
    </div>
</div>

<!-- Ejemplo de artículo -->
<article itemscope itemtype="http://schema.org/Article">
    <h1 itemprop="headline">Título del Artículo</h1>
    <meta itemprop="datePublished" content="2024-12-05">
    <div itemprop="author" itemscope itemtype="http://schema.org/Person">
        <span itemprop="name">Nombre del Autor</span>
    </div>
</article>
```

## 7.7 Checklist de Optimización


### Lista de Verificación para un Sitio Web Óptimo

#### SEO Básico

1. **Meta tags completos y optimizados**: Asegúrate de que las etiquetas meta (título, descripción y palabras clave) estén completas y bien optimizadas. Estos elementos ayudan a los motores de búsqueda a entender el contenido de la página y a presentarla de manera atractiva en los resultados de búsqueda. 
   - *Ejemplo*: Una etiqueta meta descripción para una tienda de zapatos podría ser: "Encuentra los mejores zapatos de cuero hechos a mano para todas las ocasiones. Calidad y confort garantizados."

2. **Estructura de encabezados correcta**: Utiliza los encabezados HTML de forma jerárquica (H1, H2, H3, etc.) para estructurar el contenido. Esto facilita la comprensión del contenido tanto para los usuarios como para los motores de búsqueda.
   - *Ejemplo*: Utiliza `<h1>` para el título principal de la página, `<h2>` para secciones principales, y `<h3>` para subsecciones dentro de esas secciones.

3. **URLs amigables**: Las URLs deben ser claras, fáciles de leer y descriptivas. Idealmente, deben contener palabras clave relevantes y evitar caracteres especiales o cadenas de números sin sentido.
   - *Ejemplo*: En lugar de una URL como `www.ejemplo.com/producto?id=12345`, utiliza `www.ejemplo.com/zapatos-deportivos`.

4. **Contenido único y relevante**: El contenido debe ser original, atractivo y de valor para los usuarios. Además, evita el contenido duplicado para no recibir penalizaciones de los motores de búsqueda.
   - *Ejemplo*: Si estás creando contenido sobre "cómo cuidar zapatos de cuero", asegúrate de incluir consejos útiles y únicos que no se encuentren en otros sitios web.

#### Rendimiento

1. **Imágenes optimizadas**: Utiliza formatos de imagen adecuados y comprime las imágenes para reducir su tamaño sin sacrificar calidad. Esto mejora los tiempos de carga de la página.
   - *Ejemplo*: Utiliza herramientas como TinyPNG para reducir el tamaño de las imágenes antes de subirlas al sitio web.

2. **Carga lazy de recursos no críticos**: Implementa la carga diferida (lazy load) para recursos que no sean esenciales, como imágenes que están fuera del viewport inicial. Esto ayuda a mejorar el tiempo de carga inicial de la página.
   - *Ejemplo*: Utiliza la librería `lazysizes` para implementar la carga diferida de imágenes.

3. **Minificación de recursos**: Reduce el tamaño de los archivos CSS, JavaScript y HTML mediante minificación. Esto implica eliminar espacios en blanco, comentarios y otros elementos innecesarios para reducir el peso de los recursos.
   - *Ejemplo*: Herramientas como `UglifyJS` o `CSSNano` pueden ayudar a minificar los archivos.

4. **Caché apropiado**: Configura políticas de caché adecuadas para que los recursos estáticos no necesiten descargarse cada vez que un usuario visita la página, mejorando así la velocidad de carga.
   - *Ejemplo*: Configura el encabezado `Cache-Control` para permitir que el navegador almacene recursos durante un periodo prolongado.

#### Accesibilidad

1. **ARIA roles implementados**: Utiliza roles ARIA para mejorar la accesibilidad de la página, proporcionando información adicional a tecnologías asistivas como los lectores de pantalla.
   - *Ejemplo*: Usa `role="navigation"` para identificar una barra de navegación y ayudar a los usuarios con lectores de pantalla a entender su propósito.

2. **Contraste de colores adecuado**: Asegúrate de que el contraste entre el texto y el fondo sea suficiente para que el contenido sea legible para personas con discapacidades visuales.
   - *Ejemplo*: Utiliza herramientas como `Contrast Checker` para verificar que el contraste cumpla con las pautas WCAG.

3. **Navegación por teclado**: Garantiza que toda la página pueda ser navegada usando solo el teclado, lo cual es fundamental para usuarios con discapacidades motoras.
   - *Ejemplo*: Prueba la página asegurándote de que puedas navegar por todos los elementos importantes usando la tecla `Tab`.

4. **Textos alternativos**: Proporciona descripciones (atributo alt) a todas las imágenes para que los usuarios que utilizan lectores de pantalla puedan entender el contenido visual.
   - *Ejemplo*: Para una imagen de un zapato, el atributo `alt` podría ser: "Zapato deportivo de cuero marrón con suela blanca".

#### Móvil

1. **Diseño responsive**: Adapta el diseño del sitio para que funcione bien en dispositivos de diferentes tamaños de pantalla, desde móviles hasta monitores de escritorio.
   - *Ejemplo*: Utiliza frameworks como `Bootstrap` para implementar un diseño responsive rápidamente.

2. **Viewport configurado**: Asegúrate de que la metaetiqueta viewport esté configurada correctamente para controlar cómo se muestra la página en dispositivos móviles.
   - *Ejemplo*: Usa `<meta name="viewport" content="width=device-width, initial-scale=1.0">` para asegurar una buena visualización en dispositivos móviles.

3. **Touch targets adecuados**: Los botones y enlaces deben ser lo suficientemente grandes y estar espaciados adecuadamente para facilitar la interacción táctil sin errores.
   - *Ejemplo*: Asegúrate de que los botones tengan al menos 48x48 píxeles de tamaño para que puedan ser pulsados fácilmente.

4. **Contenido adaptativo**: Ajusta el contenido para que sea fácil de consumir en dispositivos móviles, eliminando o reorganizando elementos que no aporten valor en pantallas más pequeñas.
   - *Ejemplo*: Reduce el tamaño de las imágenes y elimina elementos secundarios en la versión móvil para mejorar la experiencia del usuario.




## 7.8 Optimización para SEO y Metadatos

La optimización para motores de búsqueda (SEO) comienza desde la estructura básica de nuestro HTML. Empecemos por la sección `head`, que es crucial para el SEO:

```html
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Guía Completa de Desarrollo Web | Academia Dev</title>
    <meta name="description" content="Aprende desarrollo web desde cero con nuestra guía completa. Incluye HTML, CSS, JavaScript y más.">
</head>
```

El título y la descripción son fundamentales. El título debe ser único y descriptivo, idealmente entre 50-60 caracteres. La descripción debe ser un resumen convincente de la página en 150-160 caracteres. Piensa en ellos como tu "anuncio" en los resultados de búsqueda.

Para mejorar aún más la visibilidad en redes sociales, añadimos las meta tags de Open Graph:

```html
<head>
    <!-- Meta tags anteriores... -->
    <meta property="og:title" content="Guía Completa de Desarrollo Web">
    <meta property="og:description" content="Domina el desarrollo web con nuestra guía paso a paso">
    <meta property="og:image" content="https://tudominio.com/imagen-curso.jpg">
</head>
```

Estas etiquetas controlan cómo se ve tu contenido cuando se comparte en redes sociales. Es importante que la imagen sea atractiva y representativa, ya que puede aumentar significativamente las tasas de clic.

---

## Estructura Semántica y Accesibilidad

La estructura semántica no solo ayuda al SEO, sino que hace tu sitio más accesible. Veamos un ejemplo práctico:

```html
<header>
    <nav>
        <ul>
            <li><a href="#inicio">Inicio</a></li>
            <li><a href="#cursos">Cursos</a></li>
            <li><a href="#contacto">Contacto</a></li>
        </ul>
    </nav>
</header>

<main>
    <article>
        <h1>Aprende Desarrollo Web</h1>
        <p>Descubre cómo crear sitios web profesionales desde cero...</p>
        
        <section>
            <h2>HTML Fundamental</h2>
            <p>El HTML es el esqueleto de toda página web...</p>
        </section>
    </article>
</main>
```

Esta estructura no solo es clara para los desarrolladores, sino que también:

- Ayuda a los lectores de pantalla a navegar el contenido
- Mejora el SEO al indicar claramente la jerarquía del contenido
- Hace el código más mantenible y escalable

---

## Optimización de Imágenes

Las imágenes son a menudo el recurso más pesado en una página web. Aquí hay un ejemplo de cómo optimizarlas:

```html
<picture>
    <source 
        media="(min-width: 800px)" 
        srcset="hero-desktop.jpg 1200w,
                hero-desktop-small.jpg 800w">
    <source 
        media="(min-width: 400px)" 
        srcset="hero-tablet.jpg">
    <img 
        src="hero-mobile.jpg" 
        alt="Estudiantes aprendiendo desarrollo web"
        loading="lazy">
</picture>
```

Este código hace varias cosas inteligentes:

- Proporciona diferentes imágenes según el tamaño de la pantalla
- Usa lazy loading para cargar las imágenes solo cuando son necesarias
- Incluye un alt descriptivo para accesibilidad y SEO

---

## Formularios Accesibles

Los formularios son puntos de interacción crucial. Aquí hay un ejemplo de un formulario bien estructurado:

```html
<form method="post" action="/registro">
    <div class="form-group">
        <label for="nombre">Nombre completo</label>
        <input 
            type="text" 
            id="nombre" 
            name="nombre" 
            required 
            aria-required="true"
            autocomplete="name">
        <span class="error" aria-live="polite"></span>
    </div>

    <div class="form-group">
        <label for="email">Correo electrónico</label>
        <input 
            type="email" 
            id="email" 
            name="email" 
            required
            aria-required="true"
            autocomplete="email">
        <span class="error" aria-live="polite"></span>
    </div>

    <button type="submit">Registrarse</button>
</form>
```

Este formulario incluye:

- Labels claramente asociados con sus inputs
- Atributos ARIA para mejorar la accesibilidad
- Autocompletado para mejor experiencia de usuario
- Manejo de errores accesible

---

## Rendimiento y Carga de Recursos

La forma en que cargamos los recursos puede afectar dramáticamente el rendimiento. Aquí hay un ejemplo de carga optimizada:

```html
<!-- Estilos críticos inline -->
<style>
    /* Estilos críticos para el primer render */
    .header { /* ... */ }
    .hero { /* ... */ }
</style>

<!-- Precargar recursos críticos -->
<link rel="preload" href="fuente-principal.woff2" as="font" type="font/woff2" crossorigin>

<!-- Cargar CSS no crítico de forma asíncrona -->
<link rel="stylesheet" href="estilos.css" media="print" onload="this.media='all'">

<!-- Scripts con carga optimizada -->
<script src="analytics.js" async></script>
<script src="app.js" defer></script>
```

Esta estrategia:

- Muestra contenido crítico lo antes posible
- Carga recursos secundarios sin bloquear el renderizado
- Prioriza la experiencia del usuario

---

## Microdata para SEO Avanzado

Los datos estructurados ayudan a los motores de búsqueda a entender mejor tu contenido:

```html
<article itemscope itemtype="http://schema.org/BlogPosting">
    <h1 itemprop="headline">Guía Definitiva de HTML</h1>
    
    <div itemprop="author" itemscope itemtype="http://schema.org/Person">
        <span itemprop="name">Ana García</span>
    </div>

    <time itemprop="datePublished" datetime="2024-12-05">
        5 de diciembre, 2024
    </time>

    <div itemprop="articleBody">
        <p>Aprende todo sobre HTML moderno...</p>
    </div>
</article>
```

Esto puede resultar en rich snippets en los resultados de búsqueda, mejorando la visibilidad y las tasas de clic.

---



### 7.9 Microdata y SEO Avanzado Explicado Simplemente

La Microdata es como poner etiquetas especiales en tu HTML que ayudan a Google y otros buscadores a entender mejor qué es cada cosa en tu página web. Es como darle "pistas" al buscador sobre tu contenido.

## ¿Por qué es importante?

- Hace que tu página aparezca mejor en los resultados de búsqueda
- Puede mostrar información extra (como estrellas de valoración, precios, etc.)
- Mejora el SEO de tu página

---

## Ejemplos Prácticos

### 1. Para un Artículo de Blog

```html
<article itemscope itemtype="http://schema.org/BlogPosting">
    <!-- El título del artículo -->
    <h1 itemprop="headline">10 Trucos de Cocina Fáciles</h1>
    
    <!-- El autor -->
    <div itemprop="author">Por María González</div>
    
    <!-- La fecha -->
    <time itemprop="datePublished">15 de Diciembre, 2024</time>
    
    <!-- El contenido -->
    <div itemprop="articleBody">
        <p>Hoy vamos a aprender trucos de cocina...</p>
    </div>
</article>
```

Este código le dice a Google:

- Esto es un artículo de blog
- El título es "10 Trucos de Cocina Fáciles"
- Lo escribió María González
- Se publicó el 15 de Diciembre

---

### 2. Para un Producto

```html
<div itemscope itemtype="http://schema.org/Product">
    <!-- Nombre del producto -->
    <h1 itemprop="name">Zapatillas Deportivas XYZ</h1>
    
    <!-- Imagen del producto -->
    <img itemprop="image" src="zapatillas.jpg" alt="Zapatillas XYZ">
    
    <!-- Precio -->
    <div itemprop="offers" itemscope itemtype="http://schema.org/Offer">
        <span itemprop="price">59.99</span>
        <meta itemprop="priceCurrency" content="EUR">
    </div>
    
    <!-- Valoraciones -->
    <div itemprop="review" itemscope itemtype="http://schema.org/Review">
        <span itemprop="ratingValue">4.5</span> de 5 estrellas
    </div>
</div>
```

Este código le dice a Google:

- Es un producto
- Se llama "Zapatillas Deportivas XYZ"
- Cuesta 59.99€
- Tiene una valoración de 4.5/5

---

### 3. Para una Receta

```html
<div itemscope itemtype="http://schema.org/Recipe">
    <!-- Nombre de la receta -->
    <h1 itemprop="name">Tarta de Chocolate Casera</h1>
    
    <!-- Tiempo de preparación -->
    <meta itemprop="prepTime" content="PT30M">30 minutos
    
    <!-- Ingredientes -->
    <ul>
        <li itemprop="recipeIngredient">200g de chocolate</li>
        <li itemprop="recipeIngredient">3 huevos</li>
        <li itemprop="recipeIngredient">150g de azúcar</li>
    </ul>
    
    <!-- Instrucciones -->
    <div itemprop="recipeInstructions">
        <p>1. Derrite el chocolate...</p>
    </div>
</div>
```

---

## Beneficios Visuales en Google

Cuando usas Microdata, tu resultado en Google puede verse así:

### Para un producto:

```
⭐⭐⭐⭐½ 59.99€ - Zapatillas Deportivas XYZ
[Imagen del producto] Disponible en stock...
```

### Para una receta:

```
🕒 30 min | ⭐⭐⭐⭐ | Tarta de Chocolate Casera
[Imagen] Una deliciosa receta casera...
```

---

## Consejos Prácticos

1. **Sé específico:** Usa las propiedades más específicas posibles para tu contenido.
2. **Sé consistente:** Si empiezas a usar Microdata, úsala en todas las páginas similares.
3. **Verifica tu código:** Usa la herramienta de prueba de datos estructurados de Google para asegurarte de que todo está bien implementado.
4. **Mantén la relevancia:** Solo marca el contenido que realmente es importante y relevante.

---

## Herramientas Útiles

### Probador de Datos Estructurados de Google
https://search.google.com/test/rich-results?hl=es

- **Pega tu URL o código HTML**
- **Te muestra cómo lo ve Google**
- **Detecta errores**

### Schema.org

- **Sitio oficial con todos los tipos de Microdata**
- **Ejemplos y documentación**

https://developers.google.com/search/docs/appearance/structured-data?hl=es