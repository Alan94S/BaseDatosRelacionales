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
SELECT @pos_cuartil1 = FLOOR(COUNT(monto) / 4) - 1
FROM gasto
WHERE monto IS NOT NULL
ORDER BY monto;

SELECT monto AS cuartil_1
FROM gasto
WHERE monto IS NOT NULL
ORDER BY monto
LIMIT @pos_cuartil1, 1;

SELECT @pos_cuartil3 = FLOOR((COUNT(monto) / 4) * 3) - 1
FROM gasto
WHERE monto IS NOT NULL
ORDER BY monto;

SELECT monto AS cuartil_3
FROM gasto
WHERE monto IS NOT NULL
ORDER BY monto
LIMIT @pos_cuartil3, 1;
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