
# Tarea 3 Modelo relacional

    Empleado (idEmpleado_PK INT, nombre VARCHAR(50), apellido VARCHAR(50), correo VARCHAR(50), fechaNacimiento DATE, idPuesto_FK INT, idPais_FK INT)
    Reporte (idReporte_PK INT, nombre VARCHAR(50), fechaAlta DATETIME)
    Gasto (idGasto_PK INT, monto FLOAT, fecha DATETIME, ClasificacionGasto_FK INT, idReporte_FK INT)
    ClasificacionGasto (idClasificacion_PK INT, nombre VARCHAR(50))
    Puesto (idPuesto_PK INT, nombre VARCHAR(50))
    Pais (idPais_PK INT, nombre VARCHAR(50))

# Diagrama

![Tarea3 circle logo](/imagenes/Tarea3.png "Tarea3")

# Querys

SELECT SUM(monto) FROM gasto g INNER JOIN reporte r ON (g.idReporte = g.idReporte) INNER JOIN EMPLEADOS e ON (e.idReporte = r.idReporte) INNER JOIN puesto p ON (e.idPuesto = p.idPuesto) WHERE p.idPuesto = 1; 

SELECT SUM(monto) FROM gasto g INNER JOIN reporte r ON (g.idReporte = g.idReporte) INNER JOIN EMPLEADOS e ON (e.idReporte = r.idReporte) INNER JOIN pais p ON (e.idPais = p.idPais) WHERE p.idPais = 1;

SELECT SUM(monto) FROM gasto g INNER JOIN clasificacionGasto cg ON (g.idclasificacionGasto = cg.idclasificacionGasto) WHERE sg.idClasificacionGasto = 1;

SELECT SUM(monto) FROM gasto g WHERE fecha BETWEEN '01-01-2021' AND '31-12-2021';
