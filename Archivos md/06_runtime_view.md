# 6. Vista de Ejecución (Runtime)

## Escenario Crítico: Registrar un Producto

### Flujo del Proceso
1. El Administrador de Compras rellena y envía el formulario con los datos del nuevo producto desde la interfaz gráfica (SPA).
2. La SPA envía una petición `POST /api/productos` con los datos del producto a la API Monolítica.
3. La API procesa y valida los datos recibidos.
4. Una vez validados, la API ejecuta una instrucción `INSERT INTO productos (...)` en la base de datos (DB).
5. La base de datos responde a la API confirmando que el producto fue creado y devolviendo su ID único.
6. La API responde a la SPA con un código de estado `201 Created` y los datos del nuevo producto.
7. La SPA muestra un mensaje de éxito en pantalla y actualiza la lista de productos para el usuario.

![Diagrama de Secuencia - Registrar Producto](../docs/images/Diagrama%202.png)

## Modelo de Datos (Diagrama Entidad-Relación)
A continuación se detalla el modelo entidad-relación del dominio de compras, mostrando las entidades principales (`Producto`, `Proveedor` y la tabla intermedia `Producto_Proveedor`):

![Diagrama Entidad Relación](../docs/images/Diagrama%204.png)