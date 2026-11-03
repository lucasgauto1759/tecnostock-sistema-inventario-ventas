# Historias de Usuario - TecnoStock

Las historias se formalizan a partir de las funciones del Sistema de Gestión de Inventario y Ventas definidas en las entregas anteriores.

## US-01 - Registro de ventas
**Como** vendedor/a, **quiero** registrar las ventas con los productos y cantidades correspondientes, **para** mantener un historial centralizado de las operaciones.

Criterios de aceptación:
- Número único y fecha/hora de la operación.
- Productos y cantidades incluidos en el detalle.
- Total de la venta igual a la suma de subtotales.
- Validación de stock antes de confirmar.

## US-02 - Actualización automática del inventario
**Como** responsable de Depósito, **quiero** que el stock se actualice automáticamente después de confirmar una venta, **para** conocer la disponibilidad real y reducir errores de inventario.

Criterios de aceptación:
- Descuento de las cantidades vendidas al confirmarse la operación.
- Prohibición de stock negativo.
- Actualización visible en un máximo de 3 segundos.
- Registro de incidencia si falla la actualización.

## US-03 - Consulta de información para control
**Como** responsable de Administración, **quiero** consultar la información de ventas e inventario, **para** realizar controles y apoyar la toma de decisiones.

Criterios de aceptación:
- Consulta por fecha y producto.
- Totales consistentes con las ventas registradas.
- Consulta de stock actual.
- Acceso restringido a usuarios autorizados.

## Estados iniciales sugeridos para el tablero

| ID | Estado | Alcance del estado |
|---|---|---|
| US-01 | Listo | La definición y los criterios de aceptación están documentados. No implica que el módulo esté programado. |
| US-02 | En Progreso | Se está completando la regla de actualización y su manejo de errores. |
| US-03 | Por Hacer | Falta detallar los filtros y la presentación de los informes. |
