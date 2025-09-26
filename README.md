# SQL Notes
_
**Data in SQL**
**Definition:**_
Data is raw information stored in a database.
By itself, it has no meaning until we use SQL queries to organize, retrieve, or manipulate it into meaningful information.

**Example Table: Students**__
ID	 Name	 Age
1  	 Devi	 25
2	   Anwi	 22

Each value (1, Devi, 25) is data.

**Query example:**__
SELECT Name FROM Students WHERE Age > 23;
Output: Devi → now the raw data has meaning.

**Key Points**
Data = Raw values stored in a database.
SQL is used to store, retrieve, and manipulate data efficiently.

**Types of Data in SQL:**
Type	           Example
INT            	25, 100
FLOAT	          25.5, 99.99
VARCHAR	        "Devi", "Hello"
CHAR	          "A", "M"
DATE	          "2025-09-24"
DATETIME	      "2025-09-24 17:00:00"
BOOLEAN	         TRUE, FALSE
                                                                                       ** Understanding Database, DBMS, and SQL**
1. Database
Definition: A database is a structured place to store data.
Types of data stored:
Structured Data: Organized into tables, rows, columns (easy to query).
Raw / Unstructured Data: Data without predefined structure (files, images, videos, logs, JSON, text, etc.).
Example – Structured Data (Table):

ID	Name	Age
1	Devi	25
2	Anwi	22

Example – Raw / Unstructured Data:
A text file: "This is a sample note"
An image: profile_pic.jpg
A JSON file: {"user": "Devi", "age": 25}
Key Point: Databases can store both structured and raw/unstructured data; DBMS helps manage them.

2. DBMS (Database Management System)
Definition: Software that manages the database.
Responsibilities:
Store, retrieve, update, delete structured and unstructured data
Backup and restore data
Ensure security
Handle multiple users and transactions
Examples: MySQL, PostgreSQL, MongoDB (especially for unstructured data), Oracle
Analogy: DBMS is like a manager who organizes and controls data access.

3. SQL (Structured Query Language)
Definition: SQL is a language to communicate with DBMS.
Important: SQL is not software, it’s a set of instructions.
Example Query (Structured Data):
SELECT Name FROM Students WHERE Age > 23;
Note: For unstructured/raw data, DBMS may provide other query mechanisms (e.g., MongoDB uses JSON-based queries).

Analogy: SQL is the language you speak to DBMS to tell it what to do with structured or semi-structured data.

4. How They Work Together
Database → Stores structured tables and raw/unstructured data.
DBMS → Software that manages, organizes, and secures data.
SQL / Query Language → Communicates with DBMS to perform operations.
Flow:
User/Application → SQL / Query → DBMS → Database (Structured + Raw Data) → Result

✅ One-Line Summary
Database stores structured and unstructured data.
DBMS manages data and ensures integrity, security, and accessibility.
SQL (or queries) is the language to communicate with DBMS.

**1. What is a Database?**
A database is an organized collection of data stored electronically.
It allows data to be stored, managed, and retrieved efficiently.
**Analogy:** A database is like a digital filing cabinet for information.
**Examples:**
School: Stores student details.
Bank: Stores account details and transactions.

**2. What is Data?**
Data = raw facts or values stored in a database.
By itself, data has no meaning.
SQL helps process and organize data to turn it into meaningful information.

**Examples:**
Numbers: 25, 100, 42
Text: "Devi", "Anwi"
Dates: "2025-09-24"

Analogy: Data = ingredients, Information = prepared dish.

**3. What is SQL?**
SQL (Structured Query Language) is a language used to create, manage, and query databases.
Converts raw data into meaningful information.

**Example Table:** Students
ID	Name	Age
1	Devi	25
2	Anwi	22

**SQL Query Example:**
SELECT Name FROM Students WHERE Age > 23;
Output: Devi → raw data becomes meaningful information.

**4. SQL Data Types**
Type         	Meaning	Example
INT	          Integer numbers	25, 100
FLOAT	        Decimal numbers	25.5, 99.99
VARCHAR	      Text (variable)	"Devi", "Hello"
CHAR	        Text (fixed)	"A", "M"
DATE	        Date values	"2025-09-24"
DATETIME	    Date + Time	"2025-09-24 17:00:00"
BOOLEAN     	True / False	TRUE, FALSE

**5. Types of Databases and Usage**
**A. Relational Databases (RDBMS)**
Structure: Tables with rows & columns
Language: SQL
Examples: MySQL, SQL Server, PostgreSQL, Oracle
Use Cases: Structured data, banking, ERP, e-commerce
Example Table: Products

ID	    Product  	Price
1	      Pen	      10
2	      Book	   50

**Operations:**
Create tables & schema
Insert data (INSERT)
Query data (SELECT, JOIN, WHERE)
Update / Delete (UPDATE, DELETE)
Transactions (commit/rollback)

**B. Non-Relational Databases (NoSQL)**
Structure: Document, key-value, graph, column-family
Schema: Flexible
Examples: MongoDB, Redis, Couchbase, Cassandra, Neo4j
Use Cases: Unstructured data, social media, IoT, real-time apps
**Example (MongoDB Document):**

{
  "Name": "Devi",
  "Age": 25,
  "Hobbies": ["Reading", "Coding"]
}


**Query Example:**
db.Students.find({ Age: { $gt: 23 } });
Output: { "Name": "Devi", "Age": 25, "Hobbies": ["Reading", "Coding"] }

Database          Type Summary
Type	            Structure	                                 Examples	                                   Best Use Cases
RDBMS	           Tables (rows/columns)	                  MySQL, PostgreSQL, SQL Server, Oracle        	Structured data, banking, ERP, web apps
NoSQL	           Document / Key-Value / Graph / Column	  MongoDB, Redis, Couchbase, Cassandra	        Flexible/unstructured data, real-time apps, big data

Relational Databases = MySQL, PostgreSQL, Oracle (PL/SQL), SQL Server, MariaDB…
NoSQL Databases = MongoDB, Redis, Cassandra, Neo4j, Couchbase,dynamodb(aws) etc.

**6. How Data is Stored in a Database**
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

**7. Flow of Data in a Database**
Design Schema: Create database & tables
Insert Data: Add raw facts (rows)
Store Data: Database keeps it safe
Query with SQL: Convert data into meaningful info
Update/Delete Data: Modify or remove data

**Analogy:**
Database = cupboard
Table = shelf inside cupboard
Data = items/books on the shelf
SQL = hands/keys to arrange, take, or place items

**8. Summary (Simple Words)**
Database: Organizes and stores data safely
Data: Raw facts in the database
SQL: Language to manage and query data
RDBMS: Structured tables, relationships, SQL-based
NoSQL: Flexible, unstructured, fast
Goal: Turn raw data → meaningful information
 
                                                                                                                **DBMS**

**What is DBMS?**
DBMS (Database Management System) is software that stores, organizes, manages, and retrieves data efficiently from databases.
It acts as an interface between users/applications and the database.
Examples of DBMS:
Relational: MySQL, PostgreSQL, Oracle, SQL Server
NoSQL: MongoDB, Couchbase, Cassandra

**Key Functions:**
Data storage & retrieval – store large amounts of data and fetch it quickly.
Data security – control who can access or modify data.
Dataintegrity – ensure data is accurate and consistent.
Concurrency control – multiple users can access data simultaneously without conflicts.
Backup & recovery – recover data in case of crashes or errors.

**Use Cases of DBMS:**
Use Case                                              	Description / Example
Banking	                                      Store customer accounts, transactions, loans, and ensure secure access.
E-commerce                                    Manage product catalogs, orders, inventory, and customer data.
Healthcare	                                  Maintain patient records, prescriptions, lab reports, and appointment schedules.
Education	                                    Store student data, grades, courses, schedules, and faculty information.
Telecom                                     	Manage subscriber info, call records, billing, and network usage.
Social Media	                                Store user profiles, posts, messages, and activity logs
Data Analytics / BI	                          Power BI, Tableau, and dashboards fetch data from DBMS for analysis.
Enterprise Resource Planning (ERP)          	Store and manage HR, finance, sales, and supply chain data centrally.

                                                  **   How we process data from the database**
                   
───────────── Human / User ───────────────    ─────── Application ────────    ───── Power BI ──────
1. User types SQL query                   1. Web App sends query/login       1. Power BI fetches data
   in MySQL Workbench                        request to database                 (e.g., sales report)
   [Customer ordering food]                 [User request via app]             [BI tool request]

2. MySQL Workbench (Connector)            2. JDBC/ODBC or API Connector      2. Power BI Connector
   Sends query to DB                         Sends query to DB                  Sends query to DB
   [Waiter carries order]                    [Connector/driver carries]         [Connector carries]

3. MySQL Database Engine                   3. Database Engine                 3. Database Engine
   Parses, validates, executes,            Parses, validates, executes       Parses, validates, executes
   fetches data                             fetches data                      fetches data
   [Kitchen prepares food]                  [Kitchen prepares food]           [Kitchen prepares food]

4. MySQL Workbench (Result back)          4. Connector/API returns data      4. Connector returns results
   Receives query result                     back to Web App                   back to Power BI
   [Waiter brings food back]                [Waiter brings food back]         [Waiter brings food back]

5. User sees output                        5. Web App displays result         5. Power BI visualizes data
   [Customer eats dish]                      on screen                        [Customer sees visual report]

                                                                                                              **  DBMS and its types**
**   TYPES OF DBMS**
   🔹 1. Relational Database (RDBMS – SQL)
Definition: Stores data in tables (rows + columns) with a fixed schema.
Example:
CREATE TABLE Students (ID INT, Name VARCHAR(50), Age INT);
INSERT INTO Students VALUES (1,'Anwi',22),(2,'Devi',24);
SELECT * FROM Students;
Output:
ID	Name	Age
1	Anwi	22
2	Devi	24

Advantages:
✔ Structured & reliable
✔ ACID transactions
✔ Easy querying with SQL
Use Cases: Banking, ERP, CRM, e-commerce.

🔹 2. Document Database (NoSQL – MongoDB)
Definition: Stores data as JSON-like documents.
Example:
{ "ID":1, "Name":"Anwi", "Age":22 }
{ "ID":2, "Name":"Devi", "Age":24, "Hobbies":["Reading","Coding"] }

Output (find query):
[
 { "ID":1,"Name":"Anwi","Age":22 },
 { "ID":2,"Name":"Devi","Age":24,"Hobbies":["Reading","Coding"] }
]

Advantages:
✔ Flexible schema
✔ Stores unstructured data
✔ Scales easily
Use Cases: CMS, catalogs, web apps, mobile apps.

🔹 3. Key-Value Database (Redis, DynamoDB)
Definition: Stores data as key → value pairs.
Example (Redis):
SET user:1 "Anwi"
SET user:2 "Devi"
GET user:1

Output:
"Anwi"

Advantages:
✔ Super fast (in-memory)
✔ Simple lookup
✔ Best for caching
Use Cases: Session storage, caching, gaming apps.

🔹 4. Graph Database (Neo4j)
Definition: Stores data as nodes & relationships.
Example (Cypher query):
CREATE (a:Person {name:'Anwi'})-[:FRIENDS_WITH]->(b:Person {name:'Devi'});
MATCH (p:Person)-[:FRIENDS_WITH]->(f) RETURN p,f;
Output:
Anwi ---FRIENDS_WITH---> Devi

Advantages:
✔ Best for relationship-heavy data
✔ Fast graph traversal
✔ Natural for networks
Use Cases: Social networks, fraud detection, recommendation engines.

🔹 5. Wide-Column Database (Cassandra, HBase)
Definition: Stores data in column families instead of rows.
Example:
CREATE TABLE students (id INT PRIMARY KEY, name TEXT, age INT);
INSERT INTO students (id, name, age) VALUES (1,'Anwi',22);
INSERT INTO students (id, name, age) VALUES (2,'Devi',24);
SELECT * FROM students;
Output:
id	name	age
1	Anwi	22
2	Devi	24

Advantages:
✔ Handles huge data volumes
✔ Scales horizontally
✔ Flexible schema
Use Cases: IoT, analytics, big data applications.

🔹 6. In-Memory Database (Redis, Memcached)
Definition: Stores data in RAM for speed.
Example:
SET session:123 "Active"
GET session:123
Output:
"Active"

Advantages:
✔ Lightning-fast performance
✔ Low latency
✔ Good for real-time apps
Use Cases: Gaming, caching, stock trading apps.

🔹 7. Time-Series Database (InfluxDB, TimescaleDB)
Definition: Optimized for time-stamped data.
Example:
INSERT temperature,location=room1 value=28 1633012800
INSERT temperature,location=room1 value=29 1633016400
SELECT * FROM temperature;
Output:
time	location	value
1633012800	room1	28
1633016400	room1	29

Advantages:
✔ Optimized for time-based queries
✔ Fast ingestion
✔ Perfect for monitoring
Use Cases: IoT sensors, server monitoring, stock prices.

🔹 8. Object-Oriented Database (ObjectDB)
Definition: Stores data as objects (like in OOP).
Example (Java Object):
class Student {
 int id;
 String name;
 int age;
}

Stored as:
Object: Student {id:1, name:"Anwi", age:22}

Advantages:
✔ Works directly with OOP
✔ Handles complex data
✔ No need for conversion
Use Cases: Multimedia, CAD apps, simulations.

🔹 9. Hierarchical Database (IBM IMS)
Definition: Stores data in a tree structure (parent-child).
Example:

University
 └── Faculty
      └── Student (Anwi)
      └── Student (Devi)


Advantages:
✔ Fast retrieval
✔ Natural tree format
✔ Good for hierarchical data
Use Cases: Legacy banking, telecom systems.

🔹 10. Network Database
Definition: Stores data with multiple parent-child links.
Example:
Student (Anwi) → Course (SQL)
Student (Devi) → Course (SQL, MongoDB)
Advantages:
✔ Handles complex relationships
✔ More flexible than hierarchical DB
Use Cases: Legacy enterprise apps.

🔹 11. Cloud Database
Definition: Hosted on cloud (AWS, Azure, GCP).
Example (AWS RDS MySQL):
mysql -h mydb.rds.amazonaws.com -u admin -p
SELECT * FROM Students;

Advantages:
✔ Managed service
✔ Scalable
✔ Pay as you go
Use Cases: Startups, SaaS, global apps.

🔹 12. Multimodel Database (ArangoDB, OrientDB)
Definition: Supports multiple data models (document + graph + key-value).
Example:
Documents:
{ "id":1, "name":"Anwi" }
{ "id":2, "name":"Devi" }

Graph relation:
Anwi → FRIENDS_WITH → Devi

Advantages:
✔ Flexible
✔ Multiple models in one DB
✔ Saves integration cost
Use Cases: Apps needing mixed data (social + documents).


                                                                                                                         **  SCHEMA**
🔹 What is a Schema?
A schema is the blueprint or structure of how data is organized inside a database.
👉 Think of it like a map or design plan that tells:
What tables/collections exist
What fields/columns each table has
What type of data each column can store
Rules like Primary Key, Foreign Key, Unique, Not Null
How tables are related to each other
📌 In simple words:
Schema = design of database
Data = actual content stored in that design
🔹 Schema in SQL (Relational Database)
In SQL databases (MySQL, PostgreSQL, Oracle, SQL Server):
Schema is strict → You must define tables and columns before inserting data.
Changes in schema (adding/removing columns) require altering the table.

Example:
CREATE TABLE Students (
    StudentID INT PRIMARY KEY,
    Name VARCHAR(50) NOT NULL,
    Age INT,
    Email VARCHAR(100) UNIQUE
);

✅ Here the Schema defines:
StudentID → Integer, Primary Key
Name → String, cannot be empty
Age → Integer
Email → String, must be unique
Now when you insert data:

INSERT INTO Students (StudentID, Name, Age, Email)
VALUES (1, 'Devi', 22, 'devi@example.com');


➡️ This record follows schema rules.
🔹 Schema in NoSQL (Flexible Schema)
In NoSQL databases (MongoDB, DynamoDB, Cassandra):
Schema is flexible / schema-less.
You don’t have to predefine structure.
Documents/records in the same collection can have different fields.
Example in MongoDB:
{
  "StudentID": 1,
  "Name": "Devi",
  "Age": 22,
  "Email": "devi@example.com"
}

Another document in the same collection:

{
  "StudentID": 2,
  "Name": "Anwi",
  "Skills": ["AWS", "DevOps"]
}

✅ Different structure, but still valid.
🔹 Diagram (Analogy)
🏠 Schema = Blueprint of a House
👨‍👩‍👧 Data = People living inside
You first design rooms, windows, doors (schema)
Then you fill it with furniture, people, items (data)

🔹 Advantages of Schema
SQL (Strict Schema):
Ensures data consistency
Enforces rules (e.g., age must be number)
Prevents invalid data entry

NoSQL (Flexible Schema):
Easy to adapt to changes
No migrations needed
Good for unstructured or fast-changing data

✅ Final Definition:
A schema is the blueprint/structure of a database that defines how data is stored, organized, and related.
   

