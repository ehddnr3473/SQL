# FOREIGN KEY

- 외래 키는 테이블 간의 연결을 끊는 행위를 방지하기 위한 제약 조건이다.

- 외래 키는 다른 테이블의 **기본 키**를 참조하는 필드(또는 필드 집합)이다.

- 외래 키를 가지고 있는 테이블을 child table, 기본 키를 가지고 있는 테이블을 referenced or parent table이라고 한다.

<br>

## 예시 - MySQL

### FOREIGN KEY on CREATE TABLE

#### 단일 열 

```sql
CREATE TABLE Orders (
  OrderID int NOT NULL, 
  OrderNumber int NOT NULL, 
  PersonID int, 
  PRIMARY KEY (OrderID), 
  FOREIGN KEY (PersonID) REFERENCES Persons(PersonID)
);
```

<br>

#### FOREIGN KEY 제약 조건에 이름을 붙여주거나 여러 열을 제약 조건으로 사용하려면:

```sql
CREATE TABLE Orders (
  OrderID int NOT NULL, 
  OrderNumber int NOT NULL, 
  PersonID int, 
  PRIMARY KEY (OrderID), 
  CONSTRAINT FK_PersonOrder FOREIGN KEY (PersonID) 
  REFERENCES Persons(PersonID)
)
```

<br>

### FOREIGN KEY on ALTER TABLE

#### Orders 테이블이 이미 존재한다면:

```sql
ALTER TABLE Orders
ADD FOREIGN KEY (PersonID) REFERENCES Persons(PersonID);
```

<br>

#### 제약 조건에 이름을 붙여주거나 여러 열을 제약 조건으로 사용하려면:

```sql
ALTER TABLE Orders
ADD CONSTRAINT FK_PersonOrder
FOREIGN KEY (PersonID) REFERENCES Persons(PersonID);
```

<br>

### DROP a FOREIGN KEY Constraint

```sql
ALTER TABLE Orders
DROP FOREIGN KEY FK_PersonOrder;
```