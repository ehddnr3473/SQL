# DROP TABLE

## Syntax

#### 테이블 삭제

```sql
DROP TABLE table_name;
```

<br>

#### 테이블 구조를 유지하며 모든 데이터 삭제

```sql
TRUNCATE TABLE table_name;
```
- TRUNCATE TABLE은 DELETE 문보다 훨씬 빠르게 동작하며, 대량의 데이터를 처리하는 경우에 유용함.

<br>

### 에시

```sql
DROP TABLE Shippers;
```