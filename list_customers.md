## Listar los clientes pendientes a migrar a SAP

PKG_SAP_VENTA. USP_RUC_PEND_ENVIO_SAP (Permite obtener todos los registros que estan con codigo de estado M o N)

### Inputs

| Property | type    | Description                             |
| -------- | ------- | --------------------------------------- |
| xxNumEmp | varchar | Número de empresa (01 en caso suizalab) |

### Outputs

| Property       | type    | Description                |
| -------------- | ------- | -------------------------- |
| RUC            | varchar | Número de RUC              |
| RAZON_SOCIAL   | varchar | Razaon Social              |
| TELCIA         | varchar | Telefono                   |
| CELCIA         | varchar | Celular                    |
| CELCONT1       | varchar | Celular 2                  |
| EMACONT1       | varchar | Email                      |
| COMENTARIO     | varchar | Comentario                 |
| TIPODOC        | varchar | Tipo de documento          |
| SAP_TIPO_PER   | varchar | Tipo de persona            |
| GRUPO          | varchar | Grupo SAP                  |
| PATERNO        | varchar | Apellido paterno           |
| MATERNO        | varchar | Apellido materno           |
| NOMBRES        | varchar | Nombres                    |
| DIRCIA         | varchar | Dirección                  |
| DISTRITO       | varchar | Distrito                   |
| COD_FORPAG     | varchar | Código forma de pago       |
| SAP_GRUPO_PAGO | varchar | Codigo grupo sap           |
| NUM_DIAS       | varchar | Numero de dias             |
| ESTADO_REG_SAP | varchar | Estado de registro (M o N) |

### Data de ejemplo

```
[
    {
        "RUC": "20144364059",
        "RAZON_SOCIAL": "FUERZA AEREA DEL PERU - FOSFAP",
        "TELCIA": "990184694",
        "CELCIA": "990184694",
        "CELCONT1": "998867016",
        "EMACONT1": "",
        "COMENTARIO": "Servicio windows (cia fact)",
        "TIPODOC": "6",
        "SAP_TIPO_PER": "TPJ",
        "GRUPO": "100",
        "PATERNO": "",
        "MATERNO": "",
        "NOMBRES": "",
        "DIRCIA": "AV. LA PERUANIDAD NRO. SN CAMPO DE MARTE (NOTIF. A DIRECCION GENERAL DE ECONOMIA)",
        "DISTRITO": "JESUS MARIA",
        "COD_FORPAG": "002",
        "SAP_GRUPO_PAGO": "FACTURA%",
        "NUM_DIAS": "60",
        "ESTADO_REG_SAP": "M"
    }
]
```
