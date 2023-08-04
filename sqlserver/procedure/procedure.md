# PROCEDURE
Stored procedure는 저장하여 재사용할 수 있는 SQL 코드임.


## Syntax

```sql
CREATE PROCEDURE procedure_name
AS
sql_statement
GO;
```

<br>

## Execute a Stored Procedure

```sql
EXEC procedure_name;
```

<br>

### 예시

#### Procedure

```sql
CREATE PROCEDURE Pr_User_Insert
(
    @UserName VARCHAR(50), 
    @CountOfRecords INT OUTPUT
)
AS
BEGIN
    INSERT INTO [dbo].[TEST_TABLE] ([name])
    VALUES (@UserName)

    SELECT * FROM [dbo].[TEST_TABLE]

    SELECT @CountOfRecords = @@ROWCOUNT;
END
```

<br>

#### Execute
```sql
DECLARE @Count VARCHAR(10)
DECLARE @Name VARCHAR(50)

SET @Name = 'Kim'

EXEC [dbo].[Pr_User_Insert] @UserName = @Name, @CountOfRecords = @Count OUTPUT
PRINT 'Total number of users is ' + @Count
```