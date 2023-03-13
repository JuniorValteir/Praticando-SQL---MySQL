# Praticando-SQL---MySQL

## SOME SIMPLE COMANDS TO PRACTICE SQL USIND MYSQL

###### MODIFY COLLUMN SEQUENCE IN SOME TABLE 
```


ALTER TABLE changeColumnPositionDemo MODIFY StudentAddress varchar(200) AFTER StudentAge

INSERT A NEW COLLUMN IN SOME TABLE 
ALTER TABLE Clients 
INSERT [COLUMN] columsName dataType AFTER | BEFORE some_existing_column
```
###### CREATE SOME TABLE 
```


CREATE TABLE Clients
(
	Id INT PRYMARY KEY AUTO_INCREMENT, // Will be created automatically 
	Name VARCHAR(60),
	EMAIL VARCHAR(30),
	DATEOFBIRTH DATE,
)
```
###### INSERT COMAND
```

INSERT INTO CLIENTES(NAME, EMAIL, DATEOFBIRTH)
VALUES              ('CARLOS', 'CARLOS@GMAIL.COM, 10.02.2000')


```
###### UPDATE VALUES ON TABLE
```	     


UPDATE Clients 
SET 	Id  = '[value-1]',
	Name= '[value-2]',
	EMAIL =' [value-3]',
	DATEOFBIRTH='[value-4]',
WHERE ID= 0000990911000 // Don't forget to especified and filter by Id, or all data will be updated

```
###### RENAME COLUMNS
```

ALTER TABLE table_name   
CHANGE COLUMN old_column_name new_column_name Data Type

```
###### COMPOSITE PRIMARY KEY 
```



CREATE TABLE SALES_ITENS
(
        PRODUCTS_ID INT NOT NULL,
        SALES_ID INT NOT NULL, 
	PRODUTS_PRICE FLOAT NOT NULL, 
	DISCOUNT FLOAT NOT NULL,
	FOREIGN KEY(PRODUCTS_ID) REFERENCES PRODUCTS(ID),
	FOREIGN KEY(SALES_ID) REFERENCES SALES(ID),
	
	PRIMARY KEY (PRODUCTS_ID,SALES_ID)
)

```
###### SELECT PARIENTS DATA USING "INNER JOIN" COMAND 
```



SELECT P.ID, P.DESCRIPTION, P.PRICE, P.QUANTITY, C.NOME, C.DESCRIPTION
FROM PRODUCTS P INNER JOIN CATEGORY C
ON C.ID = P.ID_CATEGORY 

```
###### MATEMATIC OPERATION TO SHOW TOTAL DATA
```



SELECT p.ID 'Code', p.DESCRIPTION_Products 'Description', (P.PRICE_Producs * P.QUANTITY_Products) 'Total', C.NAME_Category 'Name', C.DESCRIPTION_Category 'Description' 
FROM products P INNER JOIN category C 
ON P.ID_Category = C.id;

```
```

