#
# TABLE STRUCTURE FOR: clasificacionGasto
#
``` sql
DROP TABLE IF EXISTS `clasificacionGasto`;

CREATE TABLE `clasificacionGasto` (
  `idclasificacion` int(11) NOT NULL AUTO_INCREMENT,
  `nombre` varchar(100) COLLATE utf8mb4_unicode_ci DEFAULT NULL,
  PRIMARY KEY (`idclasificacion`)
) ENGINE=InnoDB AUTO_INCREMENT=11 DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_unicode_ci;

INSERT INTO `clasificacionGasto` (`idclasificacion`, `nombre`) VALUES (1, 'similique');
INSERT INTO `clasificacionGasto` (`idclasificacion`, `nombre`) VALUES (2, 'voluptatem');
INSERT INTO `clasificacionGasto` (`idclasificacion`, `nombre`) VALUES (3, 'corrupti');
INSERT INTO `clasificacionGasto` (`idclasificacion`, `nombre`) VALUES (4, 'delectus');
INSERT INTO `clasificacionGasto` (`idclasificacion`, `nombre`) VALUES (5, 'nisi');
INSERT INTO `clasificacionGasto` (`idclasificacion`, `nombre`) VALUES (6, 'quas');
INSERT INTO `clasificacionGasto` (`idclasificacion`, `nombre`) VALUES (7, 'ullam');
INSERT INTO `clasificacionGasto` (`idclasificacion`, `nombre`) VALUES (8, 'fugiat');
INSERT INTO `clasificacionGasto` (`idclasificacion`, `nombre`) VALUES (9, 'autem');
INSERT INTO `clasificacionGasto` (`idclasificacion`, `nombre`) VALUES (10, 'ut');


#
# TABLE STRUCTURE FOR: empleado
#

DROP TABLE IF EXISTS `empleado`;

CREATE TABLE `empleado` (
  `idEmpleado` int(11) NOT NULL AUTO_INCREMENT,
  `nombre` varchar(50) COLLATE utf8mb4_unicode_ci DEFAULT NULL,
  `apellido` varchar(50) COLLATE utf8mb4_unicode_ci DEFAULT NULL,
  `correo` varchar(100) COLLATE utf8mb4_unicode_ci DEFAULT NULL,
  `fechaNacimiento` date DEFAULT NULL,
  `idPuesto` int(11) DEFAULT NULL,
  `idPais` int(11) DEFAULT NULL,
  PRIMARY KEY (`idEmpleado`),
  KEY `idPuesto` (`idPuesto`),
  KEY `idPais` (`idPais`),
  CONSTRAINT `empleado_ibfk_1` FOREIGN KEY (`idPuesto`) REFERENCES `puesto` (`idPuesto`),
  CONSTRAINT `empleado_ibfk_2` FOREIGN KEY (`idPais`) REFERENCES `pais` (`idPais`)
) ENGINE=InnoDB AUTO_INCREMENT=101 DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_unicode_ci;

INSERT INTO `empleado` (`idEmpleado`, `nombre`, `apellido`, `correo`, `fechaNacimiento`, `idPuesto`, `idPais`) VALUES (1, 'Glennie', 'Buckridge', 'arch.strosin@gibson.org', '2009-02-04', 1, 1);
INSERT INTO `empleado` (`idEmpleado`, `nombre`, `apellido`, `correo`, `fechaNacimiento`, `idPuesto`, `idPais`) VALUES (2, 'Verda', 'Schoen', 'ursula.herzog@blanda.com', '1991-04-26', 2, 2);
INSERT INTO `empleado` (`idEmpleado`, `nombre`, `apellido`, `correo`, `fechaNacimiento`, `idPuesto`, `idPais`) VALUES (3, 'Jabari', 'Nader', 'brielle.wisozk@gmail.com', '1978-11-09', 3, 3);
INSERT INTO `empleado` (`idEmpleado`, `nombre`, `apellido`, `correo`, `fechaNacimiento`, `idPuesto`, `idPais`) VALUES (4, 'Flavie', 'Smitham', 'cdibbert@yahoo.com', '2021-02-11', 4, 4);
INSERT INTO `empleado` (`idEmpleado`, `nombre`, `apellido`, `correo`, `fechaNacimiento`, `idPuesto`, `idPais`) VALUES (5, 'Glen', 'Walker', 'dereck40@halvorsonrenner.com', '2014-11-17', 5, 5);
INSERT INTO `empleado` (`idEmpleado`, `nombre`, `apellido`, `correo`, `fechaNacimiento`, `idPuesto`, `idPais`) VALUES (6, 'Shawna', 'Swaniawski', 'gerson99@hotmail.com', '2022-08-03', 6, 6);
INSERT INTO `empleado` (`idEmpleado`, `nombre`, `apellido`, `correo`, `fechaNacimiento`, `idPuesto`, `idPais`) VALUES (7, 'Erika', 'Donnelly', 'tremblay.loyal@feestlemke.com', '2000-11-05', 7, 7);
INSERT INTO `empleado` (`idEmpleado`, `nombre`, `apellido`, `correo`, `fechaNacimiento`, `idPuesto`, `idPais`) VALUES (8, 'Eloise', 'Gleason', 'marlee50@greenschuster.info', '2007-09-11', 8, 8);
INSERT INTO `empleado` (`idEmpleado`, `nombre`, `apellido`, `correo`, `fechaNacimiento`, `idPuesto`, `idPais`) VALUES (9, 'Adeline', 'Blick', 'vita.wisozk@cronin.com', '1983-01-21', 9, 9);
INSERT INTO `empleado` (`idEmpleado`, `nombre`, `apellido`, `correo`, `fechaNacimiento`, `idPuesto`, `idPais`) VALUES (10, 'Alessia', 'Bernhard', 'owiegand@hotmail.com', '1970-02-14', 10, 10);
INSERT INTO `empleado` (`idEmpleado`, `nombre`, `apellido`, `correo`, `fechaNacimiento`, `idPuesto`, `idPais`) VALUES (11, 'Cathryn', 'Mante', 'homenick.celestine@gmail.com', '2018-12-02', 1, 11);
INSERT INTO `empleado` (`idEmpleado`, `nombre`, `apellido`, `correo`, `fechaNacimiento`, `idPuesto`, `idPais`) VALUES (12, 'Amani', 'Koch', 'alfred14@zulauf.org', '1993-02-25', 2, 12);
INSERT INTO `empleado` (`idEmpleado`, `nombre`, `apellido`, `correo`, `fechaNacimiento`, `idPuesto`, `idPais`) VALUES (13, 'Cassandra', 'Morar', 'haley.hilton@hotmail.com', '1981-01-09', 3, 13);
INSERT INTO `empleado` (`idEmpleado`, `nombre`, `apellido`, `correo`, `fechaNacimiento`, `idPuesto`, `idPais`) VALUES (14, 'Audra', 'Halvorson', 'schulist.arvilla@yahoo.com', '2000-08-29', 4, 14);
INSERT INTO `empleado` (`idEmpleado`, `nombre`, `apellido`, `correo`, `fechaNacimiento`, `idPuesto`, `idPais`) VALUES (15, 'Alexys', 'Ritchie', 'ihauck@hotmail.com', '2010-09-28', 5, 15);
INSERT INTO `empleado` (`idEmpleado`, `nombre`, `apellido`, `correo`, `fechaNacimiento`, `idPuesto`, `idPais`) VALUES (16, 'Gerry', 'Zieme', 'bosco.bernadette@blandaortiz.net', '2002-03-25', 6, 16);
INSERT INTO `empleado` (`idEmpleado`, `nombre`, `apellido`, `correo`, `fechaNacimiento`, `idPuesto`, `idPais`) VALUES (17, 'Lia', 'McGlynn', 'nathanial.lebsack@doylebreitenberg.com', '1997-12-27', 7, 17);
INSERT INTO `empleado` (`idEmpleado`, `nombre`, `apellido`, `correo`, `fechaNacimiento`, `idPuesto`, `idPais`) VALUES (18, 'Alexandrea', 'Larson', 'thartmann@olson.info', '1984-01-18', 8, 18);
INSERT INTO `empleado` (`idEmpleado`, `nombre`, `apellido`, `correo`, `fechaNacimiento`, `idPuesto`, `idPais`) VALUES (19, 'Erick', 'Kiehn', 'clifton06@gmail.com', '2009-10-17', 9, 19);
INSERT INTO `empleado` (`idEmpleado`, `nombre`, `apellido`, `correo`, `fechaNacimiento`, `idPuesto`, `idPais`) VALUES (20, 'Ruby', 'Weimann', 'nmayer@gmail.com', '1994-04-30', 10, 20);
INSERT INTO `empleado` (`idEmpleado`, `nombre`, `apellido`, `correo`, `fechaNacimiento`, `idPuesto`, `idPais`) VALUES (21, 'Emmalee', 'Larson', 'ocrona@mayertgerlach.net', '1983-08-22', 1, 21);
INSERT INTO `empleado` (`idEmpleado`, `nombre`, `apellido`, `correo`, `fechaNacimiento`, `idPuesto`, `idPais`) VALUES (22, 'Juston', 'Ratke', 'hahn.jedediah@gmail.com', '1974-04-05', 2, 22);
INSERT INTO `empleado` (`idEmpleado`, `nombre`, `apellido`, `correo`, `fechaNacimiento`, `idPuesto`, `idPais`) VALUES (23, 'Bria', 'Murray', 'abreitenberg@yahoo.com', '1995-07-03', 3, 23);
INSERT INTO `empleado` (`idEmpleado`, `nombre`, `apellido`, `correo`, `fechaNacimiento`, `idPuesto`, `idPais`) VALUES (24, 'Nona', 'Gorczany', 'lucile.pouros@handleannon.info', '2013-11-30', 4, 24);
INSERT INTO `empleado` (`idEmpleado`, `nombre`, `apellido`, `correo`, `fechaNacimiento`, `idPuesto`, `idPais`) VALUES (25, 'Ena', 'Sanford', 'kemmer.bailee@yahoo.com', '1979-06-09', 5, 25);
INSERT INTO `empleado` (`idEmpleado`, `nombre`, `apellido`, `correo`, `fechaNacimiento`, `idPuesto`, `idPais`) VALUES (26, 'Shaniya', 'Daugherty', 'bette.murray@gmail.com', '1989-05-21', 6, 26);
INSERT INTO `empleado` (`idEmpleado`, `nombre`, `apellido`, `correo`, `fechaNacimiento`, `idPuesto`, `idPais`) VALUES (27, 'Westley', 'Schimmel', 'lbraun@schultz.biz', '2010-12-25', 7, 27);
INSERT INTO `empleado` (`idEmpleado`, `nombre`, `apellido`, `correo`, `fechaNacimiento`, `idPuesto`, `idPais`) VALUES (28, 'Nils', 'Leannon', 'titus.wilderman@kling.com', '2003-06-28', 8, 28);
INSERT INTO `empleado` (`idEmpleado`, `nombre`, `apellido`, `correo`, `fechaNacimiento`, `idPuesto`, `idPais`) VALUES (29, 'Cristian', 'Schiller', 'tsimonis@gmail.com', '2009-01-05', 9, 29);
INSERT INTO `empleado` (`idEmpleado`, `nombre`, `apellido`, `correo`, `fechaNacimiento`, `idPuesto`, `idPais`) VALUES (30, 'Barrett', 'Hand', 'feest.jaclyn@batz.biz', '1979-05-26', 10, 30);
INSERT INTO `empleado` (`idEmpleado`, `nombre`, `apellido`, `correo`, `fechaNacimiento`, `idPuesto`, `idPais`) VALUES (31, 'Will', 'Huel', 'jaskolski.brannon@king.com', '1983-05-01', 1, 31);
INSERT INTO `empleado` (`idEmpleado`, `nombre`, `apellido`, `correo`, `fechaNacimiento`, `idPuesto`, `idPais`) VALUES (32, 'Darius', 'Wuckert', 'mckenzie.bridgette@yahoo.com', '1986-12-31', 2, 32);
INSERT INTO `empleado` (`idEmpleado`, `nombre`, `apellido`, `correo`, `fechaNacimiento`, `idPuesto`, `idPais`) VALUES (33, 'Lesly', 'Okuneva', 'uemmerich@schaden.com', '2014-11-17', 3, 33);
INSERT INTO `empleado` (`idEmpleado`, `nombre`, `apellido`, `correo`, `fechaNacimiento`, `idPuesto`, `idPais`) VALUES (34, 'Hayley', 'Toy', 'king.keven@zemlaksauer.info', '2014-11-02', 4, 34);
INSERT INTO `empleado` (`idEmpleado`, `nombre`, `apellido`, `correo`, `fechaNacimiento`, `idPuesto`, `idPais`) VALUES (35, 'Neoma', 'Langworth', 'goyette.loyal@yahoo.com', '2014-06-13', 5, 35);
INSERT INTO `empleado` (`idEmpleado`, `nombre`, `apellido`, `correo`, `fechaNacimiento`, `idPuesto`, `idPais`) VALUES (36, 'Jeramy', 'Little', 'wrowe@hotmail.com', '1971-09-25', 6, 36);
INSERT INTO `empleado` (`idEmpleado`, `nombre`, `apellido`, `correo`, `fechaNacimiento`, `idPuesto`, `idPais`) VALUES (37, 'Rocio', 'Pacocha', 'torrance.beatty@schulist.net', '1989-01-07', 7, 37);
INSERT INTO `empleado` (`idEmpleado`, `nombre`, `apellido`, `correo`, `fechaNacimiento`, `idPuesto`, `idPais`) VALUES (38, 'Stella', 'Lueilwitz', 'gregg.kub@ortiz.com', '2002-06-08', 8, 38);
INSERT INTO `empleado` (`idEmpleado`, `nombre`, `apellido`, `correo`, `fechaNacimiento`, `idPuesto`, `idPais`) VALUES (39, 'Randall', 'Wunsch', 'myrtis.gleichner@skiles.com', '1995-10-05', 9, 39);
INSERT INTO `empleado` (`idEmpleado`, `nombre`, `apellido`, `correo`, `fechaNacimiento`, `idPuesto`, `idPais`) VALUES (40, 'Estrella', 'Fadel', 'becker.rosemarie@gmail.com', '2009-04-10', 10, 40);
INSERT INTO `empleado` (`idEmpleado`, `nombre`, `apellido`, `correo`, `fechaNacimiento`, `idPuesto`, `idPais`) VALUES (41, 'Aron', 'Vandervort', 'rosenbaum.doris@breitenberg.com', '1994-09-30', 1, 41);
INSERT INTO `empleado` (`idEmpleado`, `nombre`, `apellido`, `correo`, `fechaNacimiento`, `idPuesto`, `idPais`) VALUES (42, 'Gilberto', 'Champlin', 'clabadie@harber.org', '2001-09-26', 2, 42);
INSERT INTO `empleado` (`idEmpleado`, `nombre`, `apellido`, `correo`, `fechaNacimiento`, `idPuesto`, `idPais`) VALUES (43, 'Carroll', 'Lockman', 'yrice@hotmail.com', '1979-09-05', 3, 43);
INSERT INTO `empleado` (`idEmpleado`, `nombre`, `apellido`, `correo`, `fechaNacimiento`, `idPuesto`, `idPais`) VALUES (44, 'Haleigh', 'Wisoky', 'qmurphy@schuppe.com', '2018-12-18', 4, 44);
INSERT INTO `empleado` (`idEmpleado`, `nombre`, `apellido`, `correo`, `fechaNacimiento`, `idPuesto`, `idPais`) VALUES (45, 'Precious', 'Watsica', 'jake15@cummings.info', '1987-03-06', 5, 45);
INSERT INTO `empleado` (`idEmpleado`, `nombre`, `apellido`, `correo`, `fechaNacimiento`, `idPuesto`, `idPais`) VALUES (46, 'Scotty', 'Blanda', 'quitzon.tierra@gmail.com', '1983-02-09', 6, 46);
INSERT INTO `empleado` (`idEmpleado`, `nombre`, `apellido`, `correo`, `fechaNacimiento`, `idPuesto`, `idPais`) VALUES (47, 'Alexandro', 'Feeney', 'arlo21@conroyroberts.com', '2011-02-26', 7, 47);
INSERT INTO `empleado` (`idEmpleado`, `nombre`, `apellido`, `correo`, `fechaNacimiento`, `idPuesto`, `idPais`) VALUES (48, 'Kristian', 'Heathcote', 'schmidt.carrie@reichert.org', '2007-04-10', 8, 48);
INSERT INTO `empleado` (`idEmpleado`, `nombre`, `apellido`, `correo`, `fechaNacimiento`, `idPuesto`, `idPais`) VALUES (49, 'Cristian', 'Quigley', 'mcglynn.connie@conroy.biz', '2013-06-29', 9, 49);
INSERT INTO `empleado` (`idEmpleado`, `nombre`, `apellido`, `correo`, `fechaNacimiento`, `idPuesto`, `idPais`) VALUES (50, 'Ladarius', 'Rowe', 'uprosacco@yahoo.com', '1970-08-31', 10, 50);
INSERT INTO `empleado` (`idEmpleado`, `nombre`, `apellido`, `correo`, `fechaNacimiento`, `idPuesto`, `idPais`) VALUES (51, 'Shemar', 'Koch', 'thelma06@hotmail.com', '1980-12-01', 1, 51);
INSERT INTO `empleado` (`idEmpleado`, `nombre`, `apellido`, `correo`, `fechaNacimiento`, `idPuesto`, `idPais`) VALUES (52, 'Evan', 'Gerhold', 'chanelle52@marquardt.org', '2012-03-11', 2, 52);
INSERT INTO `empleado` (`idEmpleado`, `nombre`, `apellido`, `correo`, `fechaNacimiento`, `idPuesto`, `idPais`) VALUES (53, 'Dulce', 'Graham', 'ndaugherty@hotmail.com', '1978-07-04', 3, 53);
INSERT INTO `empleado` (`idEmpleado`, `nombre`, `apellido`, `correo`, `fechaNacimiento`, `idPuesto`, `idPais`) VALUES (54, 'Jevon', 'Krajcik', 'verda.kiehn@hayes.org', '1997-06-10', 4, 54);
INSERT INTO `empleado` (`idEmpleado`, `nombre`, `apellido`, `correo`, `fechaNacimiento`, `idPuesto`, `idPais`) VALUES (55, 'Waldo', 'Walsh', 'adela42@carroll.com', '1996-02-06', 5, 55);
INSERT INTO `empleado` (`idEmpleado`, `nombre`, `apellido`, `correo`, `fechaNacimiento`, `idPuesto`, `idPais`) VALUES (56, 'Nettie', 'Satterfield', 'melba33@hotmail.com', '2010-12-13', 6, 56);
INSERT INTO `empleado` (`idEmpleado`, `nombre`, `apellido`, `correo`, `fechaNacimiento`, `idPuesto`, `idPais`) VALUES (57, 'Lisandro', 'Gerhold', 'mertz.lavon@jacobi.com', '1982-03-28', 7, 57);
INSERT INTO `empleado` (`idEmpleado`, `nombre`, `apellido`, `correo`, `fechaNacimiento`, `idPuesto`, `idPais`) VALUES (58, 'Ross', 'Gislason', 'brant63@hotmail.com', '1974-06-07', 8, 58);
INSERT INTO `empleado` (`idEmpleado`, `nombre`, `apellido`, `correo`, `fechaNacimiento`, `idPuesto`, `idPais`) VALUES (59, 'Nona', 'Mayert', 'olson.aidan@feeney.com', '2016-01-03', 9, 59);
INSERT INTO `empleado` (`idEmpleado`, `nombre`, `apellido`, `correo`, `fechaNacimiento`, `idPuesto`, `idPais`) VALUES (60, 'Zechariah', 'Padberg', 'eduardo84@zulauf.com', '2008-09-06', 10, 60);
INSERT INTO `empleado` (`idEmpleado`, `nombre`, `apellido`, `correo`, `fechaNacimiento`, `idPuesto`, `idPais`) VALUES (61, 'Tracy', 'Rutherford', 'effie85@okon.biz', '1984-12-23', 1, 61);
INSERT INTO `empleado` (`idEmpleado`, `nombre`, `apellido`, `correo`, `fechaNacimiento`, `idPuesto`, `idPais`) VALUES (62, 'Connor', 'Douglas', 'elena.bartell@hotmail.com', '1994-10-26', 2, 62);
INSERT INTO `empleado` (`idEmpleado`, `nombre`, `apellido`, `correo`, `fechaNacimiento`, `idPuesto`, `idPais`) VALUES (63, 'Maudie', 'Rau', 'heidenreich.oda@yahoo.com', '1994-12-07', 3, 63);
INSERT INTO `empleado` (`idEmpleado`, `nombre`, `apellido`, `correo`, `fechaNacimiento`, `idPuesto`, `idPais`) VALUES (64, 'Ethyl', 'Lynch', 'andy.morissette@cruickshankhickle.info', '1984-09-16', 4, 64);
INSERT INTO `empleado` (`idEmpleado`, `nombre`, `apellido`, `correo`, `fechaNacimiento`, `idPuesto`, `idPais`) VALUES (65, 'Maxie', 'Lebsack', 'sporer.daphnee@gmail.com', '1992-06-07', 5, 65);
INSERT INTO `empleado` (`idEmpleado`, `nombre`, `apellido`, `correo`, `fechaNacimiento`, `idPuesto`, `idPais`) VALUES (66, 'Fannie', 'Wyman', 'qhaley@hotmail.com', '1993-11-19', 6, 66);
INSERT INTO `empleado` (`idEmpleado`, `nombre`, `apellido`, `correo`, `fechaNacimiento`, `idPuesto`, `idPais`) VALUES (67, 'Ole', 'Fahey', 'dicki.eleonore@andersonlangosh.org', '1995-05-25', 7, 67);
INSERT INTO `empleado` (`idEmpleado`, `nombre`, `apellido`, `correo`, `fechaNacimiento`, `idPuesto`, `idPais`) VALUES (68, 'Flossie', 'Rempel', 'casey.lemke@gmail.com', '2009-01-22', 8, 68);
INSERT INTO `empleado` (`idEmpleado`, `nombre`, `apellido`, `correo`, `fechaNacimiento`, `idPuesto`, `idPais`) VALUES (69, 'Monserrat', 'Wolf', 'erika22@hotmail.com', '2017-03-09', 9, 69);
INSERT INTO `empleado` (`idEmpleado`, `nombre`, `apellido`, `correo`, `fechaNacimiento`, `idPuesto`, `idPais`) VALUES (70, 'Neil', 'Mills', 'gislason.jasper@yahoo.com', '1996-05-11', 10, 70);
INSERT INTO `empleado` (`idEmpleado`, `nombre`, `apellido`, `correo`, `fechaNacimiento`, `idPuesto`, `idPais`) VALUES (71, 'Geovany', 'Feil', 'hhartmann@gmail.com', '2006-01-05', 1, 71);
INSERT INTO `empleado` (`idEmpleado`, `nombre`, `apellido`, `correo`, `fechaNacimiento`, `idPuesto`, `idPais`) VALUES (72, 'Nova', 'Weimann', 'jordon.wolf@shanahanhayes.info', '1989-11-26', 2, 72);
INSERT INTO `empleado` (`idEmpleado`, `nombre`, `apellido`, `correo`, `fechaNacimiento`, `idPuesto`, `idPais`) VALUES (73, 'Neha', 'Simonis', 'jonathan48@ledner.com', '1974-05-07', 3, 73);
INSERT INTO `empleado` (`idEmpleado`, `nombre`, `apellido`, `correo`, `fechaNacimiento`, `idPuesto`, `idPais`) VALUES (74, 'Cassandra', 'Deckow', 'price.darius@hermiston.net', '1992-07-26', 4, 74);
INSERT INTO `empleado` (`idEmpleado`, `nombre`, `apellido`, `correo`, `fechaNacimiento`, `idPuesto`, `idPais`) VALUES (75, 'Brielle', 'Bruen', 'tyrese13@hotmail.com', '2020-03-31', 5, 75);
INSERT INTO `empleado` (`idEmpleado`, `nombre`, `apellido`, `correo`, `fechaNacimiento`, `idPuesto`, `idPais`) VALUES (76, 'Boyd', 'Stehr', 'wallace83@gmail.com', '2011-05-25', 6, 76);
INSERT INTO `empleado` (`idEmpleado`, `nombre`, `apellido`, `correo`, `fechaNacimiento`, `idPuesto`, `idPais`) VALUES (77, 'Ralph', 'Mohr', 'nolan.kuhic@bernierhodkiewicz.net', '1985-08-03', 7, 77);
INSERT INTO `empleado` (`idEmpleado`, `nombre`, `apellido`, `correo`, `fechaNacimiento`, `idPuesto`, `idPais`) VALUES (78, 'Nasir', 'Welch', 'wilkinson.jaren@yahoo.com', '2003-11-16', 8, 78);
INSERT INTO `empleado` (`idEmpleado`, `nombre`, `apellido`, `correo`, `fechaNacimiento`, `idPuesto`, `idPais`) VALUES (79, 'Modesto', 'Goodwin', 'lmclaughlin@mitchell.biz', '2000-12-03', 9, 79);
INSERT INTO `empleado` (`idEmpleado`, `nombre`, `apellido`, `correo`, `fechaNacimiento`, `idPuesto`, `idPais`) VALUES (80, 'Nicholas', 'Oberbrunner', 'rebeca52@yahoo.com', '1986-02-22', 10, 80);
INSERT INTO `empleado` (`idEmpleado`, `nombre`, `apellido`, `correo`, `fechaNacimiento`, `idPuesto`, `idPais`) VALUES (81, 'Osvaldo', 'Larkin', 'davis.fidel@jaskolski.com', '1978-12-31', 1, 81);
INSERT INTO `empleado` (`idEmpleado`, `nombre`, `apellido`, `correo`, `fechaNacimiento`, `idPuesto`, `idPais`) VALUES (82, 'Deron', 'Hermann', 'nicola.osinski@stehr.net', '2001-08-27', 2, 82);
INSERT INTO `empleado` (`idEmpleado`, `nombre`, `apellido`, `correo`, `fechaNacimiento`, `idPuesto`, `idPais`) VALUES (83, 'Reilly', 'Padberg', 'oveum@gmail.com', '2020-07-01', 3, 83);
INSERT INTO `empleado` (`idEmpleado`, `nombre`, `apellido`, `correo`, `fechaNacimiento`, `idPuesto`, `idPais`) VALUES (84, 'Doug', 'Bechtelar', 'towne.foster@hotmail.com', '1981-10-26', 4, 84);
INSERT INTO `empleado` (`idEmpleado`, `nombre`, `apellido`, `correo`, `fechaNacimiento`, `idPuesto`, `idPais`) VALUES (85, 'Freeda', 'Blanda', 'thompson.janessa@hegmann.com', '1987-11-07', 5, 85);
INSERT INTO `empleado` (`idEmpleado`, `nombre`, `apellido`, `correo`, `fechaNacimiento`, `idPuesto`, `idPais`) VALUES (86, 'Timmothy', 'Lehner', 'mbahringer@hilll.org', '2013-01-05', 6, 86);
INSERT INTO `empleado` (`idEmpleado`, `nombre`, `apellido`, `correo`, `fechaNacimiento`, `idPuesto`, `idPais`) VALUES (87, 'Sammie', 'Kunze', 'stephan.kling@veum.com', '1989-05-31', 7, 87);
INSERT INTO `empleado` (`idEmpleado`, `nombre`, `apellido`, `correo`, `fechaNacimiento`, `idPuesto`, `idPais`) VALUES (88, 'Rossie', 'Schultz', 'marcelino.feest@gmail.com', '1988-12-19', 8, 88);
INSERT INTO `empleado` (`idEmpleado`, `nombre`, `apellido`, `correo`, `fechaNacimiento`, `idPuesto`, `idPais`) VALUES (89, 'Reyna', 'Lockman', 'spencer.keebler@hotmail.com', '2006-03-15', 9, 89);
INSERT INTO `empleado` (`idEmpleado`, `nombre`, `apellido`, `correo`, `fechaNacimiento`, `idPuesto`, `idPais`) VALUES (90, 'Kevin', 'Douglas', 'lwaelchi@hotmail.com', '1999-08-14', 10, 90);
INSERT INTO `empleado` (`idEmpleado`, `nombre`, `apellido`, `correo`, `fechaNacimiento`, `idPuesto`, `idPais`) VALUES (91, 'Paolo', 'Rau', 'bd\'amore@gmail.com', '1984-07-05', 1, 91);
INSERT INTO `empleado` (`idEmpleado`, `nombre`, `apellido`, `correo`, `fechaNacimiento`, `idPuesto`, `idPais`) VALUES (92, 'Myles', 'Buckridge', 'hortense.waters@hotmail.com', '1995-12-14', 2, 92);
INSERT INTO `empleado` (`idEmpleado`, `nombre`, `apellido`, `correo`, `fechaNacimiento`, `idPuesto`, `idPais`) VALUES (93, 'Devonte', 'Schoen', 'king88@hotmail.com', '1988-02-20', 3, 93);
INSERT INTO `empleado` (`idEmpleado`, `nombre`, `apellido`, `correo`, `fechaNacimiento`, `idPuesto`, `idPais`) VALUES (94, 'Jonathan', 'Ernser', 'swift.andy@yahoo.com', '2009-10-11', 4, 94);
INSERT INTO `empleado` (`idEmpleado`, `nombre`, `apellido`, `correo`, `fechaNacimiento`, `idPuesto`, `idPais`) VALUES (95, 'Esperanza', 'Friesen', 'haley.eliza@block.com', '2003-10-31', 5, 95);
INSERT INTO `empleado` (`idEmpleado`, `nombre`, `apellido`, `correo`, `fechaNacimiento`, `idPuesto`, `idPais`) VALUES (96, 'Landen', 'Volkman', 'waldo26@conroy.net', '1971-02-13', 6, 96);
INSERT INTO `empleado` (`idEmpleado`, `nombre`, `apellido`, `correo`, `fechaNacimiento`, `idPuesto`, `idPais`) VALUES (97, 'Garfield', 'Schinner', 'schinner.darrion@hotmail.com', '1985-03-11', 7, 97);
INSERT INTO `empleado` (`idEmpleado`, `nombre`, `apellido`, `correo`, `fechaNacimiento`, `idPuesto`, `idPais`) VALUES (98, 'Angelica', 'Bins', 'huel.mollie@dickens.org', '2013-01-11', 8, 98);
INSERT INTO `empleado` (`idEmpleado`, `nombre`, `apellido`, `correo`, `fechaNacimiento`, `idPuesto`, `idPais`) VALUES (99, 'Clair', 'Funk', 'itzel00@denesik.info', '2012-12-20', 9, 99);
INSERT INTO `empleado` (`idEmpleado`, `nombre`, `apellido`, `correo`, `fechaNacimiento`, `idPuesto`, `idPais`) VALUES (100, 'Berniece', 'Oberbrunner', 'eliane.dickinson@hotmail.com', '1988-02-18', 10, 100);


#
# TABLE STRUCTURE FOR: gasto
#

DROP TABLE IF EXISTS `gasto`;

CREATE TABLE `gasto` (
  `idGasto` int(11) NOT NULL AUTO_INCREMENT,
  `monto` float DEFAULT NULL,
  `fecha` datetime DEFAULT NULL,
  `idClasificacion` int(11) DEFAULT NULL,
  `idReporte` int(11) DEFAULT NULL,
  PRIMARY KEY (`idGasto`),
  KEY `idClasificacion` (`idClasificacion`),
  KEY `idReporte` (`idReporte`),
  CONSTRAINT `gasto_ibfk_1` FOREIGN KEY (`idClasificacion`) REFERENCES `clasificacionGasto` (`idclasificacion`),
  CONSTRAINT `gasto_ibfk_2` FOREIGN KEY (`idReporte`) REFERENCES `reporte` (`idReporte`)
) ENGINE=InnoDB AUTO_INCREMENT=101 DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_unicode_ci;

INSERT INTO `gasto` (`idGasto`, `monto`, `fecha`, `idClasificacion`, `idReporte`) VALUES (1, '295.98', '2009-05-17 02:19:51', 1, 1);
INSERT INTO `gasto` (`idGasto`, `monto`, `fecha`, `idClasificacion`, `idReporte`) VALUES (2, '147.81', '2003-05-14 07:45:41', 2, 2);
INSERT INTO `gasto` (`idGasto`, `monto`, `fecha`, `idClasificacion`, `idReporte`) VALUES (3, '599.95', '1978-07-20 07:52:51', 3, 3);
INSERT INTO `gasto` (`idGasto`, `monto`, `fecha`, `idClasificacion`, `idReporte`) VALUES (4, '780.09', '2006-05-05 19:57:37', 4, 4);
INSERT INTO `gasto` (`idGasto`, `monto`, `fecha`, `idClasificacion`, `idReporte`) VALUES (5, '561.17', '2018-10-30 18:59:05', 5, 5);
INSERT INTO `gasto` (`idGasto`, `monto`, `fecha`, `idClasificacion`, `idReporte`) VALUES (6, '944.93', '1990-10-04 22:25:12', 6, 6);
INSERT INTO `gasto` (`idGasto`, `monto`, `fecha`, `idClasificacion`, `idReporte`) VALUES (7, '575.19', '1979-05-30 21:01:12', 7, 7);
INSERT INTO `gasto` (`idGasto`, `monto`, `fecha`, `idClasificacion`, `idReporte`) VALUES (8, '385.64', '1972-02-24 20:53:17', 8, 8);
INSERT INTO `gasto` (`idGasto`, `monto`, `fecha`, `idClasificacion`, `idReporte`) VALUES (9, '709.26', '1975-04-11 22:34:46', 9, 9);
INSERT INTO `gasto` (`idGasto`, `monto`, `fecha`, `idClasificacion`, `idReporte`) VALUES (10, '808.21', '1996-09-01 20:54:34', 10, 10);
INSERT INTO `gasto` (`idGasto`, `monto`, `fecha`, `idClasificacion`, `idReporte`) VALUES (11, '822.83', '1983-06-01 23:56:32', 1, 11);
INSERT INTO `gasto` (`idGasto`, `monto`, `fecha`, `idClasificacion`, `idReporte`) VALUES (12, '213.58', '2014-04-11 15:19:34', 2, 12);
INSERT INTO `gasto` (`idGasto`, `monto`, `fecha`, `idClasificacion`, `idReporte`) VALUES (13, '786.19', '1999-03-29 23:49:06', 3, 13);
INSERT INTO `gasto` (`idGasto`, `monto`, `fecha`, `idClasificacion`, `idReporte`) VALUES (14, '734.65', '1991-06-06 05:05:57', 4, 14);
INSERT INTO `gasto` (`idGasto`, `monto`, `fecha`, `idClasificacion`, `idReporte`) VALUES (15, '355.06', '2002-05-22 15:47:20', 5, 15);
INSERT INTO `gasto` (`idGasto`, `monto`, `fecha`, `idClasificacion`, `idReporte`) VALUES (16, '911.45', '2001-06-23 18:46:20', 6, 16);
INSERT INTO `gasto` (`idGasto`, `monto`, `fecha`, `idClasificacion`, `idReporte`) VALUES (17, '26.83', '1987-11-18 05:53:43', 7, 17);
INSERT INTO `gasto` (`idGasto`, `monto`, `fecha`, `idClasificacion`, `idReporte`) VALUES (18, '433.08', '2016-09-11 00:50:22', 8, 18);
INSERT INTO `gasto` (`idGasto`, `monto`, `fecha`, `idClasificacion`, `idReporte`) VALUES (19, '257.29', '1977-10-24 07:39:09', 9, 19);
INSERT INTO `gasto` (`idGasto`, `monto`, `fecha`, `idClasificacion`, `idReporte`) VALUES (20, '602.84', '1977-12-12 03:00:45', 10, 20);
INSERT INTO `gasto` (`idGasto`, `monto`, `fecha`, `idClasificacion`, `idReporte`) VALUES (21, '282.27', '2012-07-01 20:50:42', 1, 21);
INSERT INTO `gasto` (`idGasto`, `monto`, `fecha`, `idClasificacion`, `idReporte`) VALUES (22, '231.66', '1995-12-23 17:12:08', 2, 22);
INSERT INTO `gasto` (`idGasto`, `monto`, `fecha`, `idClasificacion`, `idReporte`) VALUES (23, '936.98', '1990-03-08 01:22:16', 3, 23);
INSERT INTO `gasto` (`idGasto`, `monto`, `fecha`, `idClasificacion`, `idReporte`) VALUES (24, '159.39', '2012-10-28 10:24:22', 4, 24);
INSERT INTO `gasto` (`idGasto`, `monto`, `fecha`, `idClasificacion`, `idReporte`) VALUES (25, '361.24', '1983-04-10 17:02:04', 5, 25);
INSERT INTO `gasto` (`idGasto`, `monto`, `fecha`, `idClasificacion`, `idReporte`) VALUES (26, '976.78', '1978-06-28 06:43:16', 6, 26);
INSERT INTO `gasto` (`idGasto`, `monto`, `fecha`, `idClasificacion`, `idReporte`) VALUES (27, '182.51', '1981-12-28 10:39:16', 7, 27);
INSERT INTO `gasto` (`idGasto`, `monto`, `fecha`, `idClasificacion`, `idReporte`) VALUES (28, '463.51', '1987-12-10 00:50:16', 8, 28);
INSERT INTO `gasto` (`idGasto`, `monto`, `fecha`, `idClasificacion`, `idReporte`) VALUES (29, '34.53', '2009-11-25 14:25:35', 9, 29);
INSERT INTO `gasto` (`idGasto`, `monto`, `fecha`, `idClasificacion`, `idReporte`) VALUES (30, '444.59', '1980-09-02 20:01:17', 10, 30);
INSERT INTO `gasto` (`idGasto`, `monto`, `fecha`, `idClasificacion`, `idReporte`) VALUES (31, '348.69', '2012-07-13 17:40:36', 1, 31);
INSERT INTO `gasto` (`idGasto`, `monto`, `fecha`, `idClasificacion`, `idReporte`) VALUES (32, '931.6', '1988-05-26 17:47:21', 2, 32);
INSERT INTO `gasto` (`idGasto`, `monto`, `fecha`, `idClasificacion`, `idReporte`) VALUES (33, '957.25', '2006-06-18 15:21:31', 3, 33);
INSERT INTO `gasto` (`idGasto`, `monto`, `fecha`, `idClasificacion`, `idReporte`) VALUES (34, '487.38', '1999-06-15 03:56:54', 4, 34);
INSERT INTO `gasto` (`idGasto`, `monto`, `fecha`, `idClasificacion`, `idReporte`) VALUES (35, '57.46', '2012-06-08 09:42:11', 5, 35);
INSERT INTO `gasto` (`idGasto`, `monto`, `fecha`, `idClasificacion`, `idReporte`) VALUES (36, '281.9', '2015-08-19 08:33:15', 6, 36);
INSERT INTO `gasto` (`idGasto`, `monto`, `fecha`, `idClasificacion`, `idReporte`) VALUES (37, '895.88', '2009-08-11 11:15:26', 7, 37);
INSERT INTO `gasto` (`idGasto`, `monto`, `fecha`, `idClasificacion`, `idReporte`) VALUES (38, '902.42', '1988-09-20 18:56:32', 8, 38);
INSERT INTO `gasto` (`idGasto`, `monto`, `fecha`, `idClasificacion`, `idReporte`) VALUES (39, '410.43', '2003-07-14 11:56:54', 9, 39);
INSERT INTO `gasto` (`idGasto`, `monto`, `fecha`, `idClasificacion`, `idReporte`) VALUES (40, '153.52', '1984-06-08 02:03:28', 10, 40);
INSERT INTO `gasto` (`idGasto`, `monto`, `fecha`, `idClasificacion`, `idReporte`) VALUES (41, '632.91', '2021-07-02 23:54:38', 1, 41);
INSERT INTO `gasto` (`idGasto`, `monto`, `fecha`, `idClasificacion`, `idReporte`) VALUES (42, '419.24', '1998-01-10 06:51:08', 2, 42);
INSERT INTO `gasto` (`idGasto`, `monto`, `fecha`, `idClasificacion`, `idReporte`) VALUES (43, '323.11', '2012-11-19 10:33:34', 3, 43);
INSERT INTO `gasto` (`idGasto`, `monto`, `fecha`, `idClasificacion`, `idReporte`) VALUES (44, '773.61', '2018-04-21 14:56:46', 4, 44);
INSERT INTO `gasto` (`idGasto`, `monto`, `fecha`, `idClasificacion`, `idReporte`) VALUES (45, '359.8', '2011-12-09 18:55:22', 5, 45);
INSERT INTO `gasto` (`idGasto`, `monto`, `fecha`, `idClasificacion`, `idReporte`) VALUES (46, '382.55', '1984-07-17 07:27:33', 6, 46);
INSERT INTO `gasto` (`idGasto`, `monto`, `fecha`, `idClasificacion`, `idReporte`) VALUES (47, '868.54', '2000-05-06 22:00:00', 7, 47);
INSERT INTO `gasto` (`idGasto`, `monto`, `fecha`, `idClasificacion`, `idReporte`) VALUES (48, '213.91', '1993-08-03 17:46:37', 8, 48);
INSERT INTO `gasto` (`idGasto`, `monto`, `fecha`, `idClasificacion`, `idReporte`) VALUES (49, '663.69', '1984-08-09 09:54:42', 9, 49);
INSERT INTO `gasto` (`idGasto`, `monto`, `fecha`, `idClasificacion`, `idReporte`) VALUES (50, '722.47', '2003-03-19 09:07:27', 10, 50);
INSERT INTO `gasto` (`idGasto`, `monto`, `fecha`, `idClasificacion`, `idReporte`) VALUES (51, '361.05', '2006-05-24 23:53:06', 1, 51);
INSERT INTO `gasto` (`idGasto`, `monto`, `fecha`, `idClasificacion`, `idReporte`) VALUES (52, '51.02', '1988-04-29 12:17:32', 2, 52);
INSERT INTO `gasto` (`idGasto`, `monto`, `fecha`, `idClasificacion`, `idReporte`) VALUES (53, '5.71', '2009-08-27 11:56:38', 3, 53);
INSERT INTO `gasto` (`idGasto`, `monto`, `fecha`, `idClasificacion`, `idReporte`) VALUES (54, '440.74', '2006-08-16 21:39:50', 4, 54);
INSERT INTO `gasto` (`idGasto`, `monto`, `fecha`, `idClasificacion`, `idReporte`) VALUES (55, '108.45', '1976-12-24 07:34:15', 5, 55);
INSERT INTO `gasto` (`idGasto`, `monto`, `fecha`, `idClasificacion`, `idReporte`) VALUES (56, '583.27', '1988-02-28 04:51:48', 6, 56);
INSERT INTO `gasto` (`idGasto`, `monto`, `fecha`, `idClasificacion`, `idReporte`) VALUES (57, '712.21', '2004-09-13 23:28:21', 7, 57);
INSERT INTO `gasto` (`idGasto`, `monto`, `fecha`, `idClasificacion`, `idReporte`) VALUES (58, '316.55', '2006-05-30 02:07:15', 8, 58);
INSERT INTO `gasto` (`idGasto`, `monto`, `fecha`, `idClasificacion`, `idReporte`) VALUES (59, '797.67', '1987-12-23 15:01:25', 9, 59);
INSERT INTO `gasto` (`idGasto`, `monto`, `fecha`, `idClasificacion`, `idReporte`) VALUES (60, '437.34', '2001-05-08 12:09:07', 10, 60);
INSERT INTO `gasto` (`idGasto`, `monto`, `fecha`, `idClasificacion`, `idReporte`) VALUES (61, '378.52', '2021-08-13 01:12:04', 1, 61);
INSERT INTO `gasto` (`idGasto`, `monto`, `fecha`, `idClasificacion`, `idReporte`) VALUES (62, '329.35', '2006-03-12 08:27:45', 2, 62);
INSERT INTO `gasto` (`idGasto`, `monto`, `fecha`, `idClasificacion`, `idReporte`) VALUES (63, '413.91', '1978-09-18 19:11:49', 3, 63);
INSERT INTO `gasto` (`idGasto`, `monto`, `fecha`, `idClasificacion`, `idReporte`) VALUES (64, '111.96', '2011-08-08 02:21:51', 4, 64);
INSERT INTO `gasto` (`idGasto`, `monto`, `fecha`, `idClasificacion`, `idReporte`) VALUES (65, '471.32', '1978-03-07 04:01:30', 5, 65);
INSERT INTO `gasto` (`idGasto`, `monto`, `fecha`, `idClasificacion`, `idReporte`) VALUES (66, '425.76', '1983-02-06 08:15:40', 6, 66);
INSERT INTO `gasto` (`idGasto`, `monto`, `fecha`, `idClasificacion`, `idReporte`) VALUES (67, '4.25', '2017-05-28 15:10:20', 7, 67);
INSERT INTO `gasto` (`idGasto`, `monto`, `fecha`, `idClasificacion`, `idReporte`) VALUES (68, '570.23', '2001-03-10 01:35:18', 8, 68);
INSERT INTO `gasto` (`idGasto`, `monto`, `fecha`, `idClasificacion`, `idReporte`) VALUES (69, '840.14', '2019-12-26 22:15:49', 9, 69);
INSERT INTO `gasto` (`idGasto`, `monto`, `fecha`, `idClasificacion`, `idReporte`) VALUES (70, '74.63', '1982-10-02 06:37:52', 10, 70);
INSERT INTO `gasto` (`idGasto`, `monto`, `fecha`, `idClasificacion`, `idReporte`) VALUES (71, '723.21', '1976-07-23 15:51:59', 1, 71);
INSERT INTO `gasto` (`idGasto`, `monto`, `fecha`, `idClasificacion`, `idReporte`) VALUES (72, '368.11', '2012-02-14 10:24:39', 2, 72);
INSERT INTO `gasto` (`idGasto`, `monto`, `fecha`, `idClasificacion`, `idReporte`) VALUES (73, '269.96', '1977-02-02 13:33:48', 3, 73);
INSERT INTO `gasto` (`idGasto`, `monto`, `fecha`, `idClasificacion`, `idReporte`) VALUES (74, '883.46', '1972-05-19 14:38:39', 4, 74);
INSERT INTO `gasto` (`idGasto`, `monto`, `fecha`, `idClasificacion`, `idReporte`) VALUES (75, '253.68', '2004-02-13 21:52:45', 5, 75);
INSERT INTO `gasto` (`idGasto`, `monto`, `fecha`, `idClasificacion`, `idReporte`) VALUES (76, '524.5', '2020-03-02 14:00:42', 6, 76);
INSERT INTO `gasto` (`idGasto`, `monto`, `fecha`, `idClasificacion`, `idReporte`) VALUES (77, '19.88', '2008-06-05 09:14:33', 7, 77);
INSERT INTO `gasto` (`idGasto`, `monto`, `fecha`, `idClasificacion`, `idReporte`) VALUES (78, '405.56', '2018-03-20 18:36:28', 8, 78);
INSERT INTO `gasto` (`idGasto`, `monto`, `fecha`, `idClasificacion`, `idReporte`) VALUES (79, '723.81', '1996-10-02 16:45:07', 9, 79);
INSERT INTO `gasto` (`idGasto`, `monto`, `fecha`, `idClasificacion`, `idReporte`) VALUES (80, '791.9', '2008-01-17 06:12:24', 10, 80);
INSERT INTO `gasto` (`idGasto`, `monto`, `fecha`, `idClasificacion`, `idReporte`) VALUES (81, '773.3', '2000-09-28 05:36:55', 1, 81);
INSERT INTO `gasto` (`idGasto`, `monto`, `fecha`, `idClasificacion`, `idReporte`) VALUES (82, '788.61', '1977-04-08 07:12:05', 2, 82);
INSERT INTO `gasto` (`idGasto`, `monto`, `fecha`, `idClasificacion`, `idReporte`) VALUES (83, '63.77', '2018-01-10 15:28:00', 3, 83);
INSERT INTO `gasto` (`idGasto`, `monto`, `fecha`, `idClasificacion`, `idReporte`) VALUES (84, '820.46', '1997-07-21 03:48:18', 4, 84);
INSERT INTO `gasto` (`idGasto`, `monto`, `fecha`, `idClasificacion`, `idReporte`) VALUES (85, '642.23', '1970-07-28 19:35:09', 5, 85);
INSERT INTO `gasto` (`idGasto`, `monto`, `fecha`, `idClasificacion`, `idReporte`) VALUES (86, '59.89', '2019-04-06 10:55:31', 6, 86);
INSERT INTO `gasto` (`idGasto`, `monto`, `fecha`, `idClasificacion`, `idReporte`) VALUES (87, '878.27', '1989-07-04 17:36:24', 7, 87);
INSERT INTO `gasto` (`idGasto`, `monto`, `fecha`, `idClasificacion`, `idReporte`) VALUES (88, '555.32', '2021-03-16 15:44:30', 8, 88);
INSERT INTO `gasto` (`idGasto`, `monto`, `fecha`, `idClasificacion`, `idReporte`) VALUES (89, '598.42', '1982-08-21 10:37:02', 9, 89);
INSERT INTO `gasto` (`idGasto`, `monto`, `fecha`, `idClasificacion`, `idReporte`) VALUES (90, '133.54', '2005-02-05 23:33:50', 10, 90);
INSERT INTO `gasto` (`idGasto`, `monto`, `fecha`, `idClasificacion`, `idReporte`) VALUES (91, '26.39', '1974-09-21 17:48:54', 1, 91);
INSERT INTO `gasto` (`idGasto`, `monto`, `fecha`, `idClasificacion`, `idReporte`) VALUES (92, '864.48', '1995-11-10 19:59:16', 2, 92);
INSERT INTO `gasto` (`idGasto`, `monto`, `fecha`, `idClasificacion`, `idReporte`) VALUES (93, '159.53', '1992-12-27 16:23:23', 3, 93);
INSERT INTO `gasto` (`idGasto`, `monto`, `fecha`, `idClasificacion`, `idReporte`) VALUES (94, '782.84', '2015-06-16 00:32:18', 4, 94);
INSERT INTO `gasto` (`idGasto`, `monto`, `fecha`, `idClasificacion`, `idReporte`) VALUES (95, '244.32', '2018-10-16 21:40:57', 5, 95);
INSERT INTO `gasto` (`idGasto`, `monto`, `fecha`, `idClasificacion`, `idReporte`) VALUES (96, '36.48', '2020-02-08 17:15:57', 6, 96);
INSERT INTO `gasto` (`idGasto`, `monto`, `fecha`, `idClasificacion`, `idReporte`) VALUES (97, '62.29', '1981-10-08 11:46:35', 7, 97);
INSERT INTO `gasto` (`idGasto`, `monto`, `fecha`, `idClasificacion`, `idReporte`) VALUES (98, '173.06', '1973-11-25 18:17:16', 8, 98);
INSERT INTO `gasto` (`idGasto`, `monto`, `fecha`, `idClasificacion`, `idReporte`) VALUES (99, '948.96', '2003-12-11 17:12:09', 9, 99);
INSERT INTO `gasto` (`idGasto`, `monto`, `fecha`, `idClasificacion`, `idReporte`) VALUES (100, '396.95', '2007-02-22 17:18:01', 10, 100);


#
# TABLE STRUCTURE FOR: pais
#

DROP TABLE IF EXISTS `pais`;

CREATE TABLE `pais` (
  `idPais` int(11) NOT NULL AUTO_INCREMENT,
  `nombre` varchar(100) COLLATE utf8mb4_unicode_ci DEFAULT NULL,
  PRIMARY KEY (`idPais`)
) ENGINE=InnoDB AUTO_INCREMENT=101 DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_unicode_ci;

INSERT INTO `pais` (`idPais`, `nombre`) VALUES (1, 'Cuba');
INSERT INTO `pais` (`idPais`, `nombre`) VALUES (2, 'Spain');
INSERT INTO `pais` (`idPais`, `nombre`) VALUES (3, 'Denmark');
INSERT INTO `pais` (`idPais`, `nombre`) VALUES (4, 'Portugal');
INSERT INTO `pais` (`idPais`, `nombre`) VALUES (5, 'Fiji');
INSERT INTO `pais` (`idPais`, `nombre`) VALUES (6, 'Liechtenstein');
INSERT INTO `pais` (`idPais`, `nombre`) VALUES (7, 'Bosnia and Herzegovina');
INSERT INTO `pais` (`idPais`, `nombre`) VALUES (8, 'Bermuda');
INSERT INTO `pais` (`idPais`, `nombre`) VALUES (9, 'Nepal');
INSERT INTO `pais` (`idPais`, `nombre`) VALUES (10, 'Sao Tome and Principe');
INSERT INTO `pais` (`idPais`, `nombre`) VALUES (11, 'Russian Federation');
INSERT INTO `pais` (`idPais`, `nombre`) VALUES (12, 'Trinidad and Tobago');
INSERT INTO `pais` (`idPais`, `nombre`) VALUES (13, 'Hong Kong');
INSERT INTO `pais` (`idPais`, `nombre`) VALUES (14, 'Bahrain');
INSERT INTO `pais` (`idPais`, `nombre`) VALUES (15, 'Madagascar');
INSERT INTO `pais` (`idPais`, `nombre`) VALUES (16, 'Faroe Islands');
INSERT INTO `pais` (`idPais`, `nombre`) VALUES (17, 'Western Sahara');
INSERT INTO `pais` (`idPais`, `nombre`) VALUES (18, 'Georgia');
INSERT INTO `pais` (`idPais`, `nombre`) VALUES (19, 'Papua New Guinea');
INSERT INTO `pais` (`idPais`, `nombre`) VALUES (20, 'Holy See (Vatican City State)');
INSERT INTO `pais` (`idPais`, `nombre`) VALUES (21, 'Switzerland');
INSERT INTO `pais` (`idPais`, `nombre`) VALUES (22, 'Sierra Leone');
INSERT INTO `pais` (`idPais`, `nombre`) VALUES (23, 'United States of America');
INSERT INTO `pais` (`idPais`, `nombre`) VALUES (24, 'Aruba');
INSERT INTO `pais` (`idPais`, `nombre`) VALUES (25, 'Guadeloupe');
INSERT INTO `pais` (`idPais`, `nombre`) VALUES (26, 'Kyrgyz Republic');
INSERT INTO `pais` (`idPais`, `nombre`) VALUES (27, 'Mexico');
INSERT INTO `pais` (`idPais`, `nombre`) VALUES (28, 'Cameroon');
INSERT INTO `pais` (`idPais`, `nombre`) VALUES (29, 'China');
INSERT INTO `pais` (`idPais`, `nombre`) VALUES (30, 'Cape Verde');
INSERT INTO `pais` (`idPais`, `nombre`) VALUES (31, 'Bouvet Island (Bouvetoya)');
INSERT INTO `pais` (`idPais`, `nombre`) VALUES (32, 'Guatemala');
INSERT INTO `pais` (`idPais`, `nombre`) VALUES (33, 'Malta');
INSERT INTO `pais` (`idPais`, `nombre`) VALUES (34, 'Angola');
INSERT INTO `pais` (`idPais`, `nombre`) VALUES (35, 'Saint Martin');
INSERT INTO `pais` (`idPais`, `nombre`) VALUES (36, 'Reunion');
INSERT INTO `pais` (`idPais`, `nombre`) VALUES (37, 'Indonesia');
INSERT INTO `pais` (`idPais`, `nombre`) VALUES (38, 'Qatar');
INSERT INTO `pais` (`idPais`, `nombre`) VALUES (39, 'Nigeria');
INSERT INTO `pais` (`idPais`, `nombre`) VALUES (40, 'Japan');
INSERT INTO `pais` (`idPais`, `nombre`) VALUES (41, 'Togo');
INSERT INTO `pais` (`idPais`, `nombre`) VALUES (42, 'Senegal');
INSERT INTO `pais` (`idPais`, `nombre`) VALUES (43, 'Korea');
INSERT INTO `pais` (`idPais`, `nombre`) VALUES (44, 'Ukraine');
INSERT INTO `pais` (`idPais`, `nombre`) VALUES (45, 'Brazil');
INSERT INTO `pais` (`idPais`, `nombre`) VALUES (46, 'Greenland');
INSERT INTO `pais` (`idPais`, `nombre`) VALUES (47, 'Anguilla');
INSERT INTO `pais` (`idPais`, `nombre`) VALUES (48, 'Austria');
INSERT INTO `pais` (`idPais`, `nombre`) VALUES (49, 'Liberia');
INSERT INTO `pais` (`idPais`, `nombre`) VALUES (50, 'Antarctica (the territory South of 60 deg S)');
INSERT INTO `pais` (`idPais`, `nombre`) VALUES (51, 'Congo');
INSERT INTO `pais` (`idPais`, `nombre`) VALUES (52, 'Italy');
INSERT INTO `pais` (`idPais`, `nombre`) VALUES (53, 'Heard Island and McDonald Islands');
INSERT INTO `pais` (`idPais`, `nombre`) VALUES (54, 'Vietnam');
INSERT INTO `pais` (`idPais`, `nombre`) VALUES (55, 'Wallis and Futuna');
INSERT INTO `pais` (`idPais`, `nombre`) VALUES (56, 'Libyan Arab Jamahiriya');
INSERT INTO `pais` (`idPais`, `nombre`) VALUES (57, 'Bangladesh');
INSERT INTO `pais` (`idPais`, `nombre`) VALUES (58, 'Micronesia');
INSERT INTO `pais` (`idPais`, `nombre`) VALUES (59, 'Germany');
INSERT INTO `pais` (`idPais`, `nombre`) VALUES (60, 'Northern Mariana Islands');
INSERT INTO `pais` (`idPais`, `nombre`) VALUES (61, 'South Africa');
INSERT INTO `pais` (`idPais`, `nombre`) VALUES (62, 'Mozambique');
INSERT INTO `pais` (`idPais`, `nombre`) VALUES (63, 'Paraguay');
INSERT INTO `pais` (`idPais`, `nombre`) VALUES (64, 'Canada');
INSERT INTO `pais` (`idPais`, `nombre`) VALUES (65, 'Serbia');
INSERT INTO `pais` (`idPais`, `nombre`) VALUES (66, 'Vanuatu');
INSERT INTO `pais` (`idPais`, `nombre`) VALUES (67, 'Central African Republic');
INSERT INTO `pais` (`idPais`, `nombre`) VALUES (68, 'Nicaragua');
INSERT INTO `pais` (`idPais`, `nombre`) VALUES (69, 'Australia');
INSERT INTO `pais` (`idPais`, `nombre`) VALUES (70, 'Saint Lucia');
INSERT INTO `pais` (`idPais`, `nombre`) VALUES (71, 'Eritrea');
INSERT INTO `pais` (`idPais`, `nombre`) VALUES (72, 'Kenya');
INSERT INTO `pais` (`idPais`, `nombre`) VALUES (73, 'United Arab Emirates');
INSERT INTO `pais` (`idPais`, `nombre`) VALUES (74, 'Monaco');
INSERT INTO `pais` (`idPais`, `nombre`) VALUES (75, 'Botswana');
INSERT INTO `pais` (`idPais`, `nombre`) VALUES (76, 'San Marino');
INSERT INTO `pais` (`idPais`, `nombre`) VALUES (77, 'Zimbabwe');
INSERT INTO `pais` (`idPais`, `nombre`) VALUES (78, 'Dominican Republic');
INSERT INTO `pais` (`idPais`, `nombre`) VALUES (79, 'Guinea');
INSERT INTO `pais` (`idPais`, `nombre`) VALUES (80, 'Croatia');
INSERT INTO `pais` (`idPais`, `nombre`) VALUES (81, 'Finland');
INSERT INTO `pais` (`idPais`, `nombre`) VALUES (82, 'Morocco');
INSERT INTO `pais` (`idPais`, `nombre`) VALUES (83, 'Zambia');
INSERT INTO `pais` (`idPais`, `nombre`) VALUES (84, 'Kuwait');
INSERT INTO `pais` (`idPais`, `nombre`) VALUES (85, 'Malaysia');
INSERT INTO `pais` (`idPais`, `nombre`) VALUES (86, 'Kazakhstan');
INSERT INTO `pais` (`idPais`, `nombre`) VALUES (87, 'Bhutan');
INSERT INTO `pais` (`idPais`, `nombre`) VALUES (88, 'Mali');
INSERT INTO `pais` (`idPais`, `nombre`) VALUES (89, 'French Southern Territories');
INSERT INTO `pais` (`idPais`, `nombre`) VALUES (90, 'New Caledonia');
INSERT INTO `pais` (`idPais`, `nombre`) VALUES (91, 'Brunei Darussalam');
INSERT INTO `pais` (`idPais`, `nombre`) VALUES (92, 'New Zealand');
INSERT INTO `pais` (`idPais`, `nombre`) VALUES (93, 'Puerto Rico');
INSERT INTO `pais` (`idPais`, `nombre`) VALUES (94, 'United Kingdom');
INSERT INTO `pais` (`idPais`, `nombre`) VALUES (95, 'Comoros');
INSERT INTO `pais` (`idPais`, `nombre`) VALUES (96, 'Mongolia');
INSERT INTO `pais` (`idPais`, `nombre`) VALUES (97, 'Guinea-Bissau');
INSERT INTO `pais` (`idPais`, `nombre`) VALUES (98, 'Iran');
INSERT INTO `pais` (`idPais`, `nombre`) VALUES (99, 'Thailand');
INSERT INTO `pais` (`idPais`, `nombre`) VALUES (100, 'Sweden');


#
# TABLE STRUCTURE FOR: puesto
#

DROP TABLE IF EXISTS `puesto`;

CREATE TABLE `puesto` (
  `idPuesto` int(11) NOT NULL AUTO_INCREMENT,
  `nombre` varchar(100) COLLATE utf8mb4_unicode_ci DEFAULT NULL,
  PRIMARY KEY (`idPuesto`)
) ENGINE=InnoDB AUTO_INCREMENT=11 DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_unicode_ci;

INSERT INTO `puesto` (`idPuesto`, `nombre`) VALUES (1, 'Rowe, Fahey and Gutkowski');
INSERT INTO `puesto` (`idPuesto`, `nombre`) VALUES (2, 'Crist-Lind');
INSERT INTO `puesto` (`idPuesto`, `nombre`) VALUES (3, 'Terry, Mertz and Nader');
INSERT INTO `puesto` (`idPuesto`, `nombre`) VALUES (4, 'Toy PLC');
INSERT INTO `puesto` (`idPuesto`, `nombre`) VALUES (5, 'Armstrong Group');
INSERT INTO `puesto` (`idPuesto`, `nombre`) VALUES (6, 'Bogan-Larson');
INSERT INTO `puesto` (`idPuesto`, `nombre`) VALUES (7, 'Yost Inc');
INSERT INTO `puesto` (`idPuesto`, `nombre`) VALUES (8, 'Stokes-Abernathy');
INSERT INTO `puesto` (`idPuesto`, `nombre`) VALUES (9, 'Torp-Rosenbaum');
INSERT INTO `puesto` (`idPuesto`, `nombre`) VALUES (10, 'Morissette-Morar');


#
# TABLE STRUCTURE FOR: reporte
#

DROP TABLE IF EXISTS `reporte`;

CREATE TABLE `reporte` (
  `idReporte` int(11) NOT NULL AUTO_INCREMENT,
  `nombre` varchar(100) COLLATE utf8mb4_unicode_ci DEFAULT NULL,
  `fechaAlta` datetime DEFAULT current_timestamp(),
  `idEmpleado` int(11) DEFAULT NULL,
  PRIMARY KEY (`idReporte`),
  KEY `idEmpleado` (`idEmpleado`),
  CONSTRAINT `reporte_ibfk_1` FOREIGN KEY (`idEmpleado`) REFERENCES `empleado` (`idEmpleado`)
) ENGINE=InnoDB AUTO_INCREMENT=101 DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_unicode_ci;

INSERT INTO `reporte` (`idReporte`, `nombre`, `fechaAlta`, `idEmpleado`) VALUES (1, 'Rerum eveniet facilis eligendi libero. Excepturi ipsam quo voluptatem laudantium aliquam. Cum aut vo', '1993-12-09 11:57:23', 1);
INSERT INTO `reporte` (`idReporte`, `nombre`, `fechaAlta`, `idEmpleado`) VALUES (2, 'Doloremque soluta fugiat illo omnis numquam dolorem reprehenderit sunt. Corrupti autem ea quia aut e', '1989-11-15 22:47:27', 2);
INSERT INTO `reporte` (`idReporte`, `nombre`, `fechaAlta`, `idEmpleado`) VALUES (3, 'Aliquam omnis omnis cumque nemo. Qui autem totam veritatis excepturi consequuntur. Iste adipisci des', '1989-09-19 11:12:03', 3);
INSERT INTO `reporte` (`idReporte`, `nombre`, `fechaAlta`, `idEmpleado`) VALUES (4, 'Aut unde atque sit et blanditiis voluptatem sit. Provident nemo aut ut illo. Non occaecati nemo qui ', '2003-02-27 04:26:49', 4);
INSERT INTO `reporte` (`idReporte`, `nombre`, `fechaAlta`, `idEmpleado`) VALUES (5, 'Libero nulla autem exercitationem. Adipisci enim doloremque voluptate explicabo explicabo atque sed.', '1999-11-06 18:57:53', 5);
INSERT INTO `reporte` (`idReporte`, `nombre`, `fechaAlta`, `idEmpleado`) VALUES (6, 'Perspiciatis dolores iusto praesentium quo ea. Deleniti aut est possimus. Tempore quis occaecati dol', '1982-11-17 14:18:51', 6);
INSERT INTO `reporte` (`idReporte`, `nombre`, `fechaAlta`, `idEmpleado`) VALUES (7, 'Quia ullam velit quia expedita. Et voluptate aliquid id alias inventore quis molestiae. Neque quia q', '2014-12-16 14:29:17', 7);
INSERT INTO `reporte` (`idReporte`, `nombre`, `fechaAlta`, `idEmpleado`) VALUES (8, 'Aut accusantium natus quia sed. Illum sunt aut animi corrupti ex nihil. Delectus amet voluptate dolo', '2010-03-20 18:44:05', 8);
INSERT INTO `reporte` (`idReporte`, `nombre`, `fechaAlta`, `idEmpleado`) VALUES (9, 'In nemo et ipsam est inventore expedita voluptas. Natus qui nam non et quia aut saepe est. Corporis ', '1992-01-21 04:25:07', 9);
INSERT INTO `reporte` (`idReporte`, `nombre`, `fechaAlta`, `idEmpleado`) VALUES (10, 'Incidunt voluptatem aspernatur et voluptatem. Autem quisquam eos vero quaerat et aspernatur quia mol', '1976-11-16 09:16:10', 10);
INSERT INTO `reporte` (`idReporte`, `nombre`, `fechaAlta`, `idEmpleado`) VALUES (11, 'Explicabo quaerat doloremque rerum voluptatem et. Quia animi quidem dignissimos temporibus. At omnis', '1977-03-06 10:01:19', 11);
INSERT INTO `reporte` (`idReporte`, `nombre`, `fechaAlta`, `idEmpleado`) VALUES (12, 'Sit veniam pariatur earum commodi et fugiat facilis. Ut dolorem voluptatem sit consequatur aut dolor', '1994-02-11 08:07:07', 12);
INSERT INTO `reporte` (`idReporte`, `nombre`, `fechaAlta`, `idEmpleado`) VALUES (13, 'Totam et voluptate officia et excepturi repudiandae. Vitae est eum quas. Nesciunt facere quia et pra', '1984-12-20 19:00:21', 13);
INSERT INTO `reporte` (`idReporte`, `nombre`, `fechaAlta`, `idEmpleado`) VALUES (14, 'Laboriosam aliquid aut corrupti consequuntur aut repellat minima. Voluptas aut consequatur omnis err', '1999-04-08 15:18:39', 14);
INSERT INTO `reporte` (`idReporte`, `nombre`, `fechaAlta`, `idEmpleado`) VALUES (15, 'Beatae ipsa minima rem occaecati neque. Magnam minima eligendi quo earum sed.', '2015-12-15 18:50:33', 15);
INSERT INTO `reporte` (`idReporte`, `nombre`, `fechaAlta`, `idEmpleado`) VALUES (16, 'Consequatur quia ipsa incidunt unde assumenda sit animi. Illo in error labore. Ut nemo est sequi. Fa', '2015-12-20 08:51:49', 16);
INSERT INTO `reporte` (`idReporte`, `nombre`, `fechaAlta`, `idEmpleado`) VALUES (17, 'Esse consectetur tenetur iusto eum adipisci vel architecto. Qui vero totam mollitia. Omnis minus et ', '1999-11-28 23:17:17', 17);
INSERT INTO `reporte` (`idReporte`, `nombre`, `fechaAlta`, `idEmpleado`) VALUES (18, 'Iste sint et consequatur laborum. Cupiditate laudantium facere fugit. Et amet doloribus consequatur ', '1994-12-29 15:38:26', 18);
INSERT INTO `reporte` (`idReporte`, `nombre`, `fechaAlta`, `idEmpleado`) VALUES (19, 'Doloribus quisquam corrupti quibusdam minus molestias ut culpa. Earum voluptatem suscipit atque volu', '1970-10-04 01:02:45', 19);
INSERT INTO `reporte` (`idReporte`, `nombre`, `fechaAlta`, `idEmpleado`) VALUES (20, 'Magni neque voluptatum molestiae accusantium voluptatem. Similique nulla veritatis quam temporibus e', '2010-11-06 19:54:32', 20);
INSERT INTO `reporte` (`idReporte`, `nombre`, `fechaAlta`, `idEmpleado`) VALUES (21, 'Similique recusandae dolores eius est. Rerum numquam vel eius. Harum molestiae omnis ea magnam.\nDolo', '1979-08-27 18:39:25', 21);
INSERT INTO `reporte` (`idReporte`, `nombre`, `fechaAlta`, `idEmpleado`) VALUES (22, 'Soluta quisquam consequatur qui temporibus. Eaque aut temporibus impedit qui quis esse suscipit. Rec', '2012-03-25 21:48:02', 22);
INSERT INTO `reporte` (`idReporte`, `nombre`, `fechaAlta`, `idEmpleado`) VALUES (23, 'Non cum quis totam expedita odit qui. Aut rerum voluptas molestiae iusto. Molestias non sit sit laud', '1998-10-17 07:18:54', 23);
INSERT INTO `reporte` (`idReporte`, `nombre`, `fechaAlta`, `idEmpleado`) VALUES (24, 'Ea accusamus sed laudantium non quae magnam qui. Sit nam repellat dolor recusandae aut. Corrupti est', '1975-01-01 15:33:03', 24);
INSERT INTO `reporte` (`idReporte`, `nombre`, `fechaAlta`, `idEmpleado`) VALUES (25, 'Laudantium et temporibus nulla magni ut mollitia sed. Quis alias quod et minus. Et esse ab tempore a', '2013-08-29 15:11:16', 25);
INSERT INTO `reporte` (`idReporte`, `nombre`, `fechaAlta`, `idEmpleado`) VALUES (26, 'Voluptas minus laborum illo est. Ipsam praesentium at repellendus ut natus. Illum ut rerum sint et.', '2015-01-04 20:16:39', 26);
INSERT INTO `reporte` (`idReporte`, `nombre`, `fechaAlta`, `idEmpleado`) VALUES (27, 'Explicabo dolorem unde sunt eligendi. Blanditiis aut possimus deserunt numquam placeat voluptatem en', '1995-06-29 09:35:07', 27);
INSERT INTO `reporte` (`idReporte`, `nombre`, `fechaAlta`, `idEmpleado`) VALUES (28, 'Laborum sed illo culpa consequatur voluptas iste rerum. Reiciendis quibusdam et dolore sed minima ip', '1970-03-22 13:45:34', 28);
INSERT INTO `reporte` (`idReporte`, `nombre`, `fechaAlta`, `idEmpleado`) VALUES (29, 'Sint suscipit ducimus impedit molestias non sit repellat. Porro voluptatem ab saepe earum. Debitis n', '1981-05-18 10:33:21', 29);
INSERT INTO `reporte` (`idReporte`, `nombre`, `fechaAlta`, `idEmpleado`) VALUES (30, 'Eius debitis eius voluptatem molestiae. Architecto doloremque nam aut distinctio occaecati.', '2010-07-09 19:55:48', 30);
INSERT INTO `reporte` (`idReporte`, `nombre`, `fechaAlta`, `idEmpleado`) VALUES (31, 'Perspiciatis voluptate aut praesentium dolorem soluta. Sapiente sunt et praesentium dolorem. Debitis', '1974-05-15 21:57:46', 31);
INSERT INTO `reporte` (`idReporte`, `nombre`, `fechaAlta`, `idEmpleado`) VALUES (32, 'Repudiandae qui vel quidem et sunt et ut et. Ratione similique est impedit distinctio beatae. Ex ass', '2004-04-22 07:37:59', 32);
INSERT INTO `reporte` (`idReporte`, `nombre`, `fechaAlta`, `idEmpleado`) VALUES (33, 'Rerum saepe unde laborum numquam ratione quae voluptas. Quisquam porro earum vel pariatur commodi es', '1990-05-04 23:35:57', 33);
INSERT INTO `reporte` (`idReporte`, `nombre`, `fechaAlta`, `idEmpleado`) VALUES (34, 'Sit ut non veritatis et nemo natus vitae. Numquam excepturi doloremque a odio consequatur ad. Ipsum ', '1972-06-06 16:51:38', 34);
INSERT INTO `reporte` (`idReporte`, `nombre`, `fechaAlta`, `idEmpleado`) VALUES (35, 'Sunt praesentium ut ab neque delectus exercitationem. Labore odit amet consequatur voluptate ipsa ut', '1975-11-29 04:42:51', 35);
INSERT INTO `reporte` (`idReporte`, `nombre`, `fechaAlta`, `idEmpleado`) VALUES (36, 'Error dicta ea fugiat non dignissimos autem consequatur. Distinctio nisi magni in soluta eum et dict', '2000-07-04 20:43:17', 36);
INSERT INTO `reporte` (`idReporte`, `nombre`, `fechaAlta`, `idEmpleado`) VALUES (37, 'Repudiandae ducimus eveniet enim. Sint quod ipsum non eum dolor voluptatibus sint. Eaque voluptatem ', '2000-02-28 06:23:03', 37);
INSERT INTO `reporte` (`idReporte`, `nombre`, `fechaAlta`, `idEmpleado`) VALUES (38, 'Quo laborum aut laudantium quia earum consequatur ipsum. Sint dolor ut aspernatur adipisci odit. Har', '2017-06-30 14:20:27', 38);
INSERT INTO `reporte` (`idReporte`, `nombre`, `fechaAlta`, `idEmpleado`) VALUES (39, 'Aut eveniet eum tempore. Sint ut praesentium velit facilis inventore id. Non est soluta autem cupidi', '2007-05-02 17:44:16', 39);
INSERT INTO `reporte` (`idReporte`, `nombre`, `fechaAlta`, `idEmpleado`) VALUES (40, 'Non ratione ea rerum ut. Omnis vel velit officiis repellendus voluptas qui nihil. Illo et voluptatem', '2006-09-12 11:50:35', 40);
INSERT INTO `reporte` (`idReporte`, `nombre`, `fechaAlta`, `idEmpleado`) VALUES (41, 'Facere magni exercitationem assumenda qui. Rem tempore ut ex velit enim veniam. Omnis adipisci tenet', '2001-07-13 10:32:04', 41);
INSERT INTO `reporte` (`idReporte`, `nombre`, `fechaAlta`, `idEmpleado`) VALUES (42, 'Eum veritatis fugiat distinctio expedita aut qui voluptatibus. In delectus labore nobis sunt labore ', '2004-10-01 03:53:30', 42);
INSERT INTO `reporte` (`idReporte`, `nombre`, `fechaAlta`, `idEmpleado`) VALUES (43, 'Labore omnis quos exercitationem quis et maxime. Ut et aut dolorem cum itaque. Cupiditate et necessi', '1984-06-01 07:43:45', 43);
INSERT INTO `reporte` (`idReporte`, `nombre`, `fechaAlta`, `idEmpleado`) VALUES (44, 'Commodi dolor vel cupiditate reprehenderit aliquam ratione molestias. Dolorem consequatur sint rerum', '1988-12-09 16:21:03', 44);
INSERT INTO `reporte` (`idReporte`, `nombre`, `fechaAlta`, `idEmpleado`) VALUES (45, 'Dicta molestiae consequatur nobis sequi sit quia. Quis qui voluptatem quo autem. Maiores deserunt si', '1973-04-14 08:37:54', 45);
INSERT INTO `reporte` (`idReporte`, `nombre`, `fechaAlta`, `idEmpleado`) VALUES (46, 'Odio est laborum numquam id. Dolores voluptatem aliquid iste accusantium ut. Minus quaerat tenetur s', '1997-07-25 10:37:15', 46);
INSERT INTO `reporte` (`idReporte`, `nombre`, `fechaAlta`, `idEmpleado`) VALUES (47, 'Similique omnis corrupti esse non ut a. Ut atque ea aut similique quasi odio. Nemo suscipit molestia', '2015-03-02 21:22:12', 47);
INSERT INTO `reporte` (`idReporte`, `nombre`, `fechaAlta`, `idEmpleado`) VALUES (48, 'Repudiandae esse distinctio dicta eveniet velit voluptas soluta. Dolores et est suscipit repudiandae', '1998-11-17 17:33:55', 48);
INSERT INTO `reporte` (`idReporte`, `nombre`, `fechaAlta`, `idEmpleado`) VALUES (49, 'Esse quod labore voluptatem atque fuga similique ipsa. Esse incidunt tempora esse libero voluptates.', '1979-04-04 05:19:53', 49);
INSERT INTO `reporte` (`idReporte`, `nombre`, `fechaAlta`, `idEmpleado`) VALUES (50, 'Dolores odit dolorem omnis ea aperiam nisi. Aut itaque vel commodi odit. Vel laudantium magnam et om', '2000-11-30 02:44:39', 50);
INSERT INTO `reporte` (`idReporte`, `nombre`, `fechaAlta`, `idEmpleado`) VALUES (51, 'Quis voluptatum consectetur accusantium nihil. Sequi vitae placeat dolorum vel id explicabo corporis', '1988-08-27 03:00:51', 51);
INSERT INTO `reporte` (`idReporte`, `nombre`, `fechaAlta`, `idEmpleado`) VALUES (52, 'Ipsam saepe odio assumenda nobis. Eum est quia sunt. Veritatis eius est dolor accusantium. Quia et u', '1988-04-28 07:04:15', 52);
INSERT INTO `reporte` (`idReporte`, `nombre`, `fechaAlta`, `idEmpleado`) VALUES (53, 'Unde et eaque laudantium quam earum placeat. Ipsa labore ab voluptates rerum. Aspernatur non magnam ', '2011-09-12 14:38:53', 53);
INSERT INTO `reporte` (`idReporte`, `nombre`, `fechaAlta`, `idEmpleado`) VALUES (54, 'Voluptatibus aut alias dolor. Sint quaerat sed qui omnis. Placeat repellendus quis temporibus harum ', '2014-10-06 02:17:32', 54);
INSERT INTO `reporte` (`idReporte`, `nombre`, `fechaAlta`, `idEmpleado`) VALUES (55, 'Ut fugit quas quis explicabo in labore. Eos porro a placeat est libero quibusdam in ut. Officia eaqu', '2013-09-20 20:49:06', 55);
INSERT INTO `reporte` (`idReporte`, `nombre`, `fechaAlta`, `idEmpleado`) VALUES (56, 'Natus voluptatem est quas maiores est doloremque dignissimos ratione. Officia nam cumque nam aut. Qu', '2013-09-27 10:57:26', 56);
INSERT INTO `reporte` (`idReporte`, `nombre`, `fechaAlta`, `idEmpleado`) VALUES (57, 'Omnis tenetur in occaecati quod. Aspernatur repellat in consequatur aut ut fuga quo. Suscipit doloru', '1982-01-16 12:24:52', 57);
INSERT INTO `reporte` (`idReporte`, `nombre`, `fechaAlta`, `idEmpleado`) VALUES (58, 'Fuga ad nihil maxime quis maiores rerum. Doloribus et voluptas optio quia. Repellat totam consequatu', '2018-09-18 15:55:35', 58);
INSERT INTO `reporte` (`idReporte`, `nombre`, `fechaAlta`, `idEmpleado`) VALUES (59, 'Accusamus repudiandae itaque molestiae officiis. Earum iste natus corrupti maxime. Omnis optio tempo', '1999-09-19 05:37:52', 59);
INSERT INTO `reporte` (`idReporte`, `nombre`, `fechaAlta`, `idEmpleado`) VALUES (60, 'Eaque ea quis et est error. Consequuntur et inventore magnam dolore unde voluptate quo totam. Quod a', '2005-08-22 18:11:50', 60);
INSERT INTO `reporte` (`idReporte`, `nombre`, `fechaAlta`, `idEmpleado`) VALUES (61, 'Quasi quia expedita quis officiis sapiente. In nobis minus officia voluptas. Atque harum facere mini', '2001-03-23 04:52:11', 61);
INSERT INTO `reporte` (`idReporte`, `nombre`, `fechaAlta`, `idEmpleado`) VALUES (62, 'Quos alias eum qui officiis. Velit nam at tempore mollitia omnis. Et repudiandae totam expedita iust', '2011-07-11 18:07:11', 62);
INSERT INTO `reporte` (`idReporte`, `nombre`, `fechaAlta`, `idEmpleado`) VALUES (63, 'Dolor et recusandae inventore non. Doloribus necessitatibus est qui omnis qui placeat eveniet harum.', '1997-07-27 16:26:57', 63);
INSERT INTO `reporte` (`idReporte`, `nombre`, `fechaAlta`, `idEmpleado`) VALUES (64, 'Ut praesentium atque culpa voluptatem. Accusamus suscipit est id debitis dolore. Soluta temporibus l', '2001-10-19 10:52:18', 64);
INSERT INTO `reporte` (`idReporte`, `nombre`, `fechaAlta`, `idEmpleado`) VALUES (65, 'Sequi molestiae commodi doloribus delectus dolorem voluptates ex. Asperiores facilis sit qui aut mol', '1997-03-14 06:43:21', 65);
INSERT INTO `reporte` (`idReporte`, `nombre`, `fechaAlta`, `idEmpleado`) VALUES (66, 'Labore dolor rerum deserunt nostrum sit unde. Ut distinctio deleniti sunt rerum. Sequi provident opt', '2010-11-09 19:29:32', 66);
INSERT INTO `reporte` (`idReporte`, `nombre`, `fechaAlta`, `idEmpleado`) VALUES (67, 'Autem dolor animi ut sapiente vel laudantium. Eos et nostrum sunt ducimus voluptas voluptas. Dicta i', '1981-11-22 11:13:40', 67);
INSERT INTO `reporte` (`idReporte`, `nombre`, `fechaAlta`, `idEmpleado`) VALUES (68, 'Ratione voluptatem et minima ut qui quibusdam recusandae. Amet ut rerum veniam nulla ut ut. Officiis', '2008-01-11 13:35:57', 68);
INSERT INTO `reporte` (`idReporte`, `nombre`, `fechaAlta`, `idEmpleado`) VALUES (69, 'Sed molestiae possimus fugiat quibusdam magnam et error. Voluptatum ut quam eos iste tenetur volupta', '2001-04-14 06:11:52', 69);
INSERT INTO `reporte` (`idReporte`, `nombre`, `fechaAlta`, `idEmpleado`) VALUES (70, 'Facere asperiores dolorum dolorem nam ipsa error. Tenetur porro minus tempore perferendis velit occa', '2010-11-29 12:06:57', 70);
INSERT INTO `reporte` (`idReporte`, `nombre`, `fechaAlta`, `idEmpleado`) VALUES (71, 'Eos eveniet et asperiores suscipit reiciendis. Tempora est saepe ut dolores corrupti adipisci. Dolor', '1985-06-10 07:30:29', 71);
INSERT INTO `reporte` (`idReporte`, `nombre`, `fechaAlta`, `idEmpleado`) VALUES (72, 'Fuga cum dolores fuga ut praesentium. Cum quaerat natus tempore voluptas. Harum deleniti laudantium ', '2006-11-13 01:47:18', 72);
INSERT INTO `reporte` (`idReporte`, `nombre`, `fechaAlta`, `idEmpleado`) VALUES (73, 'Omnis unde omnis ut. Eaque vel cum vel quia in eum. Laboriosam nesciunt laboriosam commodi possimus ', '1976-09-20 09:29:45', 73);
INSERT INTO `reporte` (`idReporte`, `nombre`, `fechaAlta`, `idEmpleado`) VALUES (74, 'Facilis fugiat dolor repellendus. Doloribus consequatur dolore ea officia dolorum libero pariatur.', '1993-12-02 02:05:38', 74);
INSERT INTO `reporte` (`idReporte`, `nombre`, `fechaAlta`, `idEmpleado`) VALUES (75, 'Blanditiis soluta eius nesciunt eos vel est. Unde maxime quibusdam doloremque non accusamus. Eaque d', '1995-11-12 13:53:58', 75);
INSERT INTO `reporte` (`idReporte`, `nombre`, `fechaAlta`, `idEmpleado`) VALUES (76, 'Voluptas debitis eligendi laudantium aut nam repudiandae. Et perferendis id sed est. Ducimus sit qui', '2009-02-09 14:11:23', 76);
INSERT INTO `reporte` (`idReporte`, `nombre`, `fechaAlta`, `idEmpleado`) VALUES (77, 'Et cum suscipit corporis. Sed beatae qui ut. Nihil adipisci voluptates hic quasi eaque facilis moles', '2016-01-24 18:57:32', 77);
INSERT INTO `reporte` (`idReporte`, `nombre`, `fechaAlta`, `idEmpleado`) VALUES (78, 'Et harum sed id quos. Doloribus iusto voluptatem quaerat architecto tenetur. Dicta saepe aspernatur ', '2011-12-16 17:34:46', 78);
INSERT INTO `reporte` (`idReporte`, `nombre`, `fechaAlta`, `idEmpleado`) VALUES (79, 'Et officiis eos quis quia aperiam dolores aspernatur. Veritatis aspernatur voluptate sit aliquam. Qu', '1970-09-04 12:27:34', 79);
INSERT INTO `reporte` (`idReporte`, `nombre`, `fechaAlta`, `idEmpleado`) VALUES (80, 'Laboriosam ad accusantium molestiae corrupti. Provident et nihil est ea deserunt. Eum suscipit dolor', '2015-08-30 14:04:22', 80);
INSERT INTO `reporte` (`idReporte`, `nombre`, `fechaAlta`, `idEmpleado`) VALUES (81, 'Voluptas ea omnis vel et. Vitae quo est voluptate id quo minima est quis. Neque fuga in ipsum occaec', '1972-06-26 00:37:17', 81);
INSERT INTO `reporte` (`idReporte`, `nombre`, `fechaAlta`, `idEmpleado`) VALUES (82, 'Praesentium et blanditiis commodi et quam qui qui. Pariatur est dolorum velit consequatur consequatu', '2017-11-06 18:06:04', 82);
INSERT INTO `reporte` (`idReporte`, `nombre`, `fechaAlta`, `idEmpleado`) VALUES (83, 'Est nostrum quo doloribus veniam omnis blanditiis ut eos. Sint rerum sed necessitatibus. Voluptatem ', '2014-07-03 08:53:07', 83);
INSERT INTO `reporte` (`idReporte`, `nombre`, `fechaAlta`, `idEmpleado`) VALUES (84, 'Dolor laboriosam aut aliquam sit. Perspiciatis eos molestiae aspernatur esse aliquam laudantium. Et ', '2013-04-04 13:05:36', 84);
INSERT INTO `reporte` (`idReporte`, `nombre`, `fechaAlta`, `idEmpleado`) VALUES (85, 'Ipsam dolores ipsam dolore et maxime qui eos quia. Sapiente doloribus cumque et dolorem et aut. Reic', '1986-11-23 12:59:58', 85);
INSERT INTO `reporte` (`idReporte`, `nombre`, `fechaAlta`, `idEmpleado`) VALUES (86, 'Harum provident voluptas aut quae sint expedita. Quia odio ratione velit. Accusamus vel non voluptat', '1975-10-07 02:30:31', 86);
INSERT INTO `reporte` (`idReporte`, `nombre`, `fechaAlta`, `idEmpleado`) VALUES (87, 'Aliquam rerum omnis tenetur aut voluptatem rerum est. Natus qui blanditiis fugiat maiores dolor. Ull', '1981-05-22 23:11:12', 87);
INSERT INTO `reporte` (`idReporte`, `nombre`, `fechaAlta`, `idEmpleado`) VALUES (88, 'Explicabo expedita quia impedit. Animi accusamus sequi aut officiis molestias illo. Repellat dolorem', '1979-05-29 17:42:41', 88);
INSERT INTO `reporte` (`idReporte`, `nombre`, `fechaAlta`, `idEmpleado`) VALUES (89, 'Laboriosam possimus harum ipsa est adipisci eligendi ea. Aut sunt temporibus deserunt. Deserunt quid', '1980-12-31 08:34:11', 89);
INSERT INTO `reporte` (`idReporte`, `nombre`, `fechaAlta`, `idEmpleado`) VALUES (90, 'Dolorum autem ratione debitis itaque. Odit quia eius velit mollitia quae enim est. Voluptas ut neque', '1991-07-06 02:31:43', 90);
INSERT INTO `reporte` (`idReporte`, `nombre`, `fechaAlta`, `idEmpleado`) VALUES (91, 'Voluptates aut corporis et itaque. Nulla sint qui ab praesentium soluta non. Sed hic at velit sed qu', '2021-07-10 00:20:23', 91);
INSERT INTO `reporte` (`idReporte`, `nombre`, `fechaAlta`, `idEmpleado`) VALUES (92, 'Repudiandae officia ipsam qui modi corrupti distinctio. Odit eius aut suscipit enim nihil. Sit conse', '1994-07-23 05:01:43', 92);
INSERT INTO `reporte` (`idReporte`, `nombre`, `fechaAlta`, `idEmpleado`) VALUES (93, 'Cumque iste ea doloremque quia tempora esse. Doloremque explicabo nobis sit quasi. Omnis dolorem ape', '2021-07-18 01:01:38', 93);
INSERT INTO `reporte` (`idReporte`, `nombre`, `fechaAlta`, `idEmpleado`) VALUES (94, 'Quibusdam optio laudantium modi omnis voluptas sit eius. Non quia mollitia vero assumenda. At quo ma', '1974-11-18 16:36:20', 94);
INSERT INTO `reporte` (`idReporte`, `nombre`, `fechaAlta`, `idEmpleado`) VALUES (95, 'Molestias eligendi omnis fugit veritatis. Repellat dolore veniam a libero expedita possimus soluta. ', '2019-01-14 13:41:46', 95);
INSERT INTO `reporte` (`idReporte`, `nombre`, `fechaAlta`, `idEmpleado`) VALUES (96, 'Minima consequuntur qui nisi voluptates. Quo non labore voluptate est est pariatur magni. Saepe dele', '2020-11-21 01:13:06', 96);
INSERT INTO `reporte` (`idReporte`, `nombre`, `fechaAlta`, `idEmpleado`) VALUES (97, 'Maxime fugit laudantium facilis iure impedit iure. Alias quam ad accusantium officia nobis ut quisqu', '2007-05-10 21:11:01', 97);
INSERT INTO `reporte` (`idReporte`, `nombre`, `fechaAlta`, `idEmpleado`) VALUES (98, 'Adipisci voluptas distinctio mollitia maiores nihil blanditiis. Est facilis in vero illum. Recusanda', '2001-09-14 23:43:32', 98);
INSERT INTO `reporte` (`idReporte`, `nombre`, `fechaAlta`, `idEmpleado`) VALUES (99, 'Sint sint error rerum sint maiores cumque. Optio maiores illo dicta similique ipsam. Enim voluptas a', '2011-09-03 01:30:20', 99);
INSERT INTO `reporte` (`idReporte`, `nombre`, `fechaAlta`, `idEmpleado`) VALUES (100, 'Sed veritatis cum doloremque atque sint repellat officiis sunt. Autem dicta dolorum libero modi veli', '1997-11-25 22:44:37', 100);

UPDATE reporte SET fechaAlta = (SELECT date_format(
    from_unixtime(
         rand() * 
            (unix_timestamp('2017-01-01 16:00:00') - unix_timestamp('2022-10-27 18:00:00')) + 
             unix_timestamp('2022-10-27 18:00:00')
                  ), '%Y-%m-%d %H:%i:%s') as datum_roden) WHERE fechaAlta < '2017-01-01';

```