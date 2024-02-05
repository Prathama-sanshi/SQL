# MySQL

## 1.Database Design and Introduction to MySql
<p>Handling a complex and extensive database has to be planned accordingly , especially when the type of data managed in the organisation is expected to grow massively .This is why there is need for database managment system (DBMS) </p>

## 2.Data Warehouse
Data warehouse is a central repository of the entire enterprise's data. Data is stored such that its retrieval and managment is easy.
The main characteristic of data warehouse is are as follows :
<ol>
  <li>Subject Oriented :- Built for a specific purpose. </li>
  <li>Integrated :- gathered form multiple sorurces into one form.</li>
  <li>Non-Volatile :- Data does not change over time.</li>
  <li>Time-varient :- Capable of capturing information over time.</li>
</ol>

## 3.Journey of data in an organization
<ul>
<li>Data is captured from multiple sources and stored in excel files or databases , such as oracal/MySql (RDBMS).</li>
<li>The Extract , Transform and Load process is applied on the captured data.(Three steps for data integration process)</li>
<ol>
  <li>Extract :- Extracting the information from data sources eg: Excel, spreadsheets, SaaS platforms , Web scraping , cloud etc.</li>
  <li>Transform :- Application of functions to change format or structure and extracted data in order to prepare it for loading into the end target</li>
  <li>Load :- Loading the data into target system, such as data warehouse , data mart etc </li>
</ol>
<li>The stored data is either connected to online analytical processing (OAP) for futher processing or creating reports</li>
</ul>

## 4.Dimension Model
 The dimension model is a database structure technique which is used for faster data access.
<ol>
  <li>Facts :- Facts are numberical data that capture the factual information in data warehouse.</li>
  <li>Dimensions :- Dimensions are the metadata (context and background informations) used for analysing facts.</li>
</ol>

## 5.Entity Relationship Diagram(ERD)
<ul>
<li>ERD is representation of the table in database , it gives a quick overall idea of how differnt entities or tables are connected within the database.</li>
  <li>Here the fields marked with star (*) represent the primary key for that table.</li>
  <li>The line connecting the two tables indicate that a relationship exist between them.</li>
  <li>Types of relationships :-</li>
  <ol>
    <li>One to one:- An instance of an entity is related to only a single instance of another entity</li>
    <li>One to many:- When a single instance of an entity is related to more than one instance of another entity</li>
    <li>Many to one:- When more than one instance of an entity is related to only one instance of another entity</li>
    <li>Many to many:- When more than one instance of an entity is related to more than one instance of another entity</li>
  </ol>
</ul>
  Example-1
  
| Employee | office |
| --- | --- |
| *EmpName | *office_code |
| Last_name | city |
|email|phone|

<ul>
  <li>From above column we have EmpName and office_code as primary keys in their respective tabel</li>
  <li>The employee tabel can belong to only one office , while an office can have zero or more employes.</li>
</ul>

# 6.Star and Snowflake Schema
Schema :- A schema is an outline of the entire data model and shows how different data sets are connected and how the various attributes of each data set are used for the database design.

![image](https://github.com/Prathama-sanshi/SQL/assets/59955378/c021d721-1743-40b8-8c3d-03258542c617)

| Star Schema | Snowflake Schema |
| --- | --- |
| Simplest schema | extension of star schema |
| Resembles star structure| Resembles snowflake structure|
|Good for querying large datasets|Good for querying small datasets|
|follows top down approach|follows bottom to top approach|
|Takes more space|Takes less space|
|Good for datamarts| Good for data warehousing|

# 7.OLTP vs OLAP

| Online Transactional Processing System(OLTP)| Online Analytical Processing System(OLAP) |
| --- | --- |
| Transactional database is also known as OLTP | Dataware house is also known as OLAP|
|To perform business transactions|To conduct analysis and decision making|
|It uses DBMS and service side appliaction-api|Uses ETL(Extract ,transform, and Load|
|Frond end technology-Web Servers, mobile phones,browsers for interaction|BI tools, cognos ,tabula etc|
|Database design:based on integrity issues and normalisations|Based on dimentional modelling|

# 8.Entity Constrains:-
Constraints are the rules used in mysql to restrict the values that can be stored in column of a database.
This will ensure data integrity , which is nothing but accuracy and consistancy of data stored in database.
<ol>
  <li>Unique:- This constraint is used for columns that need unique values. Eg:employee_id </li>
  
  ```
ALTER TABLE table_name
ADD CONSTRAINT constraint_name UNIQUE(column_list);
  ```

Note: Unique constraint can co-exist with null constraint in a relational data model .(except for null, all records in that column needs to be unique.)
  <li>NULL: This constraint is used to determine the columns that can have null values. Eg:- locations- some prefer not give hence marked null.</li>
  <li>NOT NULL: Ensure that a column cannot have null values.</li>
  <li>CHECK: Ensures that a column will not accept data values outside the specified range.

  ```
CREATE TABLE Persons (
    ID int NOT NULL,
    LastName varchar(255) NOT NULL,
    FirstName varchar(255),
    Age int,
    CHECK (Age>=18)
);
```
  
  </li>
  <li>DEFAULT: specifies a default value of a column if no values is supplies when adding a record to a tabel.
    
  ```
ALTER TABLE Persons
ALTER City SET DEFAULT 'Sandnes';
  ```
  </li>
  <li>Primary key: Ensures the uniqueness of records within a table.Its purpose is to uniquely identify each record in table.(since a column that is a primary key cannot duplicate and null values , it enforces both the unique and not null constraints automatically)
    
  ```
ALTER TABLE Persons
ADD CONSTRAINT PK_Person PRIMARY KEY (ID);
```
  </li>
  <li>Composit key: It is a combination of multiple columns and these columns are used to identify all the rows that are involved uniquely.
    
   ```
ALTER TABLE Persons
ADD CONSTRAINT PK_Person PRIMARY KEY (ID,LastNam);
```
  </li>
</ol>








