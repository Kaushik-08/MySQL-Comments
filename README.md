# MySQL Comments

**The SQL SHOW DATABASES Statement**

```syntax
SHOW DATABASES;
```
| Database           |
|:----|
| information_schema |
| mysql              |
| performance_schema |
| sakila             |
| sys                |
| world              |

###### 6 rows in set (0.00 sec)
* * *

### The SQL CREATE DATABASE Statement
```syntax
CREATE DATABASE freshclass;
```
```syntax
SHOW DATABASES;
```
| Database           |
|:----|
| freshclass         |
| information_schema |
| mysql              |
| performance_schema |
| sakila             |
| sys                |
| world              |

###### 7 rows in set (0.01 sec)
* * *

### The SQL USE DATABASE Statement
```syntax
USE freshclass;
```
###### Database changed
* * *

### The SQL CREATE TABLE Statement
```syntax
 CREATE TABLE studentslist(Id int primary key auto_increment, Firstname varchar(255) NOT NULL, Lastname varchar(255) NOT NULL,Email varchar(255) UNIQUE NOT NULL, Age int(2) NOT NULL, dateofbirth date NOT NULL);
```
###### Query OK, 0 rows affected, 1 warning (0.04 sec)
* * *

### The SQL SHOW TABLES Statement
```syntax
SHOW TABLES
```
| Tables_in_freshclass |
|:----|
| studentslist         |

###### 1 row in set (0.01 sec)
* * *
### The SQL DESCRIBE TABLE Statement
```syntax
DESC studentslist
```
```syntax
DESCRIBE studentslist
```
| Field       | Type         | Null | Key | Default | Extra          |
|:----|:----|:----:|:----:|:----:|:----|
| Id          | int          | NO   | PRI | NULL    | auto_increment |
| Firstname   | varchar(255) | NO   |     | NULL    |                |
| Lastname    | varchar(255) | NO   |     | NULL    |                |
| Email       | varchar(255) | NO   | UNI | NULL    |                |
| Age         | int          | NO   |     | NULL    |                |
| dateofbirth | date         | NO   |     | NULL    |                |

###### 6 rows in set (0.01 sec)
* * *

### The SQL INSERT INTO Statement

```syntax
INSERT INTO studentslist (Firstname,Lastname,Email,Age,dateofbirth) VALUES ('Prasanna','venkatsh','prasanna@freshclass.com','21','2001-01-20');
```

###### Query OK, 1 row affected (0.00 sec)

```syntax
INSERT INTO studentslist (Firstname,Lastname,Email,Age,dateofbirth) VALUES ('Vimal','raj','vimal@freshclass.com','20','2002-01-20');
```
###### Query OK, 1 row affected (0.01 sec)
* * *

### The SQL SELECT Statement

```syntax
SELECT * FROM studentslist;
```

| Id | Firstname | Lastname | Email                   | Age | dateofbirth |
|:--:|:----------|:--------:|:------------------------|:---:|:------------|
|  1 | Prasanna  | venkatsh | prasanna@freshclass.com |  21 | 2001-01-20  |
|  2 | Vimal  | raj | vimal@freshclass.com |  20 | 2002-01-20  |

###### 1 row in set (0.01 sec)
* * *

### The SQL WHERE Clause

```syntax
SELECT * FROM studentslist WHERE Id='1';
```

| Id | Firstname | Lastname | Email                   | Age | dateofbirth |
|:--:|:----------|:--------:|:------------------------|:---:|:------------|
|  1 | Prasanna  | venkatsh | prasanna@freshclass.com |  21 | 2001-01-20  |

###### 1 row in set (0.00 sec)
* * *

### The SQL ALTER TABLE Statement

```syntax
ALTER TABLE studentslist ADD Department varchar(70);
```
###### Query OK, 0 rows affected (0.04 sec)
###### Records: 0  Duplicates: 0  Warnings: 0
```syntax
SELECT * FROM studentslist;
```
| Id | Firstname | Lastname | Email                   | Age | dateofbirth | Department |
|:--:|:----------|:--------:|:------------------------|:---:|:------------|:-----------|
|  1 | Prasanna  | venkatsh | prasanna@freshclass.com |  21 | 2001-01-20  | NULL       |
|  2 | Vimal     | raj      | vimal@freshclass.com    |  20 | 2002-01-20  | NULL       |

###### 2 rows in set (0.00 sec)
* * *
