# Tarea 4 Creación base de datos

CREATE DATABASE IF NOT EXISTS reembolsos;
USE reembolsos;

CREATE TABLE IF NOT EXISTS pais(
    idPais INT AUTO_INCREMENT PRIMARY KEY,
    nombre VARCHAR(100)
);

CREATE TABLE IF NOT EXISTS puesto(
    idPuesto INT AUTO_INCREMENT PRIMARY KEY,
    nombre VARCHAR(100)
);

CREATE TABLE IF NOT EXISTS clasificacionGasto(
    idclasificacion INT AUTO_INCREMENT PRIMARY KEY,
    nombre VARCHAR(100)
);

CREATE TABLE IF NOT EXISTS empleado(
    idEmpleado INT AUTO_INCREMENT PRIMARY KEY,
    nombre VARCHAR(50),
    apellido VARCHAR(50),
    correo VARCHAR(100),
    fechaNacimiento DATE,
    idPuesto INT,
    FOREIGN KEY (idPuesto) REFERENCES puesto(idPuesto),
    idPais INT,
    FOREIGN KEY (idPais) REFERENCES pais(idPais)
);

CREATE TABLE IF NOT EXISTS reporte(
    idReporte INT AUTO_INCREMENT PRIMARY KEY,
    nombre VARCHAR(100),
    fechaAlta DATETIME DEFAULT CURRENT_TIMESTAMP,
    idEmpleado INT,
    FOREIGN KEY (idEmpleado) REFERENCES empleado(idEmpleado)
);

CREATE TABLE IF NOT EXISTS gasto(
    idGasto INT AUTO_INCREMENT PRIMARY KEY,
    monto FLOAT,
    fecha DATETIME,
    idClasificacion INT,
    FOREIGN KEY (idClasificacion) REFERENCES clasificacionGasto(idClasificacion),
    idReporte INT,
    FOREIGN KEY (idReporte) REFERENCES reporte(idReporte)
);

INSERT INTO pais(nombre) VALUES ('Andorra'),('Angola'),('Anguilla'),('Antarctica'),('Antigua and Barbuda'),('Argentina'),('Armenia'),('Aruba'),('Australia'),('Austria'),('Azerbaijan'),('Bahamas'),('Bahrain'),('Bangladesh'),('Barbados'),('Belarus'),('Belgium'),('Belize'),('Benin'),('Mexico');

INSERT INTO puesto(nombre) VALUES ('Director'),('Gerente'),('Sistemas'),('RH'),('DH'),('Planeacion'),('Mercadotecnia'),('Consultor'),('Puesto 1'),('Puesto 2'),('Puesto 3'),('Puesto 4'),('Puesto 5'),('Puesto 6'),('Puesto 7'),('Puesto 8'),('Puesto 9'),('Puesto 10'),('Puesto 11'),('Puesto 12');

INSERT INTO clasificacionGasto(nombre) VALUES ('Gasolina'),('Hospedaje'),('Papeleria'),('Taxis'),('Transporte aereo'),('Visas'),('Maestria'),('Clasificacion 1'),('Clasificacion 2'),('Clasificacion 3'),('Clasificacion 4'),('Clasificacion 5'),('Clasificacion 6'),('Clasificacion 7'),('Clasificacion 8'),('Clasificacion 9'),('Clasificacion 10'),('Clasificacion 11'),('Clasificacion 12'),('Clasificacion 13');

INSERT INTO empleado(nombre,apellido,correo,fechaNacimiento,idPuesto,idPais) VALUES ('Alan','Salazar','alan.salazar@gmail.com','1994-11-30',1,1),('Pedro','Martinez','pedro.martinez@gmail.com','1994-11-30',2,2),('Juan','Garcia','juan.garcia@gmail.com','1994-11-30',3,3),('Luis','Lopez','luis.lopez@gmail.com','1994-11-30',4,4),('Maria','Gomez','maria.gomez@gmail.com','1994-11-30',5,5),('Daniela','Rodriguez','daniela.rodriguez@gmail.com','1994-11-30',6,6),('Pedro','Garza','pedro.garza@gmail.com','1994-11-30',7,7),('Javier','Acosta','javier.acosta@gmail.com','1994-11-30',8,8),('Ignacio','Barros','ignacio.barros@gmail.com','1994-11-30',9,9),('Mauricio','Diaz','mauricio.diaz@gmail.com','1994-11-30',10,10),('Edgar','Ojeda','edgar.ojeda@gmail.com','1994-11-30',11,11),('Carlos','Rangel','carlos.rangel@gmail.com','1994-11-30',12,12),('Joaquin','Perez','joaquin.perez@gmail.com','1994-11-30',13,13),('Oscar','Moreno','oscar.moreno@gmail.com','1994-11-30',14,14),('Jose','Yuriar','jose.yuriar@gmail.com','1994-11-30',15,15),('Francisco','Luzio','francisco.luzio@gmail.com','1994-11-30',16,16),('Victor','Benavides','victor.benavides@gmail.com','1994-11-30',17,17),('Eduardo','Flores','eduardo.flores@gmail.com','1994-11-30',18,18),('Alejandro','Amaya','alejandro.amaya@gmail.com','1994-11-30',19,19),('Rafel','Ortiz','rafael.ortiz@gmail.com','1994-11-30',20,20);

INSERT INTO reporte(nombre,idEmpleado) VALUES ('Gastos semana 22',1),('Reembolso Maestria',2),('Maleta extra',3),('Gastos semana 24',4),('Gastos semana 25',5),('Gastos semana 26',6),('Gastos semana 27',7),('Gastos semana 28',8),('Gastos semana 29',9),('Gastos semana 30',10),('Gastos semana 31',11),('Gastos semana 32',12),('Gastos semana 33',13),('Gastos semana 34',14),('Gastos semana 35',15),('Gastos semana 36',16),('Gastos semana 37',17),('Gastos semana 38',18),('Gastos semana 39',19),('Gastos semana 40',20);

INSERT INTO gasto(monto,fecha,idClasificacion,idReporte) VALUES (300.95,'2022-09-06',1,1),(125.55,'2022-09-06',2,2),(290.75,'2022-09-07',3,3),(310.95,'2022-09-08',4,4),(320.85,'2022-09-09',5,5),(456.95,'2022-09-10',6,6),(301.35,'2022-09-11',7,7),(150.95,'2022-09-12',8,8),(145.65,'2022-09-13',9,9),(154.33,'2022-09-14',10,10),(900.95,'2022-09-15',11,11),(850.65,'2022-09-16',12,12),(435.95,'2022-09-17',13,13),(130.25,'2022-09-18',14,14),(125.95,'2022-09-19',15,15),(410.85,'2022-09-20',16,16),(500.65,'2022-09-21',17,17),(340.45,'2022-09-22',18,18),(320.95,'2022-09-23',19,19),(320.75,'2022-09-24',20,20);