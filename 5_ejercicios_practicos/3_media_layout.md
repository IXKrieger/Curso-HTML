
## Ejercicio 3: Media y Layout

**Enunciado:** Diseña una página de blog que incluya:

-   Un header con navegación
-   Una sección principal con un artículo
-   Una barra lateral
-   Un video incrustado
-   Un reproductor de audio
-   Un footer con información de contacto

**Código de ejemplo:**


```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Blog</title>
</head>
<body>
    <header>
        <h1>Mi Blog</h1>
        <nav>
            <a href="#home">Inicio</a> |
            <a href="#about">Acerca de</a> |
            <a href="#contact">Contacto</a>
        </nav>
    </header>
    <main>
        <article>
            <h2>Título del Artículo</h2>
            <p>Este es el contenido principal del artículo.</p>
        </article>
        <aside>
            <h3>Barra Lateral</h3>
            <p>Contenido adicional o enlaces.</p>
        </aside>
    </main>
    <section>
        <h2>Video</h2>
        <video controls>
            <source src="video.mp4" type="video/mp4">
            Tu navegador no soporta la etiqueta de video.
        </video>
        <h2>Audio</h2>
        <audio controls>
            <source src="audio.mp3" type="audio/mpeg">
            Tu navegador no soporta la etiqueta de audio.
        </audio>
    </section>
    <footer>
        <p>Contacto: contacto@blog.com</p>
    </footer>
</body>
</html>