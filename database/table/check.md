# CHECK

- CHECK 제약 조건은 값의 범위를 제한하기 위해서 사용한다. 

## 예시

### CHECK on CREATE TABLE

#### 단일 열 CHECK

```sql
CREATE TABLE Members (
  id int NOT NULL, 
  name varchar(255) NOT NULL, 
  age int, 
  CHECK (age >= 18)
)
```

<br>

#### 제약 사항 이름 설정 및 여러 열 CHECK

```sql
CREATE TABLE Members (
  id int NOT NULL, 
  name varchar(255) NOT NULL, 
  age int, 
  city varchar(255), 
  CONSTRAINT CHK_Member CHECK (age >= 18 AND city = 'Seoul')
)
```