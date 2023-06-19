# Constraints

- 데이터의 무결성(Integrity)을 보장하기 위해 사용됨. 데이터의 정확성과 일관성을 유지하는 데 도움이 되며, 잘못된 데이터의 삽입 또는 갱신을 방지함.

- 제약 조건은 **CREATE TABLE** 문에서, 또는 생성된 이후 **ALTER TABLE** 문에서 명시됨.

- Constraints can be column level or table level.

<br>

## Syntax

```sql
CREATE TABLE table_name (
  column1 datatype constraint, 
  column2 datatype constraint, 
  ...
);
```

<br>

## Commonly used constraints

- NOT NULL: 열에 NULL 값이 들어갈 수 없도록 보장

- UNIQUE: 열의 모든 값이 다르도록 보장

- PRIMARY KEY: NOT NULL + UNIQUE

- FOREIGN KEY: 다른 테이블의 PK와 관계를 맺는 열. 외래 키 제약 조건은 참조 무결성을 유지하기 위해 사용되며, 테이블 간의 연결을 삭제하는 작업을 방지

- CHECK: 열의 값이 특정 조건을 만족하도록 보장

- DEFAULT: 아무런 값이 명시되지 않을 때 사용할 기본 값을 지정

- CREATE INDEX: 데이터베이스에서 빠르게 데이터를 생성하고 검색하기 위해 사용

<br>

### 예시

```sql
CREATE TABLE Member (
  id INT AUTO_INCREMENT PRIMARY KEY, 
  name VARCHAR(255), 
  age INT CHECK(age > 0 AND age < 150)
);
```

```sql
INSERT INTO Member (name, age) VALUES ('Dongwook', 28);
```