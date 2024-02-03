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

