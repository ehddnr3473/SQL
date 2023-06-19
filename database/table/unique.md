# UNIQUE

### 예시

#### 하나의 열

```sql
CREATE TABLE Members (
  id int NOT NULL, 
  name varchar(255) NOT NULL, 
  age int
  UNIQUE (id)
);
```

<br>

#### 여러 열을 조합한 유일성 제약 조건

```sql
CREATE TABLE Members (
    id int NOT NULL,
    name varchar(255) NOT NULL,
    age int,
    CONSTRAINT UC_Person UNIQUE (id, name)
);
```

UC_Person은 'Unique Constraint'를 의미하는 것으로, 제약 조건의 이름을 나타내는 식별자이다. 제약 조건 이름을 지정하는 것은 선택 사항이며, 이름을 지정함으로써 해당 제약 조건을 참조하거나 관리하는 데 도움을 줄 수 있다.
id와 name 열의 조합은 유일해야 하므로, 데이터베이스에서 동일한 id와 name을 가진 두 개 이상의 행을 삽입하는 것을 방지할 수 있다.

<br>

#### Constraint on ALTER TABLE

```sql
ALTER TABLE Members
ADD UNIQUE (id);
```

<br>

#### DROP a UNIQUE Constraint - MySQL

```sql
ALTER TABLE Members
DROP INDEX UC_Person;
```