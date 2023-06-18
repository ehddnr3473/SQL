# LEFT JOIN
왼쪽 테이블에서 모든 레코드를 반환하고, 오른쪽 테이블에서 일치하는 레코드를 반환함. 일치하는 레코드가 없을 경우 오른쪽 테이블의 열들은 NULL 값으로 채워짐.

## Syntax

```sql
SELECT column_name(S)
FROM table1
LEFT JOIN table2
ON table1.column_name = table2.column_name;
```

### 예시

- 모든 고객의 주문 내역을 반환하는 SQL문
- 고객과 주문은 1 : N 관계

```sql
SELECT Customers.CustomerName, Orders.OrderID
FROM Customers
LEFT JOIN Orders 
ON Customers.CustomerID = Orders.CustomerID
ORDER BY Customers.CustomerName;
```