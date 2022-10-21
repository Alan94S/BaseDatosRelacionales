# Tarea 6 Consultas

## Media

``` sql
SELECT AVG(monto)
FROM gasto
WHERE monto IS NOT NULL;
```

## Mínimos y Máximos

``` sql
SELECT MIN(monto)
FROM gasto

SELECT MAX(monto)
FROM gasto;
```

## Cuantil distinto a la mediana

``` sql
DELIMITER //
CREATE PROCEDURE quartiles(
	 quar INT)
BEGIN
    SELECT monto AS cuartil
	FROM gasto
	WHERE monto IS NOT NULL
	ORDER BY monto
	LIMIT quar, 1;
END //
DELIMITER ;

SELECT FLOOR(COUNT(monto) / 4) - 1 AS pos_cuartil1
FROM gasto
WHERE monto IS NOT NULL INTO @pos_cuartil1;

CALL quartiles(@pos_cuartil1);

SELECT FLOOR((COUNT(monto) / 4) * 3) - 1 as pos_cuartil3
FROM gasto
WHERE monto IS NOT NULL INTO @pos_cuartil3;

CALL quartiles(@pos_cuartil3);
```

## Moda

``` sql
SELECT monto, COUNT(*) AS total
FROM gasto
WHERE monto IS NOT NULL
GROUP BY monto
ORDER BY total DESC
LIMIT 1;
```