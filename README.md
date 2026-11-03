# TecnoStock - Sistema de Gestión de Inventario y Ventas

## Descripción

Proyecto académico de la asignatura **Organización Empresarial** (Tecnicatura Universitaria en Programación a Distancia, UTN). El caso de estudio es **TecnoStock**, una empresa dedicada a la comercialización de productos tecnológicos.

El proyecto propone un Sistema de Gestión de Inventario y Ventas para centralizar los datos de productos, registrar ventas y actualizar el stock automáticamente. La información puede ser consultada por Ventas, Depósito y Administración, con soporte del área de Sistemas.

## Integrante

- Lucas Gauto.

## Documentación del proyecto

- `bpmn/proceso_venta_actualizacion_stock.png`: diagrama del proceso con notación BPMN 2.0.
- `bpmn/proceso_venta_actualizacion_stock.bpmn`: fuente BPMN para abrir y editar en un modelador compatible.
- `docs/historias_usuario.md`: historias de usuario y criterios de aceptación.
- `docs/indicadores_control.md`: indicadores, estándares y frecuencia de control.
- `docs/diccionario_datos.md`: resumen de las entidades Producto, Venta y DetalleVenta.
- `docs/backlog_github_projects.csv`: datos del backlog para cargar al tablero.
- `docs/guia_github.md`: pasos para crear el repositorio, las ramas, el Pull Request y el tablero.

## Alcance funcional considerado

1. Registrar ventas con los productos y cantidades correspondientes.
2. Verificar la existencia y disponibilidad de los productos antes de confirmar una operación.
3. Registrar la venta y su detalle.
4. Actualizar el stock automáticamente luego de confirmar la venta.
5. Permitir que Depósito revise necesidades de reposición y que Administración consulte los datos para control e informes.

## Repositorio y tablero

- **Repositorio público:** https://github.com/lucasgauto1759/tecnostock-sistema-inventario-ventas
- **Tablero GitHub Projects:** https://github.com/users/lucasgauto1759/projects/1/views/1

El repositorio y el tablero fueron creados en GitHub. El tablero se configuró como público y contiene las tres historias de usuario vinculadas como Issues.

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
- Si la actualización falla, se registra una incidencia y se evita informar la operación como finalizada hasta resolverla.

### US-03 - Consulta de información para control

Como responsable de Administración, quiero consultar la información de ventas e inventario, para realizar controles y apoyar la toma de decisiones.

**Criterios de aceptación:**
- Se pueden consultar ventas por fecha y producto.
- Los totales de los informes coinciden con los registros de ventas.
- Se puede consultar el stock actual de los productos.
- El acceso a la información se limita a usuarios autorizados.

## Tablero ágil

El proyecto de GitHub Projects ya está creado con las columnas **Por Hacer**, **En Progreso** y **Listo**. Las tres historias están cargadas como Issues y vinculadas al tablero.

Estado actual del seguimiento de la documentación (no significa que las funcionalidades del software estén implementadas):

| Historia | Estado sugerido | Motivo |
|---|---|---|
| US-01 | Listo | Historia, criterios y flujo de registro documentados. |
| US-02 | En Progreso | Regla de actualización y validaciones en revisión. |
| US-03 | Por Hacer | Falta completar el diseño de los informes y sus filtros. |

Actualizar los estados según el avance real y capturar una evidencia del tablero para la entrega.

## Control de versiones: Git y GitHub

### Ramas propuestas

- `main`: versión estable de la documentación.
- `feature/bpmn-registro-ventas`: diagrama y descripción del proceso BPMN.
- `docs/historias-usuario-backlog`: historias de usuario y criterios de aceptación.
- `docs/indicadores-control`: indicadores y estándares de desempeño.

### Ejemplos de mensajes de commit

- `docs: incorpora diagrama BPMN del registro de ventas`
- `docs: define historias de usuario y criterios de aceptación`
- `docs: agrega indicadores y estándares de control`
- `docs: actualiza README con alcance y uso de IA`

### Pull Request y revisión de pares

Crear al menos un Pull Request desde una rama secundaria hacia `main`. Por ejemplo: `feature/bpmn-registro-ventas` → `main`.

En la descripción del PR indicar los archivos incorporados, el objetivo del cambio y qué debe revisar el compañero. Solicitar una revisión real a otro estudiante, registrar al menos una observación o aprobación, aplicar los cambios necesarios y recién entonces fusionar el PR. **No declarar el PR como revisado o fusionado hasta que esas acciones hayan ocurrido en GitHub.**

## Estado de la implementación del repositorio y tablero

- Repositorio público creado y documentación cargada.
- Tablero GitHub Projects creado, configurado como público y vinculado a las tres Issues.
- Historias distribuidas según el estado actual de la documentación: US-01 en **Listo**, US-02 en **En Progreso** y US-03 en **Por Hacer**.
- Pull Request #1 abierto para documentar cambios en el README. Se recibió un comentario de revisión desde la cuenta secundaria `lumsoner`, perteneciente al mismo estudiante; por transparencia, se considera una **auto-revisión técnica**, no una revisión de pares independiente. La revisión de otro estudiante queda pendiente de confirmar con la cátedra o de realizar si se consigue un compañero revisor.

Antes de entregar, incorporar capturas que muestren el repositorio público, el Pull Request y el tablero con las tres historias.

## Declaración de uso de IA

Se utilizó un asistente de IA como apoyo para proponer una primera estructura del proceso BPMN, organizar las historias de usuario y redactar indicadores de control. Entre los prompts utilizados se incluyeron pedidos para: (1) representar el registro de una venta y la actualización del stock con Pools y Lanes para Cliente, Ventas, Sistema, Depósito y Sistemas; (2) formular historias de usuario y criterios de aceptación a partir de las funcionalidades del caso; y (3) proponer indicadores medibles para verificar el registro de ventas, el tiempo de actualización y la consistencia del inventario.

La revisión humana consistió en contrastar las propuestas con el alcance de TecnoStock, conservar las entidades Producto, Venta y DetalleVenta definidas en la Entrega 3, retirar funcionalidades no establecidas (como una pasarela de pagos o la integración automática con proveedores), revisar el tratamiento de la falta de stock y de las fallas técnicas, y mantener las metas cuantitativas de la Entrega 2 (100 % de ventas registradas, reducción del 80 % de errores y actualización del stock en hasta 3 segundos). Los estados del tablero, los commits, la revisión de pares y los enlaces deben reflejar acciones reales efectuadas por el estudiante y no resultados inventados por la IA.
