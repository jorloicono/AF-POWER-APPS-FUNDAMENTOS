# Lista de SharePoint «Solicitudes de vacaciones»

Estructura usada en las Prácticas 2.1, 3.2, 4.1 y 4.2. Crea las columnas **sin espacios ni tildes** para que el nombre interno coincida con el que aparece en las fórmulas.

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

`SolicitudesVacaciones_ejemplo.xlsx` contiene cinco filas de ejemplo en una tabla llamada `Solicitudes`. Si creas la lista con **+ Nuevo > Lista > Desde Excel**, revisa después el tipo de cada columna: `Tipo` y `Estado` deben ser de elección, y `Solicitante` y `Aprobador` hay que añadirlas a mano porque las columnas de persona no se importan desde Excel.

## Lista «Pedidos máquinas» (Práctica 3.1)

| Columna | Tipo |
|---|---|
| Title | Una línea de texto (máquina) |
| Cantidad | Número |
| FechaDeseada | Fecha y hora (solo fecha) |
| Email | Una línea de texto |
| Comentarios | Varias líneas de texto |
