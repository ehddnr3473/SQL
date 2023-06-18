# RIGHT JOIN
오른쪽 테이블에서 모든 레코드를 반환하고, 왼쪽 테이블에서 일치하는 레코드를 반환함. 일치하는 레코드가 없을 경우 왼쪽 테이블의 열들은 NULL 값으로 채워짐.

## Syntax

```sql
SELECT column_name(s)
FROM table1
RIGHT JOIN table2
ON table1.column_name = table2.column_name;
```

### 예시

```sql
SELECT Orders.OrderID, Employees.LastName, Employees.FirstName
FROM Orders
RIGHT JOIN Employees
ON Orders.EmployeeID = Employees.EmployeeID
ORDER BY Orders.OrderID;
```

- 주문 받은 기록이 없는 직원의 OrderID 열은 NULL로 채워짐.