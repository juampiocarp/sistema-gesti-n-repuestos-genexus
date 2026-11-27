# Casos de uso e interacciones del sistema

## Alcance y fuente

Este documento organiza las 15 funcionalidades que el trabajo final presenta en las páginas 38 a 41. Para cada una se conserva:

- El actor que aparece en el diagrama.
- La acción o solicitud indicada como entrada (E).
- La respuesta del sistema indicada como resultado (R).

El documento original representa estas interacciones mediante diagramas E1/R1 a E15/R15. No desarrolla flujos alternativos, precondiciones, reglas de validación ni excepciones para todos los casos. Por ese motivo, esos elementos no se completan por inferencia en este portfolio.

## Resumen de actores

| Actor | Responsabilidad representada |
|---|---|
| Vendedor | Mantiene datos de proveedores y clientes, registra pedidos, busca productos y realiza ventas. |
| Dueño | Registra ingresos y movimientos de mercadería, controla stock, pagos, ventas, compras e informes. |

El actor **Proveedores** aparece en el diagrama de contexto de la página 37 y no se agrega como actor a los casos 1–15 de las páginas 38–41.

## Catálogo de casos de uso

| N.º | Caso de uso | Actor | Entrada / acción (E) | Respuesta del sistema (R) |
|---:|---|---|---|---|
| 1 | Actualizar catálogo de proveedores | Vendedor | El usuario carga o edita datos de proveedores. | El sistema guarda y actualiza el catálogo de proveedores. |
| 2 | Actualizar clientes | Vendedor | El usuario carga o edita datos de clientes. | El sistema actualiza la base de datos de clientes. |
| 3 | Agregar imagen del producto al stock | Vendedor | El usuario sube una imagen al registrar o modificar un producto. | El sistema almacena y vincula la imagen al producto. |
| 4 | Registrar pedido a proveedor | Vendedor | El usuario ingresa un pedido a un proveedor. | El sistema guarda el pedido y lo asocia al proveedor. |
| 5 | Registrar ingreso de mercadería | Dueño | El usuario indica que recibió la mercadería. | El sistema actualiza el stock con la mercadería ingresada. |
| 6 | Controlar stock | Dueño | El usuario consulta o modifica el inventario. | El sistema muestra o actualiza el stock disponible. |
| 7 | Buscar productos por código, nombre o palabra clave | Vendedor | El usuario introduce un criterio de búsqueda. | El sistema muestra los productos coincidentes. |
| 8 | Registrar pedidos de clientes | Vendedor | El usuario ingresa un nuevo pedido de cliente. | El sistema guarda el pedido y ajusta el stock provisional. |
| 9 | Registrar ventas | Vendedor | El usuario realiza una venta. | El sistema registra la venta y descuenta el stock. |
| 10 | Registrar entrada/salida de repuestos | Dueño | El usuario registra el movimiento de repuestos. | El sistema actualiza el stock de repuestos. |
| 11 | Registrar pago a proveedores | Dueño | El usuario ingresa un pago realizado. | El sistema guarda el pago y lo vincula al proveedor. |
| 12 | Controlar ventas en dinero | Dueño | El usuario consulta las ventas en dinero. | El sistema muestra el total de ventas monetarias. |
| 13 | Controlar ventas de mercaderías | Dueño | El usuario consulta las ventas por producto. | El sistema muestra las cantidades vendidas por ítem. |
| 14 | Controlar compras | Dueño | El usuario consulta o gestiona compras realizadas. | El sistema muestra o permite modificar compras. |
| 15 | Generar informes | Dueño | El usuario solicita un informe específico. | El sistema genera y muestra el informe correspondiente. |

## Detalle de los casos de uso

Los siguientes detalles amplían únicamente la interacción E/R que el documento original hace explícita.

### CU-01 — Actualizar catálogo de proveedores

- **Actor:** Vendedor.
- **Acción:** carga o edita datos de proveedores.
- **Resultado esperado documentado:** el sistema guarda la información y actualiza el catálogo de proveedores.
- **Referencia:** página 38, E1/R1.

### CU-02 — Actualizar clientes

- **Actor:** Vendedor.
- **Acción:** carga o edita datos de clientes.
- **Resultado esperado documentado:** el sistema actualiza la base de datos de clientes.
- **Referencia:** página 38, E2/R2.

### CU-03 — Agregar imagen del producto al stock

- **Actor:** Vendedor.
- **Acción:** sube una imagen al registrar o modificar un producto.
- **Resultado esperado documentado:** el sistema almacena la imagen y la vincula al producto.
- **Referencia:** página 38, E3/R3.

### CU-04 — Registrar pedido a proveedor

- **Actor:** Vendedor.
- **Acción:** ingresa un pedido a un proveedor.
- **Resultado esperado documentado:** el sistema guarda el pedido y lo asocia al proveedor.
- **Referencia:** página 38, E4/R4.

### CU-05 — Registrar ingreso de mercadería

- **Actor:** Dueño.
- **Acción:** indica que recibió la mercadería.
- **Resultado esperado documentado:** el sistema actualiza el stock con la mercadería ingresada.
- **Referencia:** página 39, E5/R5.

### CU-06 — Controlar stock

- **Actor:** Dueño.
- **Acción:** consulta o modifica el inventario.
- **Resultado esperado documentado:** el sistema muestra o actualiza el stock disponible.
- **Referencia:** página 39, E6/R6.

### CU-07 — Buscar productos por código, nombre o palabra clave

- **Actor:** Vendedor.
- **Acción:** introduce un criterio de búsqueda.
- **Resultado esperado documentado:** el sistema muestra los productos coincidentes.
- **Referencia:** página 39, E7/R7.

### CU-08 — Registrar pedidos de clientes

- **Actor:** Vendedor.
- **Acción:** ingresa un nuevo pedido de cliente.
- **Resultado esperado documentado:** el sistema guarda el pedido y ajusta el stock provisional.
- **Referencia:** página 39, E8/R8.

### CU-09 — Registrar ventas

- **Actor:** Vendedor.
- **Acción:** realiza una venta.
- **Resultado esperado documentado:** el sistema registra la venta y descuenta el stock.
- **Referencia:** página 39, E9/R9.

### CU-10 — Registrar entrada/salida de repuestos

- **Actor:** Dueño.
- **Acción:** registra el movimiento de repuestos.
- **Resultado esperado documentado:** el sistema actualiza el stock de repuestos.
- **Referencia:** página 40, E10/R10.

### CU-11 — Registrar pago a proveedores

- **Actor:** Dueño.
- **Acción:** ingresa un pago realizado.
- **Resultado esperado documentado:** el sistema guarda el pago y lo vincula al proveedor.
- **Referencia:** página 40, E11/R11.

### CU-12 — Controlar ventas en dinero

- **Actor:** Dueño.
- **Acción:** consulta las ventas en dinero.
- **Resultado esperado documentado:** el sistema muestra el total de ventas monetarias.
- **Referencia:** página 40, E12/R12.

### CU-13 — Controlar ventas de mercaderías

- **Actor:** Dueño.
- **Acción:** consulta las ventas por producto.
- **Resultado esperado documentado:** el sistema muestra las cantidades vendidas por ítem.
- **Referencia:** página 40, E13/R13.

### CU-14 — Controlar compras

- **Actor:** Dueño.
- **Acción:** consulta o gestiona compras realizadas.
- **Resultado esperado documentado:** el sistema muestra o permite modificar compras.
- **Referencia:** página 41, E14/R14.

### CU-15 — Generar informes

- **Actor:** Dueño.
- **Acción:** solicita un informe específico.
- **Resultado esperado documentado:** el sistema genera y muestra el informe correspondiente.

El diagrama menciona como ejemplos de informes: cuenta corriente de clientes y proveedores, listado de cajas y productos actualizados.

- **Referencia:** página 41, E15/R15.

## Límites de esta documentación

- Los nombres, actores y respuestas se transcriben de los diagramas del trabajo final.
- No se agregan flujos alternativos, validaciones ni reglas de negocio que no estén descritos en esas páginas.
- Las descripciones son una organización textual de los diagramas, no una especificación funcional nueva ni una afirmación de que todas las funciones fueron desplegadas en producción.

## Fuente

Trabajo Final de Carrera — Tecnicatura Superior en Desarrollo de Software, Instituto Superior Brigadier López, páginas 38–41.
