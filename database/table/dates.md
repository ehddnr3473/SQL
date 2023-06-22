# Dates

## SQL Date Data Types - MySQL

#### format

- DATE: YYYY-MM-DD
- DATETIME: YYYY-MM-DD HH:MI:SS
- TIMESTAMP: YYYY-MM-DD HH:MI:SS
- YEAR: YYYY or YY

<br>

## 예시

```sql
SELECT * FROM Orders
WHERE OrderDate = '2008-11-11';
```

#### DB에 저장된 OrderDate 값이 "2008-11-11" 일 때:
정상적으로 검색됨.

<br>

#### DB에 저장된 OrderDate 값이 "2008-11-11 13:23:44" 일 때:
위의 SQL 문으로는 아무런 결괏값을 얻을 수 없음. WHERE 절에 time 부분이 없기 떄문.