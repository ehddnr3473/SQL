# BACKUP - MySQL

- 백업

```shell
$ mysqldump -u 사용자이름 -p 데이터베이스이름 > 백업파일이름.sql
```

<br>

- 복원

```shell
$ mysql -u 사용자이름 -p 데이터베이스이름 < 백업파일이름.sql
```

'데이터베이스이름'에 해당하는 데이터베이스가 없다면, 생성 후 복원 가능