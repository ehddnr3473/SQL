# ANY Opterator

- 결과로 boolean 값 반환

- ANY of the subquery values, 서브쿼리의 결과 중 하나 이상의 조건을 만족하는지 확인. 만족하면 TRUE 반환.

<br>

## Syntax

```sql
SELECT column_name(s)
FROM table_name
WHERE column_name operator ANY
    (SELECT column_name
    FROM table_name
    WHERE condition);
```

> Note: The operator must be a standard comparison operator (=, <>, !=, >, >=, <, or <=).

<br>

### 예시

```sql
SELECT * FROM Products
WHERE Price >= ANY
    (SELECT Price
    FROM Products
    WHERE Price >= 100);
```

위의 예시에서 서브쿼리는 Products 테이블에서 Price 값이 100 이상인 모든 제품의 가격을 반환함. 
그런 다음 메인 쿼리에서는 Price 열이 ANY 연산자를 사용하여 서브쿼리의 결과와 비교함. 
따라서 메인 쿼리는 Price 값이 100 이상인 제품을 반환함.

<br>

```sql
SELECT ProductName
FROM Products
WHERE ProductID = ANY
    (SELECT ProductID
    FROM OrderDetails
    WHERE Quantity = 10);
```

OrderDetails 테이블에서 찾은 상품의 양의 10이라면 해당 상품의 이름을 나열