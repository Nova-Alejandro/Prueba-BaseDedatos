# Prueba-BaseDedatos

To install SQL Server, download the free installer from the official Microsoft SQL Server website (choosing either the Developer or Express edition). Run it as an administrator, select the basic installation, accept the terms, and wait for the process to complete. Once finished, click "Install SSMS" to download and install SQL Server Management Studio, which will allow you to manage your databases visually.


Below, I present a visual diagram showing the relationships that must be established within the QLS.
<img width="1283" height="792" alt="image" src="https://github.com/user-attachments/assets/7bd008a2-5a1b-4861-8015-e821af0a6c93" />

Using the following code, we create the tables we will need:

CREATE TABLE Suppliers (
id SERIAL PRIMARY KEY,
Name_Supplier VARCHAR(100) UNIQUE NOT NULL,
supplier_city VARCHAR(100)
);




INSERT INTO Suppliers (Name_Supplier,Supplier_city)
VALUES
('Aceros del Norte S.A.S','Cartagena'),
('Industriales SAS', 'Barranquilla'),
('Suministros Global SAS', 'Santa Marta');






We insert data into the previously created tables using the following code:

INSERT INTO Suppliers (Name_Supplier,Supplier_city)
VALUES
('Aceros del Norte S.A.S','Cartagena'),
('Industriales SAS', 'Barranquilla'),
('Suministros Global SAS', 'Santa Marta');

The following code performs queries requested by the boss, the client, or an administrator who wants to know what is in the records:





SELECT * FROM movement m
INNER JOIN suppliers s
ON s.id = m.id_proveedor
-- FIRST QUERY
CREATE VIEW Query1
SELECT COUNT(*)
FROM Products p
INNER JOIN movement m
ON p.id = m.id_Producto
GROUP BY (p.id, p.Nombre_Producto)







With the following code, we can view the previously created views:

Select view consulta4
