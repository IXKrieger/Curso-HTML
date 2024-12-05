# 2. Formularios

## 2.1 Introducción a los formularios
Los formularios son elementos fundamentales para recoger información del usuario. Se crean usando la etiqueta `<form>`:

```html
<form action="/procesar.php" method="post">
    <!-- Elementos del formulario irán aquí -->
    <input type="text" name="nombre">
    <button type="submit">Enviar</button>
</form>
```

## 2.2 Elementos de formularios
Los formularios pueden contener diversos elementos:

```html
<form>
    <!-- Campo de texto con etiqueta -->
    <label for="nombre">Nombre:</label>
    <input type="text" id="nombre" name="nombre">

    <!-- Área de texto -->
    <label for="comentario">Comentario:</label>
    <textarea id="comentario" name="comentario" rows="4" cols="50"></textarea>

    <!-- Lista desplegable -->
    <label for="pais">País:</label>
    <select id="pais" name="pais">
        <option value="es">España</option>
        <option value="mx">México</option>
        <option value="ar">Argentina</option>
    </select>

    <!-- Grupo de opciones -->
    <fieldset>
        <legend>Información de contacto</legend>
        <input type="text" name="email" placeholder="Email">
        <input type="tel" name="telefono" placeholder="Teléfono">
    </fieldset>
</form>
```

## 2.3 Tipos de input
HTML5 introdujo varios tipos de input especializados:

```html
<form>
    <!-- Texto básico -->
    <input type="text" placeholder="Texto normal">

    <!-- Email -->
    <input type="email" placeholder="correo@ejemplo.com">

    <!-- Contraseña -->
    <input type="password" placeholder="Contraseña">

    <!-- Número -->
    <input type="number" min="0" max="100" step="1">

    <!-- Fecha -->
    <input type="date">

    <!-- Hora -->
    <input type="time">

    <!-- Color -->
    <input type="color">

    <!-- Rango -->
    <input type="range" min="0" max="100">

    <!-- Archivo -->
    <input type="file" accept="image/*">

    <!-- Casillas de verificación -->
    <input type="checkbox" id="terminos">
    <label for="terminos">Acepto los términos</label>

    <!-- Botones de radio -->
    <input type="radio" name="genero" value="m" id="masculino">
    <label for="masculino">Masculino</label>
    <input type="radio" name="genero" value="f" id="femenino">
    <label for="femenino">Femenino</label>
</form>
```

## 2.4 Atributos de input
Los inputs pueden tener varios atributos que modifican su comportamiento:

```html
<form>
    <!-- Required - Campo obligatorio -->
    <input type="text" required>

    <!-- Readonly - Solo lectura -->
    <input type="text" readonly value="No se puede modificar">

    <!-- Disabled - Deshabilitado -->
    <input type="text" disabled>

    <!-- Pattern - Patrón de validación -->
    <input type="text" pattern="[A-Za-z]{3}" title="Tres letras">

    <!-- Maxlength - Longitud máxima -->
    <input type="text" maxlength="10">

    <!-- Min y Max - Valores mínimo y máximo -->
    <input type="number" min="0" max="100">

    <!-- Placeholder - Texto de ejemplo -->
    <input type="text" placeholder="Escribe aquí...">

    <!-- Autocomplete -->
    <input type="text" autocomplete="on">

    <!-- Multiple - Permite múltiples valores -->
    <input type="file" multiple>
</form>
```

