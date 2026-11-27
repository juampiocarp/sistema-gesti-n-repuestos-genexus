# Requerimientos funcionales y no funcionales

## Fuente y alcance

Este documento organiza los requerimientos del apartado **“Requerimientos del sistema”** del trabajo final, páginas 29 a 34. Se complementa con las descripciones de módulos de las páginas 24 a 28 cuando ayudan a contextualizar una función.

El documento académico distingue:

- **Requerimientos funcionales (RF):** operaciones y servicios que el sistema debe ofrecer.
- **Requerimientos no funcionales (RNF):** condiciones de calidad, seguridad, rendimiento, compatibilidad y disponibilidad que el sistema debe cumplir.

Los enunciados se agrupan y numeran para facilitar su lectura. La numeración RF/RNF es una organización del portfolio; no aparece con esos identificadores en el documento original.

> **Importante:** estos puntos expresan el alcance y las condiciones requeridas/propuestas en el trabajo académico. No constituyen por sí solos evidencia de que cada requisito haya sido implementado, probado o desplegado en el sistema final.

---

# 1. Requerimientos funcionales

## 1.1 Gestión de productos

| ID | Requerimiento |
|---|---|
| RF-01 | Permitir la búsqueda de productos por código, nombre o palabra clave. |
| RF-02 | Registrar nuevos productos con nombre, precio, proveedor, categoría, stock y descripción. |
| RF-03 | Permitir modificar o eliminar productos existentes. |
| RF-04 | Permitir asociar una imagen a cada producto del stock (opcional). |
| RF-05 | Permitir actualizar precios, categorías y descripciones. |
| RF-06 | Permitir importar datos desde archivos Excel para facilitar la carga inicial del catálogo. |

## 1.2 Gestión de ventas

| ID | Requerimiento |
|---|---|
| RF-07 | Registrar ventas con los datos correspondientes al cliente, productos vendidos, cantidades, precios, forma de pago y método de pago. |
| RF-08 | Controlar ventas realizadas en efectivo, con tarjeta, transferencia u otros medios. |
| RF-09 | Permitir emitir tickets o comprobantes de venta. |
| RF-10 | Controlar y actualizar automáticamente el stock después de cada venta. |
| RF-11 | Permitir consultar el historial de ventas por cliente, producto o rango de fechas. |
| RF-12 | Emitir un listado diario de caja con los totales de ventas realizadas. |

## 1.3 Gestión de compras y proveedores

| ID | Requerimiento |
|---|---|
| RF-13 | Registrar compras a proveedores, incluyendo producto, cantidad, precio y fecha. |
| RF-14 | Actualizar automáticamente el stock con cada ingreso de mercadería. |
| RF-15 | Registrar pagos a proveedores, incluyendo método de pago y detalle de la operación. |
| RF-16 | Generar un historial de compras filtrado por proveedor, producto o rango de fechas. |
| RF-17 | Mantener actualizada la lista de proveedores con nombre, dirección, teléfono y correo electrónico. |

## 1.4 Gestión de pedidos

| ID | Requerimiento |
|---|---|
| RF-18 | Registrar pedidos de clientes (encargos) y su estado. En el apartado formal de requerimientos se mencionan los estados pendiente, entregado y cancelado. |
| RF-19 | Registrar pedidos a proveedores cuando no haya stock disponible. |
| RF-20 | Permitir consultar el historial de pedidos realizados y recibidos. |
| RF-21 | Permitir actualizar el estado de los pedidos. |

## 1.5 Gestión de cuentas corrientes

| ID | Requerimiento |
|---|---|
| RF-22 | Registrar cuentas corrientes de clientes, con seguimiento de deuda y pagos. |
| RF-23 | Registrar pagos a cuenta corriente y actualizar automáticamente el saldo. |
| RF-24 | Permitir consultar movimientos históricos por cliente o proveedor. |
| RF-25 | Emitir recibos o resúmenes de cuenta corriente. |
| RF-26 | Controlar cuentas corrientes con proveedores, incluyendo compras, pagos y saldo. |

## 1.6 Gestión de usuarios y seguridad

| ID | Requerimiento |
|---|---|
| RF-27 | Permitir crear, editar y eliminar usuarios del sistema. |
| RF-28 | Definir niveles de acceso según el tipo de usuario (Administrador o Vendedor). |
| RF-29 | Validar el acceso mediante usuario y contraseña. |
| RF-30 | Solicitar la renovación programada de contraseñas cada seis meses. |
| RF-31 | Registrar las actividades realizadas por cada usuario. |
| RF-32 | Permitir hasta cuatro usuarios activos: un administrador y tres vendedores. |
| RF-33 | Exigir contraseñas de al menos ocho caracteres, con renovación cada seis meses. |

**Nota sobre RF-30, RF-33 y RNF-09:** el trabajo presenta la renovación semestral como caducidad programada, como parte de la política de contraseña mínima y nuevamente dentro de seguridad no funcional. Se conservan las apariciones porque están en el documento original; conceptualmente describen una misma política y podrían consolidarse en una especificación posterior.

## 1.7 Reportes e informes

| ID | Requerimiento |
|---|---|
| RF-34 | Generar reportes de ventas por fecha, cliente o producto. |
| RF-35 | Generar reportes de compras por proveedor o fecha. |
| RF-36 | Emitir un listado de productos con stock bajo. |
| RF-37 | Generar informes de cuentas corrientes de clientes y proveedores. |
| RF-38 | Permitir exportar e imprimir reportes en formato digital o papel. |

## 1.8 Configuración y mantenimiento

| ID | Requerimiento |
|---|---|
| RF-39 | Configurar copias de seguridad automáticas (backups). |
| RF-40 | Actualizar categorías, proveedores, productos y listas de precios. |
| RF-41 | Permitir la importación y exportación de datos para mantener el sistema actualizado. |
| RF-42 | Contar con una opción de configuración de acceso remoto para permitir el uso fuera del local comercial. |

---

# 2. Requerimientos no funcionales

## 2.1 Usabilidad

| ID | Requerimiento |
|---|---|
| RNF-01 | El sistema debe ser fácil de usar, intuitivo y accesible para usuarios con conocimientos básicos de informática. |
| RNF-02 | La interfaz debe ser clara, ordenada y utilizar lenguaje comprensible. |
| RNF-03 | Se debe priorizar la rapidez de acceso a las operaciones más comunes: ventas, stock y búsqueda de productos. |

## 2.2 Mantenibilidad

| ID | Requerimiento |
|---|---|
| RNF-04 | Permitir actualizar versiones y módulos sin comprometer los datos existentes. |
| RNF-05 | Permitir agregar o eliminar usuarios y modificar permisos sin afectar la estabilidad general. |
| RNF-06 | Contemplar la posibilidad de restaurar datos desde copias de seguridad. |

## 2.3 Seguridad

| ID | Requerimiento |
|---|---|
| RNF-07 | Restringir el acceso al sistema mediante usuarios y contraseñas. |
| RNF-08 | Asignar a cada usuario permisos acordes a su rol. |
| RNF-09 | Solicitar la renovación obligatoria de contraseñas cada seis meses. |
| RNF-10 | Realizar copias de seguridad de forma manual o programada para evitar pérdida de información. |
| RNF-11 | Proteger los datos contra accesos no autorizados o manipulaciones indebidas. |

## 2.4 Rendimiento

| ID | Requerimiento |
|---|---|
| RNF-12 | Responder de manera fluida a las consultas y operaciones más frecuentes. |
| RNF-13 | Ejecutar las búsquedas de productos en menos de dos segundos, incluso con grandes volúmenes de datos. |
| RNF-14 | Optimizar el acceso a la base de datos para mantener tiempos de carga mínimos. |

## 2.5 Portabilidad y acceso remoto

| ID | Requerimiento |
|---|---|
| RNF-15 | Permitir el acceso remoto desde otro equipo, sujeto a la configuración de red del cliente. |
| RNF-16 | Ser compatible con sistemas operativos Windows. |
| RNF-17 | Funcionar correctamente en una computadora de escritorio o notebook de gama media. |

## 2.6 Confiabilidad y disponibilidad

| ID | Requerimiento |
|---|---|
| RNF-18 | Garantizar la integridad de los datos en todo momento. |
| RNF-19 | Evitar la duplicación o pérdida de información. |
| RNF-20 | Mantener una disponibilidad operativa mínima del 99 % durante el uso normal. |
| RNF-21 | Solicitar confirmación previa antes de ejecutar procesos críticos: venta, actualización de stock y registro de pagos. |

---

# 3. Observaciones y puntos a validar

Durante la organización de los requerimientos se identificaron puntos que el documento presenta de más de una manera o que necesitarían mayor precisión antes de convertirse en criterios de aceptación.

1. **Estados de pedidos:** en la descripción del módulo de pedidos (página 26) aparecen “pendiente, entregado, en preparación”; en los requerimientos funcionales (página 30) aparecen “pendiente, entregado, cancelado”. No se elige una versión como definitiva: se deja registrada la diferencia.
2. **Copias de seguridad:** configuración general (página 28) menciona backups automáticos; seguridad (página 33) habla de copias manuales o programadas. No se define una única modalidad ni una frecuencia.
3. **Usuarios y roles:** el apartado de requerimientos usa “Administrador” y “Vendedor”, mientras que el manual de usuario y algunos diagramas usan “Gerente” y “Vendedor”. La equivalencia entre Administrador y Gerente debe validarse contra la implementación.
4. **Acceso remoto:** se plantea como opción de configuración y también como requisito sujeto a la red del cliente. No se detallan protocolos, infraestructura ni condiciones técnicas.
5. **Rendimiento:** se fija un objetivo inferior a dos segundos para búsquedas, pero no se especifica volumen de datos, entorno de prueba ni método de medición.
6. **Disponibilidad:** se establece un mínimo del 99 % en uso normal, pero no se define período de medición ni ventana de mantenimiento.
7. **Criterios de aceptación:** el documento lista funciones y condiciones, pero no proporciona casos de prueba ni criterios medibles para todos los puntos.

## 4. Relación con el resto del portfolio

- Los [casos de uso](casos-de-uso.md) describen interacciones concretas entre actores y sistema.
- El [alcance funcional](alcance-funcional.md) resume los módulos y las necesidades que cubren.
- El [modelo de datos](modelo-de-datos.md) documenta las entidades, atributos y relaciones descritas en el trabajo.

Los documentos se complementan, pero no son equivalentes: los requerimientos expresan lo que el sistema debía ofrecer; los casos de uso describen interacciones; el modelo de datos organiza la información.

## Fuente

Trabajo Final de Carrera — Tecnicatura Superior en Desarrollo de Software, Instituto Superior Brigadier López, principalmente páginas 29–34. Para el punto de estados de pedidos y la descripción de módulos también se consultaron las páginas 24–28.
