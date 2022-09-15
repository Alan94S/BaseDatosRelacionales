## Tarea 1

Descripción de base de datos

    Sistema de reembolsos, para obtener un reembolso un empleado debe registrar un reporte en el sistema con un nombre, por ejemplo,   "Gastos primer semestre 2022", a cada reporte se le deben agregar los gastos necesarios con el monto, fecha del gasto y el   concepto (esto puede ser taxi, comida, renta etc). Los empleados tienen asignado un puesto y un país para ayudarnos a seccionar   mejor la manera en que se distribuye el total de los reembolsos.

    Empleado (idEmpleado_PK INT, nombre VARCHAR(50), apellido VARCHAR(50), correo VARCHAR(50), fechaNacimiento DATE, idPuesto_FK INT, idPais_FK INT)
    Reporte (idReporte_PK INT, nombre VARCHAR(50), fechaAlta DATETIME)
    Gasto (idGasto_PK INT, monto FLOAT, fecha DATETIME, ClasificacionGasto_FK INT, idReporte_FK INT)
    ClasificacionGasto (idClasificacion_PK INT, nombre VARCHAR(50))
    Puesto (idPuesto_PK INT, nombre VARCHAR(50))
    Pais (idPais_PK INT, nombre VARCHAR(50))

SGBD
    
    Mysql
    Es uno de los sistemas gestores de bases de datos más famosos y utilizados por desarrolladores, esto es una gran ventaja por que   hace más sencillo encontrar información en foros cuando tienes alguna duda. Para base de datos relaciones es una buena opción por   lo sencillo que es de usar. Una de sus desventajas es que puede no ser tan eficiente cuando se trabaja con grandes cantidades de   información para estos casos existen otras alternativas, pero para la materia creo que es una excelente opción.