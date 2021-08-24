## Procedimiento para obtener el detalle

PKG_SAP_VENTA.USP_FACT_DETALLE (Permite obtener el detalle de la factura / boleta).

### Inputs

| Property   | type    | Description                                          |
| ---------- | ------- | ---------------------------------------------------- |
| xxNumtdven | varchar | Número de tipo de venta (01 - 02) (factura - boleta) |
| xxSerFac   | varchar | Número de serie de factura (AF2 - ejemplo)           |
| xxNumFac   | varchar | Número de factura (0001010 - ejemplo)                |
| xxSucFac   | varchar | Número de sucursal (02 en caso de miraflores)        |

### Outputs

| Property        | type    | Description                |
| --------------- | ------- | -------------------------- |
| NUMSER          | varchar | Número de servicio         |
| CANTIDAD        | varchar | Cantidad de servicios      |
| PRECIO_UNIT_SOL | varchar | Precio unitario en Sol     |
| PRECIO_UNIT_DOL | varchar | Precio unitario en dolares |
