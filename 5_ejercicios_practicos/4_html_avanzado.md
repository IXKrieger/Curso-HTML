## Ejercicio 4: HTML Avanzado

**Enunciado:** Crea una página de portfolio que utilice:

-   Elementos semánticos
-   `<picture>` para imágenes responsive
-   `<iframe>` para mostrar un mapa
-   Citas y referencias
-   Emojis y entidades especiales

**Código de ejemplo:**


```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Portfolio</title>
</head>
<body>
    <header>
        <h1>Portfolio</h1>
    </header>
    <section>
        <h2>Sobre Mí</h2>
        <p>¡Hola! Soy un desarrollador web apasionado por crear experiencias digitales únicas. 🌟</p>
    </section>
    <section>
        <h2>Proyectos</h2>
        <article>
            <h3>Proyecto 1</h3>
            <picture>
                <source srcset="https://placehold.co/600x400" media="(min-width: 800px)">
                <img src="https://placehold.co/600x400" alt="Descripción del proyecto">
            </picture>
        </article>
    </section>
    <section>
        <h2>Ubicación</h2>
        <iframe src="https://www.google.com/maps/embed?pb=" width="600" height="450" style="border:0;" allowfullscreen="" loading="lazy"></iframe>
    </section>
    <section>
        <h2>Testimonios</h2>
        <blockquote>
            "Este desarrollador es increíblemente talentoso." 
            <cite>- Cliente Satisfecho</cite>
        </blockquote>
    </section>
    <footer>
        <p>Contacto: contacto@portfolio.com</p>
        <p>&#169; 2024 Portfolio</p>
    </footer>
</body>
</html>