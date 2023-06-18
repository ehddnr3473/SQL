# INSERT INTO

## Syntax

1. 필드 이름과 값을 명시

```sql
INSERT INTO table_name (column1, column2, column3, ...)
VALUES (value1, value2, value3, ...);
```

2. 모든 필드에 값을 입력한다면, 필드 이름을 명시할 필요 없음. 하지만, 테이블의 필드 순서와 똑같이 값을 나열해야 함.

```sql
INSERT INTO table_name
VALUES (value1, value2, value3, ...);
```

### 예시

```sql
INSERT INTO Customers (CustomerName, City, Country)
VALUES ('Dongwook', 'Seoul', 'South Korea');
```
