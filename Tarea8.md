``` sql
CREATE DATABASE correlacion;
USE correlacion;

CREATE TABLE IF NOT EXISTS datos(
id INT PRIMARY KEY auto_increment,
x DECIMAL(5,2),
y DECIMAL(5,2)
);

INSERT INTO datos (x,y) VALUES (6,45),(12,47),(13,39),(17,58),(22,68),(25,76),(27,75),(29,74),(30,78),(32,81);

DROP PROCEDURE IF EXISTS corr;
DELIMITER //
CREATE PROCEDURE corr(
OUT a DECIMAL(5,3)
)
BEGIN
SELECT SUM(Xt*Yt)/((SQRT(SUM(POW(Xt,2))))*(SQRT(SUM(POW(Yt,2)))))
    FROM ( SELECT x - (SELECT AVG(x) FROM datos) Xt, y - (SELECT AVG(y) FROM datos) Yt FROM datos) c INTO a;
END
//

CALL corr(@a);

SELECT @a;
```