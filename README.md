# SQL Notes

Data in SQL
Definition:
Data is raw information stored in a database.
By itself, it has no meaning until we use SQL queries to organize, retrieve, or manipulate it into meaningful information.

Example Table: Students
ID	 Name	 Age
1  	 Devi	 25
2	   Anwi	 22

Each value (1, Devi, 25) is data.

Query example:
SELECT Name FROM Students WHERE Age > 23;
Output: Devi → now the raw data has meaning.

Key Points
Data = Raw values stored in a database.
SQL is used to store, retrieve, and manipulate data efficiently.

Types of Data in SQL:
Type	           Example
INT            	25, 100
FLOAT	          25.5, 99.99
VARCHAR	        "Devi", "Hello"
CHAR	          "A", "M"
DATE	          "2025-09-24"
DATETIME	      "2025-09-24 17:00:00"
BOOLEAN	         TRUE, FALSE

1. What is a Database?
A database is an organized collection of data stored electronically.
It allows data to be stored, managed, and retrieved efficiently.
Analogy: A database is like a digital filing cabinet for information.
Examples:
School: Stores student details.
Bank: Stores account details and transactions.

2. What is Data?
Data = raw facts or values stored in a database.
By itself, data has no meaning.
SQL helps process and organize data to turn it into meaningful information.

Examples:
Numbers: 25, 100, 42
Text: "Devi", "Anwi"
Dates: "2025-09-24"

Analogy: Data = ingredients, Information = prepared dish.

3. What is SQL?
SQL (Structured Query Language) is a language used to create, manage, and query databases.
Converts raw data into meaningful information.

Example Table: Students
ID	Name	Age
1	Devi	25
2	Anwi	22

SQL Query Example:
SELECT Name FROM Students WHERE Age > 23;
Output: Devi → raw data becomes meaningful information.

4. SQL Data Types
Type         	Meaning	Example
INT	          Integer numbers	25, 100
FLOAT	        Decimal numbers	25.5, 99.99
VARCHAR	      Text (variable)	"Devi", "Hello"
CHAR	        Text (fixed)	"A", "M"
DATE	        Date values	"2025-09-24"
DATETIME	    Date + Time	"2025-09-24 17:00:00"
BOOLEAN     	True / False	TRUE, FALSE

6. Types of Databases and Usage
A. Relational Databases (RDBMS)
Structure: Tables with rows & columns
Language: SQL
Examples: MySQL, SQL Server, PostgreSQL, Oracle
Use Cases: Structured data, banking, ERP, e-commerce
Example Table: Products

ID	    Product  	Price
1	      Pen	      10
2	      Book	   50

Operations:
Create tables & schema
Insert data (INSERT)
Query data (SELECT, JOIN, WHERE)
Update / Delete (UPDATE, DELETE)
Transactions (commit/rollback)

B. Non-Relational Databases (NoSQL)
Structure: Document, key-value, graph, column-family
Schema: Flexible
Examples: MongoDB, Redis, Couchbase, Cassandra, Neo4j
Use Cases: Unstructured data, social media, IoT, real-time apps
Example (MongoDB Document):

{
  "Name": "Devi",
  "Age": 25,
  "Hobbies": ["Reading", "Coding"]
}


Query Example:
db.Students.find({ Age: { $gt: 23 } });
Output: { "Name": "Devi", "Age": 25, "Hobbies": ["Reading", "Coding"] }

Database          Type Summary
Type	            Structure	                                 Examples	                                   Best Use Cases
RDBMS	           Tables (rows/columns)	                  MySQL, PostgreSQL, SQL Server, Oracle        	Structured data, banking, ERP, web apps
NoSQL	           Document / Key-Value / Graph / Column	  MongoDB, Redis, Couchbase, Cassandra	        Flexible/unstructured data, real-time apps, big data

6. How Data is Stored in a Database
Step 1: Create a Database
CREATE DATABASE SchoolDB;

Step 2: Create a Table
USE SchoolDB;
CREATE TABLE Students (
    ID INT PRIMARY KEY,
    Name VARCHAR(50),
    Age INT
);

Step 3: Insert Data
INSERT INTO Students (ID, Name, Age)
VALUES (1, 'Devi', 25),
       (2, 'Anwi', 22);

Step 4: Retrieve Data
SELECT * FROM Students;
SELECT Name FROM Students WHERE Age > 23;
Output: Devi → data becomes meaningful information

Step 5: Update Data
UPDATE Students
SET Age = 26
WHERE ID = 1;

Step 6: Delete Data
DELETE FROM Students WHERE ID = 2;

7. Flow of Data in a Database
Design Schema: Create database & tables
Insert Data: Add raw facts (rows)
Store Data: Database keeps it safe
Query with SQL: Convert data into meaningful info
Update/Delete Data: Modify or remove data

Analogy:
Database = cupboard
Table = shelf inside cupboard
Data = items/books on the shelf
SQL = hands/keys to arrange, take, or place items

8. Summary (Simple Words)
Database: Organizes and stores data safely
Data: Raw facts in the database
SQL: Language to manage and query data
RDBMS: Structured tables, relationships, SQL-based
NoSQL: Flexible, unstructured, fast
Goal: Turn raw data → meaningful information
