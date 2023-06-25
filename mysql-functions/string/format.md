# FORMAT

number를 "#,###,###.##" 포맷으로 반올림 및 변환하여, string으로 반환

<br>

## Syntax

```sql
SELECT FORMAT(number, decimal_places)
```

- number, decimal_places: Required

- decimal_places가 0일 때, 소수점 이하가 없는 문자열 반환(반올림은 수행)

<br>

### 예시

```sql
SELECT FORMAT(250500.5634, 2); -- 250,500.56
```