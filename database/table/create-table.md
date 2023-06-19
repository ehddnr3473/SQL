# CREATE TABLE

데이터베이스에 새로운 테이블 생성

## Syntax

#### Basic

```sql
CREATE TABLE table_name (
  column1 datatype, 
  column2 datatype, 
  column3 datatype, 
  ...
);
```

- The column parameters specify the names of the columns of the table.

- The datatype parameter specifies the type of data the column can hold (e.g. varchar, integer, date, etc.).

<br>

#### Create table using another table

```sql
CREATE TABLE new_table_name AS
  SELECT column1, column2, ...
  FROM existing_table_name
  WHERE ...;
```

<br>

### 예시

- Basic

```sql
CREATE TABLE Persons (
  PersonID int, 
  LastName varchar(255), 
  FirstName varchar(255), 
  Address varchar(255), 
  City varchar(255)
);
```

<br>

- Create table using another table

```sql
CREATE TABLE TestTable AS
  SELECT CustomerName, ContactName
  FROM Customers;
```
