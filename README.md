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

- **Repositorio público:** [PEGAR AQUÍ LA URL REAL DEL REPOSITORIO]
- **Tablero GitHub Projects:** [PEGAR AQUÍ LA URL REAL DEL TABLERO]

> Estos enlaces deben reemplazarse por las direcciones reales una vez creados y publicados el repositorio y el tablero. No se deben entregar los marcadores de posición.

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

Crear un proyecto de GitHub Projects con las columnas **Por Hacer**, **En Progreso** y **Listo**. Cargar las tres historias anteriores como Issues y vincularlas al proyecto.

Estado inicial sugerido para el seguimiento de la documentación (no significa que las funcionalidades del software estén implementadas):

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

## Puesta en marcha en GitHub (pasos pendientes de ejecución)

1. Crear en GitHub un repositorio **público** llamado `tecnostock-sistema-inventario-ventas`.
2. Cargar el contenido de esta carpeta, conservando `README.md`, `bpmn/`, `docs/` y `.github/`.
3. Crear las ramas secundarias indicadas en la sección de control de versiones y realizar commits con mensajes descriptivos.
4. Abrir un Pull Request desde una rama secundaria hacia `main`, solicitar la revisión de otro estudiante, resolver los comentarios y fusionarlo solo después de recibir una aprobación real.
5. Crear un proyecto en GitHub Projects con las columnas `Por Hacer`, `En Progreso` y `Listo`; cargar las tres historias como Issues y vincularlas al tablero.
6. Copiar las direcciones públicas reales del repositorio y del tablero a la primera página del informe y a los enlaces de este README.
7. Incorporar capturas que muestren el repositorio público, las ramas, los commits, el Pull Request revisado y el tablero con las tres historias.

Los elementos anteriores son una guía de ejecución. Los enlaces, estados y revisiones deben actualizarse con evidencia real después de realizar las acciones en GitHub; no deben presentarse como realizadas antes de ejecutarlas.

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

