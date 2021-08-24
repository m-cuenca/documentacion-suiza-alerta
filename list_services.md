## Listar los servicios pendientes a migrar a SAP

PKG_SAP_VENTA.USP_SERVICIO_PEND_ENVIO_SAP (Permite obtener todos los registros que estan con codigo de estado M o N)

### Inputs

| Property | type    | Description                             |
| -------- | ------- | --------------------------------------- |
| xxNumEmp | varchar | Número de empresa (01 en caso suizalab) |

### Outputs

| Property    | type    | Description                |
| ----------- | ------- | -------------------------- |
| NUMSER      | varchar | Número de servicio         |
| DESCRIPCION | varchar | Nombre de servicio         |
| PROYECTO    | varchar | Codigo de proyecto         |
| ESTADO_REG  | varchar | Estado de registro (M o N) |
