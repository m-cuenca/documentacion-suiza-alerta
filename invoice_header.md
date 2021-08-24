## Procedimiento para obtener la cabecera

USP_OBTENER_ULTIMA_VENTA (Permite obtener datos de la cabecera del comprobante a migrar).

### Inputs

| Property | type    | Description                        |
| -------- | ------- | ---------------------------------- |
| xxNUMEMP | varchar | Número de empresa (Suizalab es 01) |

### Outputs

| Property           | type    | Description                                |
| ------------------ | ------- | ------------------------------------------ |
| SERIE_ELECT        | varchar | Serie del documento (BAF1)                 |
| FLAG_ELECT         | varchar | Flag envio (1)                             |
| FACT_TDVEN         | varchar | Tipo de venta facturación (01)             |
| SAP_TDVEN          | varchar | Tpo de documento SAP (03)                  |
| SAP_TDVEN_SUNAT    | varchar | Código de documento (BV)                   |
| FACT_SERIE         | varchar | Serie (AF1)                                |
| FACT_NUMERO        | varchar | Correlativo (0003625)                      |
| FACT_SUC           | varchar | Sucursal código (53)                       |
| NUM_MONEDA         | varchar | Código moneda (01)                         |
| SAP_MONEDA         | varchar | Moneda letra (SOL)                         |
| TASA_IGV           | varchar | Tasa igv (18)                              |
| SAP_IGV            | varchar | Tasa SAP (IGV_18)                          |
| RUCCIA             | varchar | Documento de identidad (07449037)          |
| SAP_RUC            | varchar | Documento de identidad SAP (99999999999)   |
| RAZON_SOCIAL       | varchar | Razon social (DELFIN JAIME GLORIA)         |
| FECHA_DOC          | varchar | Fecha de documento (18/08/2021 19:00:51)   |
| FECHA_VENCE        | varchar | Fecha de vencimiento (18/08/2021 19:00:51) |
| SAP_TOTAL_DOC      | varchar | Total SAP (80)                             |
| SAP_CORTESIA_MONTO | varchar | Cortesia (0)                               |
| SAP_FLAG_CORTESIA  | varchar | Cortesia flag (N)                          |
| PLANILLA_DSCTO_DNI | varchar | Descuento DNI (0)                          |
| FOXCIA             | varchar | Código Fox (8308)                          |
| SAP_CENTRO_COSTO   | varchar | Centro costo (HNAVAL)                      |
| COMENTARIO         | varchar | Comentario (INTERFACE SUIZALAB)            |
