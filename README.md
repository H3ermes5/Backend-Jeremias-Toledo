### Servidor Node.js con Express - Gestión de Productos y Carritos

Este proyecto consiste en el desarrollo de un servidor utilizando _Node.js_ y _Express_ para gestionar productos y carritos de compra. Los endpoints están implementados con el router de Express y se utiliza el sistema de archivos para la persistencia de datos.

#### Especificaciones del Proyecto

1. **Rutas de Productos**:

   - `POST /`: Agrega un nuevo producto con los siguientes campos:
     - id (autogenerado)
     - title
     - description
     - code
     - price
     - status (por defecto: true)
     - stock
     - category
     - thumbnails (array de strings, opcional)
   - `PUT /:pid`: Actualiza un producto existente.
   - `DELETE /:pid`: Elimina un producto por su id.

2. **Rutas de Carritos**:
   - `POST /`: Crea un nuevo carrito con una estructura definida.
   - `GET /:cid`: Lista los productos de un carrito.
   - `POST /:cid/product/:pid`: Agrega un producto al carrito con su cantidad correspondiente.

#### Persistencia de Datos

La información se guarda utilizando el sistema de archivos, con archivos "productos.json" y "carrito.json" para respaldar los datos.

#### Instrucciones de Uso

1. Clona el repositorio desde GitHub.
2. Instala las dependencias con `npm install`.
3. Ejecuta el servidor con `npm start`.
4. Utiliza Postman u otro cliente para probar las rutas especificadas.
5. Consulta el archivo `README.md` para instrucciones detalladas sobre el uso del servidor.

#### Requisitos y Sugerencias

- Se utiliza `express.json()` para el manejo de datos en formato JSON.
- No es necesario implementar Multer.
