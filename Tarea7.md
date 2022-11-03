## Vista

``` sql
CREATE VIEW monto_total_empleado AS
    SELECT e.idEmpleado, SUM(monto)
    FROM gasto g
    INNER JOIN reporte r ON (g.idReporte = g.idReporte)
    INNER JOIN empleado e ON (e.idReporte = r.idReporte)
    GROUP BY e.idEmpleado; 
```


## Trigger

``` sql
DELIMITER $$

CREATE TRIGGER eliminar_reportes_empleado
    AFTER UPDATE
    ON empleado FOR EACH ROW
BEGIN
    IF (new.activo = 0)
        UPDATE reporte r
        SET r.activo = 0;
    END IF;
END$$    

DELIMITER ;
```

## Video