## Vista

``` sql
CREATE VIEW monto_total_empleado AS
SELECT e.correo, ROUND(SUM(monto),2) AS total
FROM gasto g
INNER JOIN reporte r ON (r.idReporte = g.idReporte)
RIGHT JOIN empleado e ON (e.idEmpleado = r.idEmpleado)
GROUP BY r.idEmpleado;

CREATE VIEW monto_total_pais AS
SELECT p.nombre, IF(ROUND(SUM(monto),2) IS NULL,0,ROUND(SUM(monto),2)) AS total
FROM gasto g
INNER JOIN reporte r ON (r.idReporte = g.idReporte)
INNER JOIN empleado e ON (e.idEmpleado = r.idEmpleado)
RIGHT JOIN pais p ON (e.idPais = p.idPais)
GROUP BY p.nombre;

--OBTENER GASTOS QUE NO TENGAN CLAIFICACIÓN
CREATE VIEW gasto_no_clasificado AS
SELECT g.*
FROM gasto g
LEFT JOIN clasificaciongasto cg ON (g.idClasificacion = cg.idclasificacion)
WHERE cg.idclasificacion IS NULL;

-- OBTENER MONTO TOTAL POR EMPLEADO SIN TOMAR EN CUENTA UNA CLASIFICACIÓN EN ESPECÍFICO
CREATE VIEW monto_total_empelado_sin_clasificacion_gasolina AS
SELECT e.correo, IF(ROUND(SUM(g.monto),2) IS NULL,0,ROUND(SUM(g.monto),2)) AS monto_gasto_sin_clasificacion
FROM reporte r
INNER JOIN empleado e ON (r.idEmpleado = e.idEmpleado)
LEFT JOIN gasto g ON (g.idReporte = r.idReporte AND g.idGasto NOT IN (SELECT g.idGasto FROM gasto WHERE g.idClasificacion = 1))
GROUP BY e.idEmpleado;

```


## Trigger

``` sql
DELIMITER $$

CREATE TRIGGER eliminar_reportes_empleado
    AFTER UPDATE
    ON empleado FOR EACH ROW
BEGIN
    IF (new.activo = 0) THEN
        UPDATE reporte r
        SET r.activo = 0;
ELSE IF (new.activo = 1) THEN
UPDATE reporte r
        SET r.activo = 1;
END IF;
    END IF;
END$$    

DELIMITER ;

SELECT * FROM reporte WHERE idEmpleado = 1;
UPDATE empleado SET activo = 1 WHERE idEmpleado = 1 LIMIT 1;
```

## Video