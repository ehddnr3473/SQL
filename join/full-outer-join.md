# FULL OUTER JOIN

테이블 사이에서 일치하는 레코드뿐만 아니라 모든 레코드를 결합하여 결과를 생성함. 왼쪽 테이블과 오른쪽 테이블의 모든 레코드를 포함하며, 일치하는 레코드가 없는 경우에는 NULL 값을 사용하여 열을 채움.

## Syntax

```sql
SELECT column_name(s)
FROM table1
FULL OUTER JOIN table2
ON table1.column_name = table2.column_name
WHERE condition;
```

### 예시

```sql
SELECT Customers.CustomerName, Orders.OrderID
FROM Customers
FULL OUTER JOIN Orders ON Customers.CustomerID = Orders.CustomerID
ORDER BY Customers.CustomerName;
```