# ORDER BY

## Syntax

```sql
SELECT column1, column2, ...
FROM table_name
ORDER BY column1, column2, ... ASC|DESC;
```

- ORDER BY 키워드는 기본적으로 오름차순 정렬
- 내림차순으로 정렬하기 위해, DESC 키워드를 사용

### 예시

- 오름차순

```sql
SELECT * FROM Customers
ORDER BY Country;
```

- 내림차순

```sql
SELECT * FROM Customers
ORDER BY Country DESC;
```

- ORDER BY Several Columns

```sql
SELECT * FROM Customers
ORDER BY Country ASC, CustomerName DESC;
```

1. "Country"에 대해서 오름차순으로 정렬
2. "Country"가 같은 레코드들은, 다시 "CustomerName"에 대해서 내림차순 정렬
