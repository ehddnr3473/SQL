# INDEX

- 인덱스는 데이터베이스에서 테이블의 특정 열에 대한 **검색** 및 **정렬** 성능을 향상시키기 위해 사용함.

- 인덱스는 특정 열에 대한 정렬된 데이터 구조로, 테이블의 각 행의 값과 해당 행의 물리적 위치를 매핑함. 따라서 특정 열의 값을 기준으로 빠르게 원하는 데이터를 찾을 수 있음.

- 인덱스를 사용하는 것은 일반적으로 검색 성능을 향상시키는 장점을 가지지만, 인덱스 자체는 데이터베이스의 용량을 증가시키고 데이터 변경 작업(삽입, 갱신, 삭제)에 대한 성능을 감소시킬 수 있음. 따라서 인덱스는 데이터베이스의 특정 요구 사항과 작업 부하 패턴에 맞게 신중하게 설계되어야 함.

<br>

## 인덱스를 사용하는 상황

- 검색 속도 향상: 특정 열의 값을 기준으로 레코드를 검색하는 데 필요한 시간을 줄일 수 있음. 데이터베이스는 해당 열의 값이 일치하는 레코드를 더 빠르게 찾을 수 있음.

- 정렬 성능 향상: 특정 열을 기준으로 정렬된 결과를 필요로 할 때, 인덱스를 사용하면 데이터베이스는 인덱스의 정렬 순서에 따라 데이터를 반환하므로 정렬 작업의 성능이 향상됨.

- 중복 값 제한: 인덱스를 사용하면 해당 열에 대해 고유한 값을 유지할 수 있음. 이를 통해 중복된 값을 허용하지 않는 데이터의 무결성을 유지할 수 있음.

<br>

## Syntax

#### INDEX(중복값 허용)

```sql
CREATE INDEX index_name
ON table_name (column1, column2, ...);
```

<br>

#### UNIQUE INDEX(해당 열의 각 값이 고유해야 함.)

```sql
CREATE UNIQUE INDEX index_name
ON table_name (column1, column2, ...);
```

<br>

#### DROP INDEX Statement

```sql
ALTER TABLE table_name
DROP INDEX index_name;
```

<br>

### 예시

#### Single column

```sql
CREATE INDEX idx_lastname
ON Members (lastName);
```

<br>

#### Combination of columns

```sql
CREATE INDEX idx_mname
ON Members (lastName, firstName);
```

