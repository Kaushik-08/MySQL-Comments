# MySQL
### mysql> show databases;
| Database           |
|--------------------|
| information_schema |
| mysql              |
| performance_schema |
| prasanna           |
| sakila             |
| sys                |
| world              |

7 rows in set (0.00 sec)

### USE prasanna;
Database changed

### CREATE TABLE userlist(Id int primary key auto_increment, Firstname varchar(255), Lastname varchar(255),Age int(2), dateofbirth date);
Query OK, 0 rows affected, 1 warning (0.03 sec)

### DESC prasanna;
| Field | Type        | Null | Key | Default | Extra          |
|-------|-------------|------|-----|---------|----------------|
| Id    | int         | NO   | PRI | NULL    | auto_increment |
| name  | varchar(45) | NO   | UNI | NULL    |                |

2 rows in set (0.01 sec)
