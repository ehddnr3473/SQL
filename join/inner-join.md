# INNER JOIN

양쪽 테이블에서 값이 일치하는 레코드 반환

## Syntax

```sql
SELECT column_name(s)
FROM table1
INNER JOIN table2
ON table1.column_name = table2.column_name;
```

<br>

### 예시

#### INNER JOIN

```sql
SELECT Orders.OrderID, Customers.CustomerName, Orders.OrderDate
FROM Orders
INNER JOIN Customers ON Orders.CustomerID=Customers.CustomerID;
```

INNER JOIN 키워드는 열 간에 일치하는 경우 두 테이블 모두에서 모든 행을 선택함. "Orders" 테이블과 "Customers" 테이블에 일치하는 레코드가 없는 경우, 주문 항목은 표시되지 않음.

<br>

#### INNER JOIN using Alias

```sql
SELECT o.OrderID, c.CustomerName, o.OrderDate
FROM Orders AS o
INNER JOIN Customers AS c ON o.CustomerID = c.CustomerID;
```

INNER JOIN 절에는 테이블의 별칭이 아닌 **테이블의 실제 이름**을 명시

<br>

#### JOIN Three Tables

아래 SQL문은 customer, shipper 정보와 함께 orders를 추출

```sql
SELECT Orders.OrderID, Customers.CustomerName, Shippers.ShipperName
FROM ((Orders
INNER JOIN Customers ON Orders.CustomerID = Customers.CustomerID)
INNER JOIN Shippers ON Orders.ShipperID = Shippers.ShipperID);
```
