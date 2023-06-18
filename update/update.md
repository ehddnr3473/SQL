# UPDATE

## Syntax

```sql
UPDATE table_name
SET column1 = value1, column2 = value2, ...
WHERE condition;
```

**주의) 레코드를 업데이트할 때, WHERE 절을 적어주지 않으면, 테이블의 모든 레코드가 업데이트 된다.**

### 예시

- UPDATE Table

```sql
UPDATE Customers
SET CustomerName = 'Yeolmok', City = 'Masan'
WHERE CustomerID = 1;
```

- UPDATE Multiple Records

```sql
UPDATE Customers
SET ContactName = 'Juan'
WHERE Country = 'Mexico'
```
