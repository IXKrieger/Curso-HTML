# Proyecto: Portfolio Personal

```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mi Portfolio Personal</title>
</head>
<body>
    <!-- Header con navegación -->
    <header>
        <nav>
            <ul>
                <li><a href="#inicio">Inicio</a></li>
                <li><a href="#sobre-mi">Sobre Mí</a></li>
                <li><a href="#proyectos">Proyectos</a></li>
                <li><a href="#contacto">Contacto</a></li>
            </ul>
        </nav>
    </header>

    <!-- Sección principal -->
    <main>
        <!-- Sección de inicio -->
        <section id="inicio">
            <h1>Juan Desarrollador</h1>
            <picture>
                <source media="(min-width: 800px)" srcset="foto-grande.jpg">
                <source media="(min-width: 400px)" srcset="foto-mediana.jpg">
                <img src="foto-pequeña.jpg" alt="Mi foto de perfil">
            </picture>
        </section>

        <!-- Sobre mí -->
        <section id="sobre-mi">
            <h2>Sobre Mí</h2>
            <article>
                <p>Desarrollador web con experiencia en HTML, CSS y JavaScript.</p>
                <blockquote>
                    <p>"La programación es el arte de resolver problemas"</p>
                </blockquote>
            </article>
        </section>

        <!-- Proyectos -->
        <section id="proyectos">
            <h2>Mis Proyectos</h2>
            <div class="proyecto">
                <h3>Proyecto 1</h3>
                <img src="proyecto1.jpg" alt="Captura del Proyecto 1">
                <p>Descripción del proyecto...</p>
            </div>
            <!-- Más proyectos... -->
        </section>

        <!-- Formulario de contacto -->
        <section id="contacto">
            <h2>Contacto</h2>
            <form action="/enviar" method="POST">
                <label for="nombre">Nombre:</label>
                <input type="text" id="nombre" name="nombre" required>

                <label for="email">Email:</label>
                <input type="email" id="email" name="email" required>

                <label for="mensaje">Mensaje:</label>
                <textarea id="mensaje" name="mensaje" rows="5" required></textarea>

                <button type="submit">Enviar Mensaje</button>
            </form>
        </section>
    </main>

    <!-- Footer -->
    <footer>
        <p>© 2024 Mi Portfolio. Todos los derechos reservados.</p>
        <div class="social-links">
            <a href="https://github.com/usuario">GitHub</a>
            <a href="https://linkedin.com/in/usuario">LinkedIn</a>
        </div>
    </footer>
</body>
</html>