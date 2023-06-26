# CAST

## Syntax

```sql
CAST(value AS datatype)
```

<br>

## Parameter Values

|Datatype|Description|
|---|---|
|DATE|Format: "YYYY-MM-DD"|
|DATETIME|Format: "YYYY-MM-DD HH:MM:SS"|
|DECIMAL|_|
|TIME|Format: "HH:MM:SS"|
|CHAR|a fixed length string|
|NCHAR|like CHAR, but produces a string with the national character set. 고정 길이의 유니코드 문자열 데이터를 저장|
|SIGNED|a signed 64-bit integer|
|UNSIGNED|an unsigned 64-bit integer|
|BINARY|a binary string|

<br>

### 예시

```sql
SELECT CAST("2017-08-29" AS DATE);
```

```sql
SELECT CAST(5-10 AS SIGNED); -- -5
```

