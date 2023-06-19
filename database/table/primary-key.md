# PRIMARY KEY

### 예시

#### PRIMARY KEY on CREATE TABLE - MySQL

```sql
CREATE TABLE Members (
  id int NOT NULL, 
  name varchar(255) NOT NULL, 
  age int, 
  PRIMARY KEY (id)
);
```

<br>

#### PK 제약 조건에 이름을 부여하거나 여러 열을 조합하기 위한 syntax 예시

```sql
CREATE TABLE Members (
  id int NOT NULL, 
  name varchar(255) NOT NULL, 
  age int, 
  CONSTRAINT PK_Member PRIMARY KEY (id, name)
);
```

<br>

#### PRIMARY KEY on ALTER TABLE

```sql
ALTER TABLE Members
ADD PRIMARY KEY (id);
```

```sql
ALTER TABLE Members
ADD CONSTRAINT PK_Person PRIMARY KEY (id, name);
```

<br>

#### DROP a PRIMARY KEY Constraint - MySQL

```sql
ALTER TABLE Members
DROP PRIMARY KEY;
```