# 5. Vista de Bloques de Construcción

## Vista de Contenedores (C2)
El siguiente diagrama detalla la estructura interna de alto nivel del sistema ERP y cómo se distribuyen las responsabilidades entre los distintos contenedores ejecutable/desplegables.

![Diagrama de Contenedores](../docs/images/Diagrama%203.png)

### Responsabilidad de los Contenedores
* **Single Page Application (React):** Interfaz de usuario ejecutable en el navegador que consume la API del backend.
* **API Backend (Spring Boot):** Contiene la lógica de negocio del módulo de compras, procesamiento de datos y autenticación/autorización.
* **Base de Datos (PostgreSQL):** Almacena de manera persistente los datos transaccionales de compras, inventario y proveedores.