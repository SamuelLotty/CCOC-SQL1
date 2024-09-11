# CCOC-SQL1
Assignment to practice SQL and creating databases and tables. Working on datatypes and sizes. 

Tables
CREATE TABLE Staff
(
StaffNumber varchar(8) PRIMARY KEY,
StaffName varchar(20),
TimeWorked date,
Sales money,
StaffEmail varchar(25),
PhoneNumber varchar(14),
DealershipNumber tinyint
)

CREATE TABLE Dealership
(
DealershipNumber tinyint PRIMARY KEY,
DealershipLocation varchar(20)NOT NULL,
NumberOfCars tinyint,
NumberOfStaff tinyint,
CarsSold smallint CHECK(CarsSold BETWEEN 0 AND 1000)
)

CREATE TABLE CarsLeased
(
CarReg varchar(14) NOT NULL PRIMARY KEY,
EngineType varchar (6),
NumberOfDoors tinyint CHECK (NumberOfDoors BETWEEN 0 AND 8),
Mileage int NOT NULL,
ServiceDate date,
LeaseOwner varchar (16) NOT NULL,
DealershipNumber tinyint
)

CREATE TABLE CarsSelling
(
CarReg varchar(14),
StaffNumber varchar (8),
PreviousOwners tinyint,
Price money NOT NULL,
DateOfSale date,
CONSTRAINT PRIMARY KEY (CarReg,StaffNumber)
)

Values

INSERT INTO Dealership
VALUES (1,'Airport,Road,Cork',102,4,430),
	(2,'Glen Road,Kerry',120,3,225),
	(3,'Harbour view,Tralee',76,2,57),
	(4,'Ard Cross, Waterford',187,5,102),
	(5,'Crosshaven, Cork',43,4,11),
	(6,'Hill view, Tipperary',98,6,203),
	(7, 'Castltroy,Limerick',246,3,79),
	(8,'Cashel, Tipperary',76,3,93),
	(9,'Youghal, Cork',145,5,194),
	(10,'Bantry, Cork',213,2,424),
	(11,'Kenmare,Kerry',104,5,541),
	(12,'Sneem, Kerry',83,7,24)

INSERT INTO Staff
VALUES ('12A','John Murphy',12/04/2008,104532,'Jmurph@gmail.com','085231456',1),
	   ('21A','Jerry O Connel',08/02/2022,50921,'Jerry@gmail.com','085234232',1),
	   ('42B','Alica Brown',10/03/2012,1902,'Brown@gmail.com','085231233',1),
	   ('46C','Mary Grand',11/11/2013,50291,'Grand@gmail.com','085211231',1),
	   ('2D','Sam Smith',09/20/2004,102,'SamSmith@gmail.com','085421231',2),
	   ('4A','Sam Brown',02/24/2001,7452,'SBrown@gmail.com','085232356',2),
	   ('32B','John Smith',04/25/2015,9023,'JSmith@gmail.com','085232212',2),
	   ('41C','Don Geary',02/28/2001,80282,'DGeary@gmail.com','083221452',3),
	   ('31B','Martha Lotty',01/30/2020,74282,'MLotty@gmail.com','083211122',3),
	   ('12C','John Matthew',02/28/2001,1282,'DGeary@gmail.com','083221452',4),
	   ('21C','Mat Andrews',07/22/2005,128232,'MAndrews@gmail.com','082441252',4),
	   ('54A','Mary Andrews',01/11/2008,12232,'MAndrews@gmail.com','086782121',4),
	   ('1A','Samuel Adams',04/21/2014,182,'SAdams@gmail.com','0816572711',4),
	   ('2C','John Rivers',05/23/2018,32282,'JRivers@gmail.com','085621332',4),
	   ('72B','Paul Rudd',07/09/2019,182,'PRudd@gmail.com','082312341',5),
	   ('75C','Maria Rivers',01/09/2020,12382,'MRivers@gmail.com','083213411',5),
	   ('92A','Adam McCarthy',07/02/2021,1382,'AMcCart@gmail.com','082322221',5),
	   ('72A','Jonny Stevenson',09/27/2021,90212,'JStevenson@gmail.com','084123111',5),
	   ('54D','Yolonda Gwythyr',23/04/2017,2223382,'Yolonda@gmail.com','08412311',6),
	   ('98A','Sigmund Esther',08/24/2022,89,'SEsther@gmail.com','089023212',6),
	   ('65B','Buffy Magdalena',09/09/2020,8982,'Buffy@gmail.com','08982321',6),
	   ('87E','Ruairí Vladan',12/08/2017,3382,'RVladan@gmail.com','089823112',6),
	   ('83G','Adolfo Marcianus',04/09/2014,3282,'AMarc@gmail.com','086123123',6),
	   ('72F','Kerime Nanaia',01/09/2022,41382,'KNanaia@gmail.com','0865463433',6),
	   ('12F','Andrej Tuukka',07/23/2015,42,'ATuukka@gmail.com','0858658747',7),
	   ('34E','Filibert Jove',09/11/2012,42182,'FJove@gmail.com','0842521433',7),
	   ('23E','Leeba Chadwick',02/15/2011,44322,'LChadwick@gmail.com','085225433',7),
	   ('28B','Karen Mcconnell',01/18/2001,4222,'KMcconnell@gmail.com','085231231',8),
	   ('98A','Nikolas Gillespie',06/16/2001,14322,'NGillespie@gmail.com','085992321',8),
	   ('75H','Henry Coleman',09/18/2011,41222,'HColeman@gmail.com','085757511',8),
	   ('12H','Cecily Kent',02/22/2005,222,'CKent@gmail.com','0897574847',9),
	   ('1H','Maximus Strong',09/18/2006,41,'MStrong@gmail.com','089788757',9),
	   ('45E','Alex Spence',03/09/2021,10231,'ASpence@gmail.com','085987987',9),
	   ('41F','Alysha Moon',05/19/2022,99232,'AMoon@gmail.com','08657887',9),
	   ('4E','Wyatt Webster',11/12/2009,100231,'WWebster@gmail.com','087458473',9),
		('14E','Mary McGibb',01/15/2019,101,'MGibb@gmail.com','087555213',10),
		('54F','John Wyyatt',03/16/2022,1231,'JWyyatt@gmail.com','0851535333',10),
		('57A','Bentley Ruiz',09/19/2012,56231,'BRuiz@gmail.com','082565477',11),
		('60B','Stan Henry',08/11/2000,192021,'SHenry@gmail.com','088575543',11),
		('60A','Rosa Buckley',02/10/2005,14000,'RBuckley@gmail.com','0854631221',11),
		('79G','Eric Hunt',12/19/2021,50,'EHunt@gmail.com','0849876654',11),
		('81A','Arther Graves',10/25/2017,10982,'AGraves@gmail.com','0852891446',11),
		('99A','Sterling Joe',03/01/2014,102,'SJoe@gmail.com','0854442136',12),
		('98B','Fabian Lynch',06/06/2012,12,'FLynch@gmail.com','0857751446',12),
		('95F','Tyler Hanson',07/11/2009,90021,'THanson@gmail.com','0851231446',12),
		('3E','Harley Foster',08/02/2007,75602,'HFoster@gmail.com','0852895646',12),
		('90A','Lucas Massy',09/20/2019,65201,'LMassy@gmail.com','0852891786',12),
		('45F','Jim Beam',10/26/2010,23552,'JBeam@gmail.com','0864891446',12),
		('77D','Joe Foster',12/22/2011,982,'JFoster@gmail.com','0859091446',12)

INSERT INTO CarsSelling
VALUES ('191-C-9012','12A','2','€40000','12/05/2022'),
	   ('181-C-48292','1H','4','€22549','09/22/2021'),
	   ('131-C-762314','21A','5','€5450','07/21/2019'),
       ('12-C-12','60A','8','€2500','05/29/2015'),
	   ('211-C-4212','57A','2','€50000','07/25/2021'),
	   ('212-C-48','65B','1','€80000','02/02/2023'),
	   ('191-D-8923','87E','3','€37500','01/09/2023'),
	   ('202-KE-97231','83G','4','€27250','10/15/2020'),
	   ('201-KE-89723','92A','2','€46750','09/22/2020'),
	   ('192-D-4','90A','3','€65250','10/13/2021'),
	   ('182-D-1123','75H','1','€42525','07/07/2021'),
	   ('151-D-52313','4A','5','€56750','09/22/2018'),
	   ('172-DL-44423','4E','6','€32525','07/18/2022'),
	   ('181-KE-1972','54D','2','€13520','01/25/2023'),
	   ('192-C-1823','54A','4','€50250','05/13/2019')

INSERT INTO CarsLeased
VALUES
('212-C-205','Petrol','4','25675','03/10/2023','John McCabe',1),
('202-D-7884','Diesel','3','50298','05/15/2023','Mary Addams',5),
('211-C-6095','Diesel','4','90675','07/28/2024','Mary Joesph',12),
('192-D-1982','Petrol','2','28752','05/17/2023','Jeremy Medina',8),
('181-C-55295','Petrol','2','18624','02/02/2024','Valerie Wise',4),
('162-KE-87795','Diesel','4','104926','02/18/2024','Harriet Bradley',1),
('222-C-994','Petrol','2','4265','01/04/2025','Rhea Mills',12),
('202-D-5539','Diesel','4','67876','01/28/2025','Oriel Kirk',5),
('192-KE-9963','Petrol','4','34215','03/03/2023','Gene Robson',4),
('172-D-8842','Diesel','2','88664','01/21/2023','Emily Cummings',1),
('152-G-62632','Petrol','4','110873','04/28/2023','Lonnie Garret',3),
('201-L-1123','Diesel','3','87442','12/28/2022','Jeff Whitehead',12),
('202-L-44267','Diesel','2','55317','05/24/2023','Misty Olson',1),
('222-C-95','Petrol','2','18542','02/04/2024','Elbert Long',2),
('151-DL-266472','Diesel','4','11265','11/24/2022','Osbert Currey',3)

Queries 
1.	List what car registrations are for sale in each dealership in Munster.

SELECT CarReg,DealershipLocation
FROM CarsSelling,Staff,Dealership
WHERE Staff.StaffNumber=CarsSelling.StaffNumber AND Dealership.DealershipNumber=Staff.DealershipNumber

2.	List names of staff members and dealerships in Munster.
SELECT StaffName,DealershipLocation
FROM Staff,Dealership
WHERE Staff.DealershipNumber=Dealership.DealershipNumber
ORDER BY DealershipLocation

3.	List leased car owners and staff numbers in Munster cars.
SELECT LeaseOwner,StaffNumber
FROM CarsLeased,Dealership,Staff
WHERE CarsLeased.DealershipNumber=Dealership.DealershipNumber AND Dealership.DealershipNumber=Staff.DealershipNumber

4.	Identify the total number of cars per dealerships saved as a view.

/****** Script for SelectTopNRows command from SSMS  ******/
SELECT TOP (1000) [DealershipLocation]
 ,[NumberOfCars]
FROM [SLottyMunsterCarSales].[dbo].[Total Number of cars in Dealerships]

5.	Identify how much sales a dealership made with how much staff saved as a view.

/****** Script for SelectTopNRows command from SSMS  ******/
SELECT TOP (1000) [DealershipLocation]
      ,[NumberOfStaff]
      ,[CarsSold]
 FROM [SLottyMunsterCarSales].[dbo].[Sales per dealership with staff amount]
 
6.	List all of the leased cars and when the cars service date is due saved as a view.
/****** Script for SelectTopNRows command from SSMS  ******/
SELECT TOP (1000) [CarReg]
       ,[ServiceDate]
FROM [SLottyMunsterCarSales].[dbo].[Leased cars and service date]

7.	Show staff numbers of sales and dealership numbers in one enquiry saved as a view.
/****** Script for SelectTopNRows command from SSMS  ******/
SELECT TOP (1000) [StaffNumber]
      ,[Sales]
      ,[DealershipNumber]
FROM [SLottyMunsterCarSales].[dbo].[Staff sales]


8.	 List car registration, price and previous owners for cars selling as a stored procedure.
CREATE PROCEDURE ListCarInfo @CarReg varchar(20)
AS
SELECT Price,PreviousOwners
FROM CarsSelling
WHERE CarReg = @CarReg

9.	Show staff names from dealership numbers saved as a function.

CREATE FUNCTION DealershipInfo(@DealershipNumber int)
RETURNS table 
AS 
RETURN
	(SELECT StaffName from Staff WHERE DealershipNumber=@DealershipNumber)
  

10.	List staff number and phone numbers of those staff members as a database trigger.
CREATE TRIGGER StaffTrigger
ON Staff
AFTER INSERT 
AS 
BEGIN 
		INSERT INTO Contact(StaffNumber,PhoneNumber,StaffEmail,date)
	SELECT inserted.StaffNumber AS StaffNumber,inserted.PhoneNumber AS PhoneNumber,
		inserted.StaffEmail AS StaffEmail, GETDATE() as date
		FROM INSERTED 
   	 END
