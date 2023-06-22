# CASE Expression

- if-then-else 문 처럼, 조건을 만족하는 첫 문장의 결과를 반환
- 만족하는 조건이 없다면, ELSE 절의 값을 반환
- ELSE 절도 없으면, NULL 반환

<br>

## Syntax

```sql
CASE
    WHEN condition1 THEN result1
    WHEN condition2 THEN result2
    WHEN conditionN THEN resultN
    ELSE result
END;
```

<br>

### 예시

#### SQL 문

```sql
SELECT OrderID, Quantity, 
CASE
    WHEN Quantity > 30 THEN 'The quantity is greater than 30'
    WHEN Quantity = 30 THEN 'The quantity is 30'
    ELSE 'The quantity is under 30'
END AS QuantityText
FROM OrderDetails;
```

<br>

#### 결과

|OrderID|Quantity|QuantityText|
|---|---|---|
|10248|12|The quantity is under 30|
|10249|40|The quantity is greater than 30|
|...|...|...|

<br>
<hr>
<br>

#### 도시명에 의해서 고객 정렬

```sql
SELECT CustomerName, City, Country
FROM Customers
ORDER BY
(CASE
    WHEN City IS NULL THEN Country -- 만약 도시명이 NULL이라면, 나라명으로 정렬
    ELSE City
END);
```

데이터가 아래와 같이 있다면:
<br>
(Ansan, South Korea), <br>
(NULL, France), <br>
(NULL, Argentina), <br>
(NULL, NULL), <br>
(California, USA)

<br>

다음과 같이 정렬:
1. (NULL, NULL)
2. (Ansan, South Korea)
3. (NULL, Argentina)
4. (California, USA)
5. (NULL, France)