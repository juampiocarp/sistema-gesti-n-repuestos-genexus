# Reglas de negocio y procesos documentados

## 1. Alcance y forma de lectura

Este documento organiza las reglas y los procesos que se desprenden del trabajo final y su manual de usuario.

Se distinguen tres tipos de información:

- **Regla o requisito expresamente documentado:** aparece en los módulos, requerimientos o manual del trabajo.
- **Flujo resumido:** secuencia textual que ordena los pasos que el manual describe; no agrega decisiones nuevas.
- **Punto no especificado o inconsistente:** aspecto que el documento no define o presenta de distintas maneras.

El trabajo describe tanto funcionalidades propuestas como pantallas y operaciones explicadas en el manual. Por eso, lo aquí documentado no debe interpretarse automáticamente como evidencia de que todas las reglas hayan sido implementadas y probadas en la versión final.

## 2. Reglas de negocio expresamente documentadas

### RN-01 — Identificación del producto
Cada producto cuenta con un identificador y se asocia a una categoría y a un proveedor. La información de producto incluye nombre, precio, stock y descripción.

**Fuente:** requerimientos funcionales, página 29; modelo de tablas, páginas 46–48.

### RN-02 — Imagen de producto opcional
El sistema contempla asociar una imagen a un producto. El manual indica que, al registrar un producto, la imagen puede agregarse si se desea.

**Fuente:** páginas 24 y 29; manual, páginas 65–66.

### RN-03 — Alta de producto y datos previos
El manual indica expresamente que la categoría debe estar registrada previamente. También señala que, si el stock inicial es inexistente, debe quedar en cero. El producto se vincula con un proveedor, pero ese pasaje no detalla de forma explícita una condición de alta previa del proveedor.

**Fuente:** manual, páginas 65–66.

### RN-04 — Búsqueda y consulta de productos
Los productos pueden buscarse por código, nombre o palabra clave. El documento también contempla filtros por categoría, proveedor y rango de precios, entre otros.

**Fuente:** páginas 24 y 29.

### RN-05 — Actualización de stock por ventas
El requerimiento establece que el stock debe actualizarse automáticamente después de cada venta. El caso de uso 9 también indica que, al registrar una venta, el sistema descuenta el stock.

**Fuente:** páginas 25 y 30; caso de uso 9, página 39.

### RN-06 — Actualización de stock por ingreso de mercadería
El requerimiento de compras establece que el stock se actualiza automáticamente con cada ingreso de mercadería. El caso de uso 5 indica que, cuando se registra la recepción de mercadería, el sistema actualiza el stock.

**Fuente:** páginas 25 y 30; caso de uso 5, página 39.

### RN-07 — Datos de una venta
La venta debe registrar cliente, productos, cantidades, precios, forma y método de pago. El módulo contempla clientes ocasionales o con cuenta corriente y la posibilidad de aplicar descuentos.

**Fuente:** páginas 24 y 29; modelo de tablas, páginas 44–46.

### RN-08 — Comprobante de venta
El sistema contempla emitir un ticket o comprobante. El manual indica que, luego de confirmar una venta, se redirige a una pantalla para visualizar e imprimir la factura.

**Fuente:** páginas 25 y 29; manual, páginas 64–65.

### RN-09 — Registro de compras
La compra se asocia a un usuario y a un proveedor, e incluye fecha, método de pago y detalle de productos, cantidades y precios unitarios.

**Fuente:** modelo de tablas, páginas 49–51; manual, página 63.

### RN-10 — Pedidos a proveedores por falta de stock
El módulo de pedidos contempla registrar pedidos a proveedores cuando no hay stock disponible.

**Fuente:** páginas 26 y 30.

### RN-11 — Seguimiento de pedidos de clientes
El sistema contempla registrar pedidos de clientes como reserva de stock o encargo, consultar su estado y mantener un historial.

**Fuente:** página 26.

### RN-12 — Cuentas corrientes de clientes
El sistema contempla registrar deuda y pagos de clientes, permitir pagos parciales o totales, actualizar el saldo y consultar movimientos históricos.

**Fuente:** páginas 26 y 31.

### RN-13 — Cuentas corrientes de proveedores
El sistema contempla controlar compras, pagos y saldo de cada proveedor, así como consultar movimientos e informes.

**Fuente:** páginas 25, 26 y 31; estructura de consultas, páginas 55–56.

### RN-14 — Acceso según tipo de usuario
El documento plantea perfiles con distintos permisos. El manual diferencia opciones disponibles para Gerente y Vendedor. El apartado de requerimientos utiliza los nombres Administrador y Vendedor.

**Fuente:** páginas 27 y 31; manual, páginas 62 y 69.

### RN-15 — Confirmación de operaciones críticas
El requerimiento no funcional establece que los procesos críticos —venta, actualización de stock y registro de pagos— deben contar con confirmación previa a su ejecución.

**Fuente:** página 34.

## 3. Procesos operativos resumidos

Los procesos siguientes ordenan la información que aparece en módulos y manual. Cuando un paso no está definido por la fuente, se indica como pendiente de especificación.

### 3.1 Alta de producto

**Actor descrito en el manual:** Gerente.

1. Ingresar a la opción de alta de producto.
2. Cargar nombre del producto.
3. Ingresar el ID del proveedor y el ID de la categoría. El manual aclara que la categoría debe estar registrada previamente; no especifica de forma expresa una validación equivalente para el proveedor.
4. Definir el stock inicial; el manual indica cero cuando no existe stock inicial.
5. Cargar el precio de venta.
6. Agregar una imagen si se desea.
7. Confirmar el registro.

**Resultado documentado:** el producto queda registrado para su utilización en compras y ventas.

**Fuente:** manual, páginas 65–66.

### 3.2 Registro de compra e ingreso de mercadería

**Actor descrito en el manual:** Gerente.

1. Consultar el historial de compras.
2. Seleccionar la opción de insertar una compra.
3. Ingresar usuario, proveedor, fecha de compra, costo, producto y cantidad.
4. Seleccionar las opciones disponibles en los campos desplegables.
5. Confirmar el registro.

**Regla relacionada:** el requerimiento establece que el stock se actualiza automáticamente con cada ingreso de mercadería. El caso de uso de recepción indica que el stock se actualiza cuando se informa que la mercadería fue recibida.

**Pendiente de especificación:** el manual no explica con detalle si la confirmación de la compra y la confirmación de recepción son una única operación o dos momentos distintos.

**Fuente:** manual, página 63; requerimiento de compras, página 30; caso de uso 5, página 39.

### 3.3 Registro de venta

**Actores descritos en el manual:** Gerente y Vendedor, con distintas opciones según el rol.

1. Acceder a la opción de registrar una venta.
2. Ingresar el usuario y el cliente.
3. Indicar la fecha de venta.
4. Seleccionar método y forma de pago, e indicar cuotas cuando corresponda.
5. Informar el descuento, si corresponde.
6. Seleccionar los productos y las cantidades.
7. Confirmar la operación.
8. Visualizar e imprimir el comprobante o factura.

**Regla relacionada:** el requerimiento establece que el stock se descuenta automáticamente después de cada venta.

**Fuente:** páginas 24–25 y 29–30; manual, páginas 64–65.

### 3.4 Registro de pedido de cliente

El módulo contempla registrar un pedido como reserva de stock o encargo, asociarlo a producto y cantidad, consultar su estado y mantener un historial.

**Estados documentados con diferencias:**
- En la descripción del módulo (página 26): pendiente, entregado y en preparación.
- En requerimientos funcionales (página 30): pendiente, entregado y cancelado.

**Pendiente de especificación:** confirmar el catálogo definitivo de estados y definir qué ocurre con el stock reservado cuando un pedido se entrega o cancela.

**Fuente:** páginas 26 y 30.

### 3.5 Pedido a proveedor

El módulo establece que se registran pedidos a proveedores cuando no hay stock. También contempla asociar el pedido con producto y cantidad, y consultar el historial de pedidos emitidos y recibidos.

**Pendiente de especificación:** no se detallan estados del pedido al proveedor, aprobación, recepción parcial ni tratamiento de diferencias entre cantidad pedida y recibida.

**Fuente:** páginas 26 y 30.

### 3.6 Cuenta corriente de cliente

El sistema contempla registrar cuentas corrientes, seguir deudas y pagos, aceptar pagos parciales o totales, actualizar el saldo y emitir recibos o resúmenes.

**Pendiente de especificación:** no se detallan límites de crédito, vencimientos, intereses, asignación de un pago a una o varias ventas ni reglas de imputación.

**Fuente:** páginas 26 y 31.

### 3.7 Cuenta corriente de proveedor

El sistema contempla relacionar las compras y los pagos realizados a proveedores para consultar movimientos y saldo.

**Pendiente de especificación:** no se describe el procedimiento detallado para imputar pagos a facturas o compras específicas ni el tratamiento de pagos parciales.

**Fuente:** páginas 25–26 y 31; consultas descriptas en páginas 55–56.

## 4. Reglas y decisiones que requieren validación

El trabajo no permite cerrar de forma inequívoca los siguientes puntos:

1. **Estados de pedidos de clientes:** se documentan dos conjuntos distintos de estados.
2. **Reserva de stock:** se menciona reserva o ajuste provisional, pero no se explica exactamente cuándo se descuenta el stock disponible ni cuándo se libera una reserva.
3. **Recepción de compras:** no se aclara si el registro de la compra y la recepción de mercadería son la misma operación.
4. **Stock negativo:** no se especifica qué debe ocurrir si una venta supera el stock disponible.
5. **Cancelación y modificación de ventas:** el manual contempla modificar o eliminar registros, pero no explica cómo se revierten movimientos de stock o pagos.
6. **Devoluciones:** no se define el tratamiento de devoluciones de clientes ni devoluciones a proveedores.
7. **Pagos parciales:** se contemplan en cuentas corrientes de clientes, pero no se detallan reglas de imputación o conciliación.
8. **Descuentos:** se menciona su aplicación, pero no se definen prioridades, acumulación, autorizaciones ni reglas de redondeo.
9. **Roles:** se usan los términos Gerente/Administrador y Vendedor en distintas partes; se requiere confirmar si Gerente equivale a Administrador.
10. **Confirmación de operaciones:** se exige confirmación previa para operaciones críticas, pero no se documenta el comportamiento ante cancelación de la confirmación o errores durante el registro.

Estos puntos se presentan como **pendientes de definición**, no como fallas confirmadas de la aplicación.

## 5. Relación con otros documentos del portfolio

- [Requerimientos funcionales y no funcionales](requerimientos-funcionales-no-funcionales.md): capacidades y condiciones que el sistema debía cumplir.
- [Casos de uso](casos-de-uso.md): interacciones entre actores y sistema.
- [Alcance funcional](alcance-funcional.md): módulos y capacidades generales.
- [Modelo de datos](modelo-de-datos.md): entidades, atributos y relaciones descriptas.

## 6. Fuente

Trabajo Final de Carrera — Tecnicatura Superior en Desarrollo de Software, Instituto Superior Brigadier López. Se consultaron principalmente las páginas 24–34, 44–56 y 62–69.
