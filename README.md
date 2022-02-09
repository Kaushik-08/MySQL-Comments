# MySQL
### mysql> SHOW DATABASES;
| Database           |
|--------------------|
| information_schema |
| mysql              |
| performance_schema |
| prasanna           |
| sakila             |
| sys                |
| world              |

###### 7 rows in set (0.00 sec)

### mysql> USE prasanna;
###### Database changed

### mysql> CREATE TABLE userlist(Id int primary key auto_increment, Firstname varchar(255), Lastname varchar(255),Age int(2), dateofbirth date);
###### Query OK, 0 rows affected, 1 warning (0.03 sec)

### mysql> DESC userlist;

| Database           |
|--------------------|
| information_schema |
| mysql              |
| performance_schema |
| prasanna           |
| sakila             |
| sys                |
| world              |
| Field       | Type         | Null | Key | Default | Extra          |
|-------------|-------------------------------------|----------------|
| Id          | int          | NO   | PRI | NULL    | auto_increment |
| Firstname   | varchar(255) | YES  |     | NULL    |                |
| Lastname    | varchar(255) | YES  |     | NULL    |                |
| Age         | int          | YES  |     | NULL    |                |
| dateofbirth | date         | YES  |     | NULL    |                |

###### 5 rows in set (0.01 sec)
