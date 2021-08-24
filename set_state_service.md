## Cambiar estado de servicio

PKG_SAP_VENTA.USP_SERVICIO_EST_ENVIO_SAP (Permite cambiar el estado - erroneo o válido)

### Inputs

| Property     | type    | Description       |
| ------------ | ------- | ----------------- |
| P_NUMSER     | varchar | Número de ruc     |
| P_VALOR      | varchar | Flag de envío     |
| P_MENSAJESAP | varchar | Mensaje a guardar |

### Outputs

| Property  | type    | Description                                   |
| --------- | ------- | --------------------------------------------- |
| Resultado | Integer | flag de validación (-1 o 2 / Error - 1 / OK ) |
| Mensaje   | varchar | Mesnaje de respuesta                          |

### Codigo referencia

```
BEGIN


    BEGIN

            SELECT CASE WHEN EXISTS(SELECT * FROM SIGESER.SGS_SERVICIO WHERE S_NUMSER= P_NUMSER AND S_ESTSER='A')
            THEN
                1 --VALIDA SI EXISTE EL SERVICIO )
            ELSE
                0
            END
            INTO
            P_ITEM
        FROM
            DUAL;

        EXCEPTION
            WHEN OTHERS THEN
                P_ITEM := 0;

    END;

    IF(P_ITEM > 0 )THEN

        UPDATE
            SIGESER.SGS_SERVICIO
        SET
           -- DS.OSD_LAB_FLAG_MIGR   = P_FLAG_MIG,
            S_ESTADO_SAP   = P_VALOR,
            S_SAP_ERROR    = P_MENSAJESAP
            --SYS_FECMOD   = SYSDATE
        WHERE
           S_NUMSER = P_NUMSER AND
           S_ESTSER='A';

        Resultado := 1;
        Mensaje   := 'Datos actualizados en SAP - Servicios';

        ELSE

        Resultado := -1;
        Mensaje   := 'No se encontro el numero de servicio' + P_NUMSER;

    END IF;

EXCEPTION
    WHEN OTHERS THEN
        Resultado := 2;
        Mensaje   := TO_CHAR(SQLCODE) || ' - '|| SUBSTR(SQLERRM, 1, 100);
END;
```
