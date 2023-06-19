# Data Types - MySQL(Version 8.0)

## String Data Types

- CHAR(size)
  * 고정 길이의 문자열을 저장하는 타입
  * 최대 길이를 지정해야 하며, 0 ~ 255까지 가능. 기본 값은 1. 
  * 지정된 길이보다 짧은 문자열을 저장할 경우 공백으로 채워짐.

- VARCHAR(size)
  * 가변 길이의 문자열을 저장하는 타입
  * 최대 길이를 지정해야 하며, 지정된 길이보다 짧은 문자열을 저장할 경우 실제 문자열 길이만큼만 저장됨. 
  * size는 해당 varchar 필드가 저장할 수 있는 최대 문자의 개수를 나타냄.

- TEXT(size)
  * 가변 길이의 긴 문자열을 저장하는 타입
  * 최대 길이가 65,535 바이트로, 대용량의 텍스트 데이터를 저장할 수 있음.

<br>

## Numeric Data Types

- INT(size): 
  * 정수 값을 저장하는 타입
  * 보통 4바이트를 사용
  * -2,147483648 ~ 2,147,483,647 까지의 범위를 가짐.

- BIGINT(size)
  * 큰 정수 값을 저장하는 타입
  * 8바이트를 사용
  * -9,223,372,036,854,775,808 ~ 9,223,372,036,854,775,807 까지의 범위를 가짐.

- FLOAT
  * 부동 소수점 숫자를 저장하는 타입
  * 약 7자리 까지의 정확도를 가짐.

- DOUBLE
  * 두 배의 부동 소수점 숫자를 저장하는 타입
  * 약 15 자리까지의 정확도를 가짐.

- DECIMAL(size, d)
  * 총 자릿수는 size로 지정
  * 소수점 이하의 자릿수는 d로 지정
  * size의 최댓값은 65, d의 최댓값은 30
  * 기본 값은 size: 10, d: 0

- BOOL: zero == false, nonzero == true

<br>

## Date and Time Data Types

- DATE
  * 날짜 값을 저장하는 타입
  * Format: YYYY-MM-DD. 
  * 지원하는 범위: '1000-01-01' ~ '9999-12-31'

- DATETIME
  * 날짜와 시간 값을 저장하는 타입
  * Format: YYYY-MM-DD HH:MM:SS

- TIME
  * 시간 값을 저장하는 타입
  * Format: HH:MM:SS

- TIMESTAMP
  * 날짜와 시간 값을 저장하는 타입
  * 타임스탬프 값은 Unix epoch('1970-01-01 00:00:00' UTC) 이후의 초 단위로 저장됨.
  * Format: YYYY-MM-DD hh:mm:ss
  * 지원되는 범위: '1970-01-01 00:00:01' UTC ~ '2038-01-09 03:14:07' UTC
  * 열 정의에서 DEFAULT CURRENT_TIMESTAMP 및 ON UPDATE CURRENT_TIMESTAMP를 명시해서 현재 날짜 및 시간으로 자동 초기화 및 업데이트를 지정할 수 있음.

- YEAR
  * four-digit를 사용해서 연도를 저장하는 타입