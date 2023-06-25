# LOWER

- 문자열을 lower-case로 변환

- LCASE() 함수와 같음.

<br>

## Syntax

```sql
LOWER(text)
```

<br>

### 예시

```sql
SELECT LOWER(CustomerName) AS LowercaseCustomerName
FROM Customers;
```

<br>

# UPPER

- 문자열을 upper-case로 변환

- UCASE() 함수와 같음.

<br>

## Syntax

```sql
UPPER(text)
```

<br>

### 예시

```sql
SELECT UPPER(CustomerName) AS UppercaseCustomerName
FROM Customers;
```
