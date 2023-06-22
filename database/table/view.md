# VIEW

SQL 문의 결과 집합을 기반으로 한 가상 테이블

<br>

## Syntax

```sql
CREATE VIEW view_name AS
SELECT column1, column2, ...
FROM table_name
WHERE condition;
```

<br>

### 예시

#### View 생성

```sql
CREATE VIEW [Brazil Customers] AS
SELECT CustomerName, ContactName
FROM Customers
WHERE Country = 'Brazil';
```

<br>

```sql
CREATE VIEW [Product Above Average Price] AS
SELECT ProductName, Price
FROM Products
WHERE Price > (SELECT AVG(Price) FROM Products);
```

<br>

#### 생성한 View 검색

```sql
SELECT * FROM [Brazil Customers];
```

<br>

```sql
SELECT * FROM [Product Above Average Price];
```