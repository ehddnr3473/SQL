# HAVING

WHERE 키워드가 집계(aggregate) 함수와 함께 사용할 수 없으므로 HAVING 절을 사용한다.

<br>

## Syntax

```sql
SELECT column_name(s)
FROM table_name
WHERE condition
GROUP BY column_name(s)
HAVING condition
ORDER BY column_name(s);
```

<br>

### 예시

#### 고객수 5명 이상인 도시를 포함하는 레코드, 고객수 기준 내림차순 정렬

```sql
SELECT COUNT(CustomerID), Country
FROM Customers
GROUP BY Country
HAVING COUNT(CustomerID) > 5;
ORDER BY COUNT(CustomerID) DESC;
```

<br>

#### 직원 중 10개 이상의 주문을 담당하는 직원 검색
```sql
SELECT Employees.LastName, COUNT(Orders.OrderID) AS NumberOfOrders
FROM (Orders
INNER JOIN Employees ON Orders.EmployeeID = Employees.EmployeeID)
GROUP BY LastName
HAVING COUNT(Orders.OrderID) > 10;
```

<br>

#### 직원, 'Davolio' 또는 'Fuller' 중, 25개 이상의 주문을 담당하는 직원 검색
```sql
SELECT Employees.LastName, COUNT(Orders.OrderID) AS NumberOfOrders
FROM (Orders
INNER JOIN Employees ON Orders.EmployeeID = Employees.EmployeeID)
WHERE LastName = 'Davolio' OR 'Fuller'
GROUP BY LastName
HAVING COUNT(Orders.OrderID) > 25;
```