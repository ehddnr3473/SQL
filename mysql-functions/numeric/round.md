# ROUND

수를 특정 소수점 이하 자리 수 기준으로 반올림하는 함수

<br>

## Syntax

```sql
ROUND(number, decimal)
```

- decimal의 기본값은 0. 생략 가능
- decimal이 2인 경우, 소수점 이하 3번째 자리에서 반올림

<br>

### 예시

```sql
SELECT ROUND(345.156, 0); -- 345
```
