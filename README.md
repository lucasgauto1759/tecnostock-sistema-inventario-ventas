# TecnoStock - Sistema de Gestión de Inventario y Ventas

## Descripción

Proyecto académico de la asignatura **Organización Empresarial**, correspondiente a la Tecnicatura Universitaria en Programación a Distancia de la UTN. El caso de estudio es **TecnoStock**, una empresa ficticia dedicada a la comercialización de productos tecnológicos.

Se propone un Sistema de Gestión de Inventario y Ventas para centralizar la información de productos, registrar las ventas y actualizar automáticamente las existencias. La información puede ser consultada por Ventas, Depósito y Administración, con soporte del área de Sistemas.

## Integrante

- Lucas Gauto.

## Repositorio y tablero

- **Repositorio público:** [TecnoStock - Sistema de Gestión de Inventario y Ventas](https://github.com/lucasgauto1759/tecnostock-sistema-inventario-ventas).
- **Tablero GitHub Projects:** enlace pendiente de incorporar cuando esté creado y vinculado al repositorio.

## Documentación del proyecto

Los archivos se encuentran actualmente en la raíz del repositorio:

- [Diagrama BPMN en PNG](proceso_venta_actualizacion_stock.png): representación visual del proceso de ventas y actualización de stock.
- [Archivo fuente BPMN](proceso_venta_actualizacion_stock.bpmn): modelo BPMN del proceso.
- [Diagrama en SVG](proceso_venta_actualizacion_stock.svg): versión vectorial del diagrama.
- [Historias de usuario](historias_usuario.md): tres historias y sus criterios de aceptación.
- [Indicadores de control](indicadores_control.md): indicadores, estándares, fórmulas y frecuencia de control.
- [Diccionario de datos](diccionario_datos.md): entidades Producto, Venta y DetalleVenta.
- [Backlog para GitHub Projects](backlog_github_projects.csv): datos iniciales de las tres historias.
- [Guía de GitHub](guia_github.md): referencia para completar las actividades de versionado, PR y tablero.

## Alcance funcional considerado

1. Registrar ventas con los productos y cantidades correspondientes.
2. Verificar la disponibilidad de los productos antes de confirmar una operación.
3. Registrar la venta y su detalle.
4. Actualizar el stock automáticamente después de confirmar la venta.
5. Permitir que Depósito controle las existencias y revise necesidades de reposición.
6. Permitir que Administración consulte la información de ventas e inventario para realizar controles e informes.

## Historias de usuario

Las siguientes historias se formalizan a partir de las funcionalidades y áreas trabajadas en las Entregas 1, 2 y 3.

### US-01 - Registro de ventas

Como vendedor/a, quiero registrar las ventas con los productos y cantidades correspondientes, para mantener un historial centralizado de las operaciones.

**Criterios de aceptación:**
- La operación queda identificada con un número único y fecha/hora.
- Cada producto vendido queda registrado en el detalle de la venta.
- El total se corresponde con la suma de los subtotales.
- No se confirma una venta si el stock no es suficiente.

### US-02 - Actualización automática del inventario

Como responsable de Depósito, quiero que el stock se actualice automáticamente después de confirmar una venta, para conocer la disponibilidad real de los productos y reducir errores de inventario.

**Criterios de aceptación:**
- Se descuentan las cantidades vendidas una vez confirmada la operación.
- El stock no puede quedar en un valor negativo.
- La actualización queda visible en un máximo de 3 segundos.
- Si la actualización falla, se registra una incidencia para su revisión.

### US-03 - Consulta de información para control

Como responsable de Administración, quiero consultar la información de ventas e inventario, para realizar controles y apoyar la toma de decisiones.

**Criterios de aceptación:**
- Se pueden consultar ventas por fecha y producto.
- Los totales de los informes coinciden con los registros de ventas.
- Se puede consultar el stock actual de los productos.
- El acceso a la información se limita a usuarios autorizados.

## Tablero ágil

La consigna prevé un tablero interactivo de GitHub Projects con los estados **Por Hacer**, **En Progreso** y **Listo**. Las tres historias deben cargarse como Issues y vincularse al proyecto.

Estados iniciales propuestos para organizar el trabajo documental (no significan que las funcionalidades del software estén implementadas):

| Historia | Estado propuesto | Motivo |
|---|---|---|
| US-01 | Listo | Historia, criterios y flujo de registro documentados. |
| US-02 | En Progreso | Regla de actualización y validaciones en revisión. |
| US-03 | Por Hacer | Falta completar el diseño de los informes y sus filtros. |

Los estados deberán actualizarse según el avance real. Cuando el tablero esté creado, se incorporará aquí su enlace y se guardará una captura como evidencia.

## Control de versiones: Git y GitHub

### Estado del repositorio

- Repositorio público: creado.
- Rama principal: `main`.
- Rama secundaria existente: `feature/bpmn.registro-ventas`.
- Pull Request #1: [Incorporación del diagrama BPMN del proceso de ventas](https://github.com/lucasgauto1759/tecnostock-sistema-inventario-ventas/pull/1).
- Estado actual del PR #1: abierto y pendiente de revisión de pares. El cambio presentado en ese PR corresponde a documentación agregada al README; el diagrama BPMN ya se encuentra publicado en la rama principal.

### Mensajes de commit

Los mensajes deben describir el cambio realizado. Se pueden utilizar, cuando correspondan a modificaciones reales, ejemplos como:

- `docs: documenta las reglas del proceso de ventas`
- `docs: define historias de usuario y criterios de aceptación`
- `docs: agrega indicadores y estándares de control`
- `docs: actualiza README con alcance y uso de IA`

### Pull Request y revisión de pares

El PR debe revisarlo otra persona, quien podrá dejar observaciones o aprobar los cambios. Las observaciones recibidas deben resolverse y la fusión debe realizarse después de la revisión correspondiente. No se debe declarar una revisión de pares si la revisión fue realizada por el mismo estudiante desde otra cuenta.

## Próximas tareas de configuración

1. Corregir y mantener actualizados los enlaces a los archivos según su ubicación real en el repositorio.
2. Completar la revisión real del PR #1, resolver las observaciones recibidas y fusionarlo una vez aprobado.
3. Crear o completar el proyecto de GitHub Projects, cargar las tres historias como Issues y vincularlas al tablero.
4. Incorporar el enlace real del tablero en este README y en la primera página del PDF final.
5. Guardar capturas que evidencien el repositorio público, las ramas, los commits, el PR con su revisión y el tablero con las tres historias.

## Declaración de uso de IA

Se utilizó un asistente de IA como apoyo para proponer una primera estructura del proceso BPMN, organizar las historias de usuario y redactar indicadores de control. Entre los prompts utilizados se incluyeron pedidos para: (1) representar el registro de una venta y la actualización del stock con Pools y Lanes para Cliente, Ventas, Sistema, Depósito y Sistemas; (2) formular historias de usuario y criterios de aceptación a partir de las funcionalidades del caso; y (3) proponer indicadores medibles para verificar el registro de ventas, el tiempo de actualización y la consistencia del inventario.

La revisión humana consistió en contrastar las propuestas con el alcance de TecnoStock, conservar las entidades Producto, Venta y DetalleVenta definidas en la Entrega 3, retirar funcionalidades no establecidas (como una pasarela de pagos o la integración automática con proveedores), revisar el tratamiento de la falta de stock y de las fallas técnicas, y mantener las metas cuantitativas de la Entrega 2 (100 % de ventas registradas, reducción del 80 % de errores y actualización del stock en hasta 3 segundos). Los estados del tablero, los commits, la revisión de pares y los enlaces deben reflejar acciones reales efectuadas por el estudiante y no resultados inventados por la IA.

## Reglas del proceso de ventas

1. El vendedor registra los productos y las cantidades solicitadas por el cliente.
2. El sistema verifica si existe stock suficiente.
3. Si hay disponibilidad, registra la venta y su detalle.
4. El sistema actualiza automáticamente el inventario.
5. Si no hay stock suficiente, informa la situación y no confirma la venta.
6. Si ocurre un error durante la actualización, se registra una incidencia para su revisión.
