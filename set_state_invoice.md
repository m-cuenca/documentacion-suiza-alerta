## Cambiar estado de factura

PKG_SAP_VENTA.USP_PROVIS_EST_ENVIO_SAP (Permite cambiar el estado - erroneo o válido)

### Inputs

| Property     | type    | Description                       |
| ------------ | ------- | --------------------------------- |
| xxSucFac     | varchar | Número de sucursal                |
| xxTdoFac     | varchar | Número de tipo de venta (01 - 02) |
| xxSerFac     | varchar | Serie                             |
| xxNumFac     | varchar | Número de factura (correlativo)   |
| xxEnvioSap   | varchar | Flag de envio a sap               |
| xxMensajeSAP | varchar | Mensaje                           |

### Codigo referencia

```
  UPDATE SIGESER.SGS_FACTURACION_CAB FA
  SET FA.FC_ENVIO_SAP = xxEnvioSap,
      FA.FC_ENVIO_SAP2 = xxEnvioSap,
      FA.FC_ERROR_ENVIO_SAP =SUBSTR(xxMensajeSAP,1,250),
      FA.FC_ERROR_SAP2 = SUBSTR(xxMensajeSAP,1,250),
      FA.FC_FECENVIO_SAP2 = SYSDATE
  WHERE FA.FC_NUMSUC = xxSucFac
  AND FA.FC_NUMTDVEN = xxTdoFac
  AND FA.FC_SERFAC = xxSerFac
  AND FA.FC_NUMFAC = xxNumFac;
```
