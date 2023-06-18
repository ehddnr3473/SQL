# SELECT DISTINCT

필드에서 중복된 값 없이 데이터를 추출하는 데 사용

## Syntax

```sql
SELECT DISTINCT column1, column2, ...
FROM table_name;
```

### 예시

```sql
SELECT DISTINCT Country FROM Customers;
```

```sql
SELECT COUNT(DISTINCT Country) FROM Customers;
```
