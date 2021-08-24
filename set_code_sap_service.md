## Cambiar codigo de SAP en servicio

PKG_SAP_VENTA.USP_SERVICIO_CODIGO_SAP (Permite agregar el cardcode en el servicio)

### Inputs

| Property | type    | Description        |
| -------- | ------- | ------------------ |
| P_NUMSER | varchar | Número de servicio |
| P_VALOR  | varchar | Cardcode a guardar |

### Outputs

| Property  | type    | Description                            |
| --------- | ------- | -------------------------------------- |
| Resultado | Integer | Flag de resultado del procedimiento    |
| Mensaje   | varchar | Mensaje de resultado del procedimiento |

### Código referencia

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
            S_COD_SAP  = P_VALOR,
            S_NUMSER_AGRUPADO = P_VALOR
            --SYS_FECMOD   = SYSDATE
        WHERE
           S_NUMSER = P_NUMSER AND
           S_ESTSER='A';

        Resultado := 1;
        Mensaje   := 'CODIGO SAP ACTUALIZADO ';

        ELSE

        Resultado := -1;
        Mensaje   := 'El servicio No existe' + P_NUMSER;

    END IF;

EXCEPTION
    WHEN OTHERS THEN
        Resultado := 2;
        Mensaje   := TO_CHAR(SQLCODE) || ' - '|| SUBSTR(SQLERRM, 1, 100);
END;
```
