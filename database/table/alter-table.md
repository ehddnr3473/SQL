# ALTER TABLE

- 테이블의 열을 추가, 수정, 삭제할 때 사용

- 테이블의 다양한 Constraints(제약조건)을 추가 및 삭제할 때 사용

## Syntax

### ALTER TABLE - COLUMN NAME

#### ADD Column

```sql
ALTER TABLE table_name
ADD column_name datatype;
```

<br>

#### DROP COLUMN

```sql
ALTER TABLE table_name
DROP COLUMN column_name;
```

<br>

#### RENAME COLUMN

```sql
ALTER TABLE table_name
RENAME COLUMN old_name to new_name;
```

<br>

### ALTER TABLE - COLUMN DATATYPE

#### MODIFY DATATYPE - MySQL

```sql
ALTER TABLE table_name
MODIFY COLUMN column_name datatype;
```