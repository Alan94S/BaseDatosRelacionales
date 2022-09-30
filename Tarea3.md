
# Tarea 3 Modelo relacional

    Empleado (idEmpleado_PK INT, nombre VARCHAR(50), apellido VARCHAR(50), correo VARCHAR(50), fechaNacimiento DATE, idPuesto_FK INT, idPais_FK INT)
    Reporte (idReporte_PK INT, nombre VARCHAR(50), fechaAlta DATETIME)
    Gasto (idGasto_PK INT, monto FLOAT, fecha DATETIME, ClasificacionGasto_FK INT, idReporte_FK INT)
    ClasificacionGasto (idClasificacion_PK INT, nombre VARCHAR(50))
    Puesto (idPuesto_PK INT, nombre VARCHAR(50))
    Pais (idPais_PK INT, nombre VARCHAR(50))

![Tarea3 circle logo](/imagenes/Tarea3.png "Tarea3")


