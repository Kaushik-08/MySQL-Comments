# MySQL Comments
```syntax
SHOW DATABASES;
```
| Database           |
|:----:|
| information_schema |
| mysql              |
| performance_schema |
| prasanna           |
| sakila             |
| sys                |
| world              |

###### 7 rows in set (0.00 sec)

```syntax
USE prasanna;
```
###### Database changed

```syntax
CREATE TABLE userlist(Id int primary key auto_increment, Firstname varchar(255), Lastname varchar(255), Age int(2), dateofbirth date);
```
###### Query OK, 0 rows affected, 1 warning (0.03 sec)

```syntax
DESC userlist
```

| Field       | Type         | Null | Key | Default | Extra          |
|:----:|:----:|:----:|:----:|:----:|:----:|
| Id          | int          | NO   | PRI | NULL    | auto_increment |
| Firstname   | varchar(255) | YES  |     | NULL    |                |
| Lastname    | varchar(255) | YES  |     | NULL    |                |
| Age         | int          | YES  |     | NULL    |                |
| dateofbirth | date         | YES  |     | NULL    |                |

###### 5 rows in set (0.01 sec)
