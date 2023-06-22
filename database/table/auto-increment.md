# AUTO INCREMENT Field

AUTO_INCREMENT는 테이블에 새로운 레코드가 삽입될 때, 자동으로 생성된 고유한 번호를 가질 수 있도록 해준다. 따라서 기본 키 필드로서 사용하기도 한다.

<br>

## Syntax for MySQL

- By dafault, the starting value for AUTO_INCREMENT is 1, and it will increment by 1 for each new record.

```sql
CREATE TABLE Members (
  id int AUTO_INCREMENT, 
  name varchar(255) NOT NULL, 
  age int, 
  PRIMARY KEY id
);
```

<br>

- AUTO_INCREMENT의 시작값으로 다른 값을 설정하고 싶다면:
- 아래 SQL문에서 유추할 수 있듯이, **AUTO_INCREMENT는 하나의 열에만 적용할 수 있음.**

```sql
ALTER TABLE Members AUTO_INCREMENT = 100;
```

