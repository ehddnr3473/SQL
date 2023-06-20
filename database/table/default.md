# DEFAULT

- 열에 기본값을 설정하는 제약 조건

- 새로운 레코드의 필드에 값을 명시하지 않는다면, 기본값이 적용됨.

## 예시

### DEFAULT on CREATE TABLE

```sql
CREATE TABLE Members (
  id int NOT NULL, 
  name varchar(255) NOT NULL, 
  age int, 
  city varchar(255) DEFAULT 'Seoul'
);
```

<br>

- DEFAULT 제약 조건은 다음과 같이 시스템값을 삽입할 수도 있음.

```sql
CREATE TABLE Orders (
  id int NOT NULL, 
  orderNumber int NOT NULL, 
  orderDate date DEFAULT GETDATE()
);
```

<br>

### DEFAULT on ALTER TABLE

```sql
ALTER TABLE Members
ALTER city SET DEFAULT 'Seoul';
```