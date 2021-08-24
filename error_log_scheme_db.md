## Estructura de la tabla log de errores de facturacion

Lista de propiedades para la tabla de registro de errores en el proceso de migración

### Properties

| Property           | type    | Description                             |
| ------------------ | ------- | --------------------------------------- |
| LFC_NUMEMP         | char(2) | Número de empresa                       |
| LFC_NUMSUC         | char(2) | Número de sucursal                      |
| LFC_NUMTDVEN       | char(2) | Número de tipo de venta                 |
| LFC_SERFAC         | varchar | Serie                                   |
| LFC_NUMFAC         | varchar | Correlativo                             |
| LFC_DOC            | char(2) | Código de documento (01 - 03 - 07 - 08) |
| LFC_TIPO_MIGRACION | char(2) | Código de tipo de migración             |
| LFC_ESTADO         | char(2) | Estado (F - finalizado, P en proceso)   |
| LFC_MENSAJE_BACK   | varchar | Mensaje para el Back                    |
| LFC_MENSAJE_FRONT  | varchar | mensaje para el Front                   |
| LFC_MIGRACION      | varchar | Tipo de migración en texto              |
| LFC_USUARIO        | char(1) | Responsable de solución                 |
| LFC_FECHA_REGISTRO | date    | Fecha de registro                       |
| LFC_FECHA_SOLUCION | date    | Feccha de solucion                      |
| LFC_ID             | integer | Id autoincrementable                    |
| LFC_COD_ERROR      | varchar | Codigo de error                         |
| LFC_REFERENCIA     | varchar | Propiedad de referencia                 |
