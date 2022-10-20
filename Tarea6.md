# Tarea 6 Consultas

## Media

``` sql
SELECT AVG(monto) FROM gasto;
```

## Mínimos y Máximos

``` sql
SELECT MIN(monto) FROM gasto;
SELECT MAX(monto) FROM gasto;
```

## Cuantil distinto a la mediana

``` sql
SELECT AVG(monto) FROM gasto;
```

## Moda

``` sql
SELECT monto, COUNT(*) AS total FROM gasto GROUP BY monto ORDER BY total DESC LIMIT 1;
```

## Hallazgos