# Diccionario de datos - resumen para el repositorio

## Producto
| Campo | Tipo | Descripción |
|---|---|---|
| id_producto | Integer | Identificador único del producto. |
| nombre | String | Nombre comercial. |
| descripcion | String | Características del producto. |
| precio_unitario | Decimal | Precio de venta por unidad. |
| stock_actual | Integer | Cantidad disponible. |
| stock_minimo | Integer | Umbral para revisar reposición. |

## Venta
| Campo | Tipo | Descripción |
|---|---|---|
| id_venta | Integer | Identificador único de la operación. |
| fecha_hora | DateTime | Fecha y hora de registro. |
| id_cliente | Integer | Identificador del cliente asociado a la venta, si corresponde. |
| total_venta | Decimal | Importe total de la operación. |
| metodo_pago | String | Medio de pago. |
| estado | String | Estado de la operación. |

## DetalleVenta
| Campo | Tipo | Descripción |
|---|---|---|
| id_detalle | Integer | Identificador único del detalle. |
| id_venta | Integer | Referencia a Venta. |
| id_producto | Integer | Referencia a Producto. |
| cantidad | Integer | Unidades vendidas. |
| precio_unitario_venta | Decimal | Precio aplicado al momento de la venta. |
| subtotal | Decimal | cantidad × precio_unitario_venta. |

Relaciones: una Venta tiene muchos DetalleVenta; un Producto puede estar en muchos DetalleVenta. Cada DetalleVenta pertenece a una sola Venta y referencia un solo Producto.
