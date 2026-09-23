# Solicitudes de vacaciones: estructura de datos

## Tabla de Excel «Solicitudes» (Práctica 2.1)

`SolicitudesVacaciones_OneDrive.xlsx` contiene la tabla `Solicitudes`, con cinco filas de ejemplo, lista para subir a OneDrive para la Empresa. El conector de Excel no tiene tipos: todo llega a Power Apps como texto, por eso las fechas se guardan como texto `aaaa-mm-dd`.

| Columna | Contenido | Tipo en Excel |
|---|---|---|
| Id | Identificador de la solicitud, `SOL-aaaammddhhmmss` | Texto |
| Title | Motivo | Texto |
| FechaInicio | Primer día, `aaaa-mm-dd` | Texto |
| FechaFin | Último día, `aaaa-mm-dd` | Texto |
| Dias | Días naturales | Número |
| Tipo | Vacaciones · Asuntos propios · Formación | Texto |
| Estado | Pendiente · En revisión · Aprobada · Rechazada | Texto |
| Solicitante | Correo del empleado | Texto |
| Aprobador | Correo del responsable | Texto |
| Comentarios | Texto libre | Texto |

Power Apps añade por su cuenta una columna oculta `__PowerAppsId__` para identificar cada fila. No hay que crearla ni borrarla.

## Tabla de Excel «Pedidos» (Práctica 3.1)

`PedidosMaquinas_OneDrive.xlsx` contiene la tabla `Pedidos`, para el formulario de pedido de la Machine Ordering App.

| Columna | Contenido | Tipo en Excel |
|---|---|---|
| Id | Identificador del pedido, `PED-aaaammddhhmmss` | Texto |
| Title | Máquina | Texto |
| Cantidad | Unidades | Número |
| FechaDeseada | Fecha de entrega, `aaaa-mm-dd` | Texto |
| Email | Correo de contacto | Texto |
| Comentarios | Texto libre | Texto |

## Estados de una solicitud

| Estado | Quién lo pone |
|---|---|
| Pendiente | La app, al crear la solicitud |
| En revisión | El flujo de aprobación, al pedir la respuesta al responsable |
| Aprobada · Rechazada | El flujo de aprobación, con la respuesta del responsable |

## Si prefieres SharePoint

El curso trabaja sobre Excel en OneDrive para no depender de un sitio de SharePoint ni de permisos de administrador. `SolicitudesVacaciones_ejemplo.xlsx` sigue en esta carpeta por si quieres crear la lista con **+ Nuevo > Lista > Desde Excel**: en ese caso, `Tipo` y `Estado` pasan a columnas de elección, `Solicitante` y `Aprobador` a columnas de persona, las fechas dejan de ser texto (sobran los `DateValue`) y el flujo de aprobación puede usar el desencadenador *Cuando se crea un elemento* en lugar de la programación.
