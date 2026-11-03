# Indicadores y estándares de control - TecnoStock

Los indicadores se proponen para auditar el funcionamiento del Sistema de Gestión de Inventario y Ventas. Las metas de 100 %, 80 % y 3 segundos retoman los objetivos cuantitativos de la Entrega 2. Los restantes estándares son criterios técnicos propuestos para controlar la consistencia de la información.

| Indicador | Fórmula / método | Estándar | Frecuencia | Responsable |
|---|---|---|---|---|
| Registro de ventas | (Ventas registradas en el sistema / total de ventas realizadas) × 100 | 100 % de las ventas registradas | Diario | Ventas / Administración |
| Tiempo de actualización del stock | Tiempo entre la confirmación de la venta y la disponibilidad del nuevo stock en consulta | Máximo 3 segundos | Por operación y en pruebas de versión | Sistemas |
| Reducción de errores de inventario | ((Errores de referencia inicial - errores posteriores) / errores de referencia inicial) × 100 | Reducción mínima del 80 % frente al procedimiento anterior | Semanal | Depósito / Administración |
| Integridad de relaciones | (Detalles de venta con id_venta e id_producto válidos / total de detalles) × 100 | 100 % | Antes de cada versión y control semanal | Sistemas |
| Prevención de stock negativo | Cantidad de operaciones que dejan stock negativo | 0 operaciones con stock negativo | Por operación | Sistema / Depósito |

## Procedimiento de control

1. **Control diario:** Ventas revisa que las operaciones del día estén registradas; Administración compara la cantidad de operaciones con los comprobantes o registros disponibles.
2. **Control semanal:** Depósito contrasta una muestra de existencias físicas con el stock del sistema e informa diferencias.
3. **Control técnico por versión:** Sistemas ejecuta pruebas de registro, actualización, validación de stock e integridad de relaciones antes de aprobar cambios.
4. **Revisión de resultados:** Administración consolida los indicadores y comunica desvíos a Dirección/Gerencia.

## Tratamiento de desvíos

- Si una venta no queda registrada, se revisa la operación y se corrige el registro antes de considerarla finalizada.
- Si el stock tarda más de 3 segundos en actualizarse, Sistemas registra la incidencia, identifica la causa y vuelve a probar.
- Si aparecen diferencias de inventario, Depósito realiza un recuento y Administración registra el desvío para su análisis.
- Si una relación de detalle no referencia una venta o producto válido, la versión no se considera apta hasta corregir la integridad de los datos.

**Nota sobre la línea de base:** antes de calcular la reducción del 80 %, se debe registrar la cantidad de errores del procedimiento anterior. Si la línea de base es cero, el porcentaje no se calcula; se informa que no se registraron errores iniciales y se mantiene el control de incidencias.
