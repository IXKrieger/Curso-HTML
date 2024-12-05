Ejercicio 2: Tablas y Formularios
## Ejercicio 2: Tablas y Formularios

**Enunciado:** Crea una página de registro que contenga:

-   Una tabla con información de precios
-   Un formulario de registro con:
    -   Campos para nombre y apellido
    -   Email
    -   Contraseña
    -   Fecha de nacimiento
    -   Género
    -   País de residencia
    -   Botón de envío

**Código de ejemplo:**

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Registro</title>
</head>
<body>
    <h1>Tabla de Precios</h1>
    <table border="1">
        <thead>
            <tr>
                <th>Producto</th>
                <th>Precio</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>Producto 1</td>
                <td>$10</td>
            </tr>
            <tr>
                <td>Producto 2</td>
                <td>$20</td>
            </tr>
        </tbody>
    </table>
    <h1>Formulario de Registro</h1>
    <form>
        <label for="nombre">Nombre:</label>
        <input type="text" id="nombre" name="nombre" required><br>
        <label for="apellido">Apellido:</label>
        <input type="text" id="apellido" name="apellido" required><br>
        <label for="email">Email:</label>
        <input type="email" id="email" name="email" required><br>
        <label for="password">Contraseña:</label>
        <input type="password" id="password" name="password" required><br>
        <label for="dob">Fecha de Nacimiento:</label>
        <input type="date" id="dob" name="dob"><br>
        <label for="genero">Género:</label>
        <select id="genero" name="genero">
            <option value="masculino">Masculino</option>
            <option value="femenino">Femenino</option>
            <option value="otro">Otro</option>
        </select><br>
        <label for="pais">País de Residencia:</label>
        <select id="pais" name="pais">
            <option value="mexico">México</option>
            <option value="españa">España</option>
            <option value="argentina">Argentina</option>
        </select><br>
        <button type="submit">Enviar</button>
    </form>
</body>
</html>