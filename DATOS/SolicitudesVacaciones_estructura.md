# Solicitudes de vacaciones: estructura de datos

## Tabla de Excel «Solicitudes» (Práctica 2.1)

`SolicitudesVacaciones_OneDrive.xlsx` contiene la tabla `Solicitudes`, con cinco filas de ejemplo, lista para subir a OneDrive para la Empresa. El conector de Excel no tiene tipos: todo llega a Power Apps como texto, por eso las fechas se guardan como texto `aaaa-mm-dd`.

| Columna | Contenido | Tipo en Excel |
|---|---|---|
| Title | Motivo | Texto |
| FechaInicio | Primer día, `aaaa-mm-dd` | Texto |
| FechaFin | Último día, `aaaa-mm-dd` | Texto |
| Dias | Días naturales | Número |
| Tipo | Vacaciones · Asuntos propios · Formación | Texto |
| Estado | Pendiente · Aprobada · Rechazada | Texto |
| Solicitante | Correo del empleado | Texto |
| Aprobador | Correo del responsable | Texto |
| Comentarios | Texto libre | Texto |

Power Apps añade por su cuenta una columna oculta `__PowerAppsId__` para identificar cada fila. No hay que crearla ni borrarla.

## Lista de SharePoint «Solicitudes de vacaciones» (Prácticas 3.2, 4.1 y 4.2)

Estructura usada a partir de la Sesión 3. Crea las columnas **sin espacios ni tildes** para que el nombre interno coincida con el que aparece en las fórmulas.

| Columna | Tipo | Configuración |
|---|---|---|
| Title | Una línea de texto | Existe por defecto. Guarda el motivo |
| FechaInicio | Fecha y hora | Solo fecha · obligatoria |
| FechaFin | Fecha y hora | Solo fecha · obligatoria |
| Dias | Número | 0 decimales |
| Tipo | Elección | Vacaciones · Asuntos propios · Formación · predeterminado *Vacaciones* |
| Estado | Elección | Pendiente · Aprobada · Rechazada · predeterminado *Pendiente* |
| Solicitante | Persona | Una persona |
| Aprobador | Persona | Una persona |
| Comentarios | Varias líneas de texto | Texto sin formato |

`SolicitudesVacaciones_ejemplo.xlsx` contiene cinco filas de ejemplo para crear la lista. Si creas la lista con **+ Nuevo > Lista > Desde Excel**, revisa después el tipo de cada columna: `Tipo` y `Estado` deben ser de elección, y `Solicitante` y `Aprobador` hay que añadirlas a mano porque las columnas de persona no se importan desde Excel.

## Lista «Pedidos máquinas» (Práctica 3.1)

| Columna | Tipo |
|---|---|
| Title | Una línea de texto (máquina) |
| Cantidad | Número |
| FechaDeseada | Fecha y hora (solo fecha) |
| Email | Una línea de texto |
| Comentarios | Varias líneas de texto |
