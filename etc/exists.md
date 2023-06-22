# EXISTS

- Subquery를 통해서, 레코드가 존재하는지 확인하는 연산자

- EXISTS 연산자는 Subquery가 하나 이상의 레코드를 반환하면, TRUE를 반환한다. 따라서 외부 쿼리의 WHERE 절을 만족하게 되면, 결과에 그 레코드가 포함됨(마치 반복문의 조건과 같이).

<br>

## Syntax

```sql
SELECT column_name(s)
FROM table_name
WHERE EXISTS
(SELECT column_name FROM table_name WHERE condition);
```

<br>

### 예시

#### 가격이 20 미만인 상품을 가진 공급업체 이름을 반환하는 쿼리

```sql
SELECT SupplierName
FROM Suppliers
WHERE EXISTS (SELECT ProductName FROM Products WHERE Products.SupplierID = Suppliers.supplierID AND Price < 20);
```

<br>

#### 주문을 한 번 이상 한 고객의 이름을 반환하는 쿼리

```sql
SELECT CustomerName
FROM Customers
WHERE EXISTS (
  SELECT *
  FROM Orders
  WHERE Orders.CustomerID = Customers.CustomerID
);
```

EXISTS 연산자를 사용하여 주문을 한 번 이상 한 고객의 존재 여부를 확인하고, EXISTS결과가 True인 경우 해당 고객의 이름을 반환. 결과가 False인 경우, 결과에 포함되지 않음.