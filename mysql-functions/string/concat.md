# CONCAT

두 개 이상의 문자열(식)을 결합

<br>

## Syntax

```sql
CONCAT(expression1, expression2, expression3, ...)
```

expression: 문자열 값이나 열의 이름

<br>

### 예시

```sql
SELECT CustomerName, CONCAT(Address, " ", PostalCode, " ", City) AS Address
FROM Customers;
```

#### 결과

| CustomerName | Addess                 |
| ------------ | ---------------------- |
| Dongwook     | Daehak-dong 1234 Seoul |
