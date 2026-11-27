# Análisis y modelado

## Relevamiento

El trabajo comenzó con una entrevista al responsable del comercio para conocer:

- La organización y los roles de trabajo.
- Cómo se registraban las ventas y los cobros.
- Cómo se controlaba el inventario.
- Cómo se realizaban pedidos y compras a proveedores.
- Qué información necesitaba consultar cada tipo de usuario.
- Qué expectativas existían sobre facilidad de uso, acceso y seguridad.

Los datos identificatorios del comercio y las respuestas que puedan revelar información privada fueron omitidos de esta versión pública.

## Modelado funcional

El trabajo final incluye un diagrama de contexto y diagramas de casos de uso para representar las interacciones entre actores y funcionalidades del sistema.

- [Diagramas y pantallas](diagramas-y-pantallas.md): reúne las versiones visuales y las fuentes editables de los dos diagramas publicados.
- [Casos de uso e interacciones](casos-de-uso.md): transcribe las 15 interacciones E/R documentadas en las páginas 38 a 41.

Las representaciones SVG y Mermaid del repositorio son transcripciones preparadas para el portfolio; no son exportaciones originales de GeneXus.

## Estructura de datos

El trabajo incluye especificaciones tabulares de entidades, atributos, tipos de datos, claves primarias y relaciones mediante claves foráneas. Entre las entidades documentadas se encuentran:

- Clientes.
- Usuarios.
- Proveedores.
- Productos.
- Categorías.
- Compras y detalles de compra.
- Ventas y detalles de venta.
- Imágenes de productos.
- Descuentos.

La documentación original describe atributos como identificadores, nombres, datos de contacto, stock, precios, fechas y referencias entre registros. No se publican datos reales ni registros de la base de datos.

## Modelo entidad-relación

- [Modelo de datos y diagrama entidad-relación](modelo-de-datos.md): presenta una reconstrucción lógica del modelo a partir de las tablas y claves descritas en las páginas 42 a 51.
- [Fuente Mermaid editable](../diagrams/modelo-entidad-relacion.mmd).

Esta reconstrucción no debe interpretarse como el diagrama original del equipo ni como una extracción del esquema físico de GeneXus. Los tipos de datos y las cardinalidades que no están definidos en la fuente se señalan como tales.

## Consideraciones

El material publicado resume la documentación académica y conserva las ambigüedades que requieren validación. No se agregan datos privados del comercio ni se afirma que cada requisito o funcionalidad haya sido implementado y probado.
