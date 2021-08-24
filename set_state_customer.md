## Cambiar estado de cliente

PKG_SAP_VENTA.USP_RUC_EST_ENVIO_SAP (Permite cambiar el estado - erroneo o válido)

### Inputs

| Property     | type    | Description                                          |
| ------------ | ------- | ---------------------------------------------------- |
| xxNumRuc     | varchar | Número de ruc                                        |
| xxEnvioSap   | varchar | Flag de envío                                        |
| xxMensajeSAP | varchar | Mensaje a guardar                                    |
| xxEstadoSAP  | varchar | Estado SAP (N / nuevo - M / Modificar - E / Enviado) |

### Codigo referencia

```
  UPDATE SIGESER.SGS_COMPANIA_MAESTRO
  SET CM_ENVIO_SAP = xxEnvioSap,
      CM_SAP_ERROR =xxMensajeSAP,
      CM_ESTADO_SAP = xxEstadoSAP
  WHERE CM_RUCCIA=  xxNumRuc  ;
```
