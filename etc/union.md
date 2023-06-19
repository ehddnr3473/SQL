# UNION

둘 이상의 SELECT 문의 결과를 결합하여 단일 결과 집합 생성

- UNION operator를 사용할 때, 모든 SELECT 문의 열 수와 데이터 타입은 같아야 함.

<br>

## Syntax

```sql
SELECT column_name(s) FROM table1
UNION
SELECT column_name(s) FROM table2;
```

- 중복된 행이 제거되므로 결과 집합에는 고유한(DISTINCT) 행들만 포함됨.

- 아래와 같이 **UNION ALL**을 사용해서 중복 값을 허용할 수 있음.

```sql
SELECT column_name(s) FROM table1
UNION ALL
SELECT column_name(s) FROM table2;
```

<br>

### 예시

- UNION

```sql
SELECT City FROM Customers
UNION
SELECT City FROM Suppliers
ORDER BY City;
```

<br>

- UNION With WHERE

```sql
SELECT City, Country FROM Customers
WHERE Country = 'Germany'
UNION
SELECT City, Country FROM Suppliers
WHERE Country = 'Germany'
ORDER BY City;
```

<br>

- UNION With Alias

```sql
SELECT 'Customer' AS Type, ContactName, City, Country
FROM Customers
UNION
SELECT 'Supplier', ContactName, City, Country
FROM Suppliers;
```

쿼리를 수행하는 동안 유효한, Type이라는 alias를 가지는 열을 생성해서, 고객인지 공급자인지 구분함.