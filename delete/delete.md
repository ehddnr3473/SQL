# DELETE

## Syntax

```sql
DELETE FROM table_name WHERE condition;
```

- **주의) 레코드를 삭제할 때, WHERE 절을 적어주지 않으면, 테이블의 모든 레코드가 삭제된다.**

- 따라서 table structure, attributes와 indexes를 유지하면서 테이블의 모든 레코드를 삭제하는 방법은 다음과 같음.
  - ```sql
    DELETE FROM table_name;
    ```

### 예시

```sql
DELETE FROM Customers
WHERE CustomerName = 'Dongwook';
```
