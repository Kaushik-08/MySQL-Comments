# MySQL Comments

### The MySQL SHOW DATABASES Statement

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

### The MySQL CREATE DATABASE Statement
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

### The MySQL USE DATABASE Statement
```syntax
USE freshclass;
```
###### Database changed
* * *

### The MySQL CREATE TABLE Statement
```syntax
 CREATE TABLE studentslist(Id int primary key auto_increment, Firstname varchar(255) NOT NULL, Lastname varchar(255) NOT NULL,Email varchar(255) UNIQUE NOT NULL, Age int(2) NOT NULL, dateofbirth date NOT NULL);
```
###### Query OK, 0 rows affected, 1 warning (0.04 sec)
* * *

### The MySQL SHOW TABLES Statement
```syntax
SHOW TABLES;
```
| Tables_in_freshclass |
|:----|
| studentslist         |

###### 1 row in set (0.01 sec)
* * *
### The MySQL DESCRIBE TABLE Statement
```syntax
DESC studentslist;
```
```syntax
DESCRIBE studentslist;
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

### The MySQL INSERT INTO Statement

```syntax
INSERT INTO studentslist (Firstname,Lastname,Email,Age,dateofbirth) VALUES ('Prasanna','venkatsh','prasanna@freshclass.com','21','2001-01-20');
```

###### Query OK, 1 row affected (0.00 sec)

```syntax
INSERT INTO studentslist (Firstname,Lastname,Email,Age,dateofbirth) VALUES ('Vimal','raj','vimal@freshclass.com','20','2002-01-20');
```
###### Query OK, 1 row affected (0.01 sec)
* * *

### The MySQL SELECT Statement

```syntax
SELECT * FROM studentslist;
```

| Id | Firstname | Lastname | Email                   | Age | dateofbirth |
|:--:|:----------|:--------:|:------------------------|:---:|:------------|
|  1 | Prasanna  | venkatsh | prasanna@freshclass.com |  21 | 2001-01-20  |
|  2 | Vimal  | raj | vimal@freshclass.com |  20 | 2002-01-20  |

###### 1 row in set (0.01 sec)
* * *

### The MySQL WHERE Clause

```syntax
SELECT * FROM studentslist WHERE Id='1';
```

| Id | Firstname | Lastname | Email                   | Age | dateofbirth |
|:--:|:----------|:---------|:------------------------|:---:|:------------|
|  1 | Prasanna  | venkatsh | prasanna@freshclass.com |  21 | 2001-01-20  |

###### 1 row in set (0.00 sec)
* * *

### The MySQL ALTER TABLE Statement

```syntax
ALTER TABLE studentslist ADD Department varchar(70);
```
###### Query OK, 0 rows affected (0.04 sec)
###### Records: 0  Duplicates: 0  Warnings: 0

```syntax
ALTER TABLE studentslist MODIFY COLUMN Department char(100);
```
###### Query OK, 2 rows affected (0.06 sec)
###### Records: 2  Duplicates: 0  Warnings: 0

```syntax
DESC studentslist;
```

| Field       | Type         | Null | Key | Default | Extra          |
|:----|:----|:----:|:----:|:----:|:----|
| Id          | int          | NO   | PRI | NULL    | auto_increment |
| Firstname   | varchar(255) | NO   |     | NULL    |                |
| Lastname    | varchar(255) | NO   |     | NULL    |                |
| Email       | varchar(255) | NO   | UNI | NULL    |                |
| Age         | int          | NO   |     | NULL    |                |
| dateofbirth | date         | NO   |     | NULL    |                |
| Department  | char(100)    | YES  |     | NULL    |                |

###### 7 rows in set (0.01 sec)
```syntax
SELECT * FROM studentslist;
```
| Id | Firstname | Lastname | Email                   | Age | dateofbirth | Department |
|:--:|:----------|:---------|:------------------------|:---:|:------------|:-----------|
|  1 | Prasanna  | venkatsh | prasanna@freshclass.com |  21 | 2001-01-20  | NULL       |
|  2 | Vimal     | raj      | vimal@freshclass.com    |  20 | 2002-01-20  | NULL       |

###### 2 rows in set (0.00 sec)
* * *

### The MySQL UPDATE Statement

```syntax
 UPDATE studentslist SET Department = "Tech" WHERE Id = 1;
```
###### Query OK, 1 row affected (0.03 sec)
###### Rows matched: 1  Changed: 1  Warnings: 0
```syntax
SELECT * FROM studentslist;
```
| Id | Firstname | Lastname | Email                   | Age | dateofbirth | Department |
|:--:|:----------|:---------|:------------------------|:---:|:------------|:-----------|
|  1 | Prasanna  | venkatsh | prasanna@freshclass.com |  21 | 2001-01-20  | Tech       |
|  2 | Vimal     | raj      | vimal@freshclass.com    |  20 | 2002-01-20  | NULL       |

###### 2 rows in set (0.00 sec)
* * *

### The MySQL DELETE Statement

```syntax
DELETE FROM studentslist WHERE Id=1;
```
###### Query OK, 1 row affected (0.01 sec)
```syntax
SELECT * FROM studentslist;
```
| Id | Firstname | Lastname | Email                   | Age | dateofbirth | Department |
|:--:|:----------|:---------|:------------------------|:---:|:------------|:-----------|
|  2 | Vimal     | raj      | vimal@freshclass.com    |  20 | 2002-01-20  | NULL       |

###### 1 row in set (0.01 sec)
* * *

### The MySQL DROP TABLE Statement

```syntax
DROP TABLE studentslist;
```
###### Query OK, 0 rows affected (0.03 sec)
```syntax
SHOW TABLES;
```
###### Empty set (0.01 sec)
```syntax
DROP DATABASE freshclass;
```
###### Query OK, 0 rows affected (0.03 sec)
```syntax
SHOW DATABASES;
```
| Database           |
|:-------------------|
| information_schema |
| mysql              |
| performance_schema |
| sakila             |
| sys                |
| world              |


###### 6 rows in set (0.02 sec)
* * *

# MySQL Constraints

### NOT NULL

```syntax
 CREATE TABLE Constraints(Firstname varchar(255) NOT NULL);
```

### UNIQUE

```syntax
 CREATE TABLE Constraints(Email varchar(255) UNIQUE);
```

### DEFAULT

```syntax
CREATE TABLE Constraints(Department varchar(255) DEFAULT 'Tech');
```

### CHECK

```syntax
CREATE TABLE Constraints(Age int(2) NOT NULL, CHECK (Age>=21));
```

### PRIMARY KEY

```syntax
CREATE TABLE Constraints(Id int(3) PRIMARY KEY AUTO_INCREMENT);
```

### CREATE TABLE with all Constraints without FOREIGN KEY

```syntax
CREATE TABLE Constraints(Id int(3) PRIMARY KEY AUTO_INCREMENT, Firstname varchar(255) NOT NULL, Lastname varchar(255) NOT NULL, Email varchar(255) UNIQUE, Age int(2) NOT NULL, dateofbirth date NOT NULL, Department varchar(255) DEFAULT 'Tech', CHECK (Age>=21));
```
###### Query OK, 0 rows affected, 2 warnings (0.03 sec)
```syntax
DESC Constraints;
```
| Field       | Type         | Null | Key | Default | Extra          |
|:------------|:-------------|:-----|:---:|:-------:|:---------------|
| Id          | int          | NO   | PRI | NULL    | auto_increment |
| Firstname   | varchar(255) | NO   |     | NULL    |                |
| Lastname    | varchar(255) | NO   |     | NULL    |                |
| Email       | varchar(255) | YES  | UNI | NULL    |                |
| Age         | int          | NO   |     | NULL    |                |
| dateofbirth | date         | NO   |     | NULL    |                |
| Department  | varchar(255) | YES  |     | Tech    |                |

###### 7 rows in set (0.01 sec)

### FOREIGN KEY

```syntax
CREATE TABLE foreignkey(studId int PRIMARY KEY AUTO_INCREMENT, mark int(3), Id int, FOREIGN KEY(Id) REFERENCES constraints(Id));
```
###### Query OK, 0 rows affected, 1 warning (0.05 sec)

```syntax
DESC foreignkey;
```

| Field  | Type | Null | Key | Default | Extra |
|:-------|:-----|:-----|:---:|:--------|:------|
| studId | int  | NO   | PRI | NULL    |       |
| mark   | int  | YES  |     | NULL    |       |
| Id     | int  | YES  | MUL | NULL    |       |

###### 3 rows in set (0.00 sec)
*  *  *

# MySQL Operators

```syntax
SELECT * FROM studentslist;
```
| Id | Firstname | Lastname | Email                   | Age | dateofbirth | Department |
|:--:|:----------|:---------|:------------------------|:---:|:------------|:-----------|
|  1 | Prasanna  | venkatsh | prasanna@freshclass.com |  21 | 2001-01-20  | Tech       |
|  2 | Vimal     | raj      | vimal@freshclass.com    |  20 | 2002-01-20  | NULL       |

###### 2 rows in set (0.00 sec)
* * *

### AND

```syntax
SELECT * FROM studentslist WHERE Department = 'Design' AND Age = 20;
```
| Id | Firstname | Lastname | Email                | Age | dateofbirth | Department |
|:---|:----------|:---------|:---------------------|:----|:------------|:-----------|
|  2 | Vimal     | raj      | vimal@freshclass.com |  20 | 2002-01-20  | Design     |

###### 1 row in set (0.00 sec)
*  *  *

### OR

```syntax
SELECT * FROM studentslist WHERE Department = 'Design' AND Age = 20;
```
| Id | Firstname | Lastname | Email                | Age | dateofbirth | Department |
|:---|:----------|:---------|:---------------------|:----|:------------|:-----------|
|  2 | Vimal     | raj      | vimal@freshclass.com |  20 | 2002-01-20  | Design     |

###### 1 row in set (0.00 sec)
*  *  *

### NOT

```syntax
SELECT * FROM studentslist WHERE NOT Age = 21;
```
| Id | Firstname | Lastname | Email                | Age | dateofbirth | Department |
|:---|:----------|:---------|:---------------------|:----|:------------|:-----------|
|  2 | Vimal     | raj      | vimal@freshclass.com |  20 | 2002-01-20  | Design     |

###### 1 row in set (0.00 sec)
*  *  *

### BETWEEN

```syntax
SELECT * FROM studentslist WHERE Age BETWEEN 20 AND 22;
```
| Id | Firstname | Lastname | Email                   | Age | dateofbirth | Department |
|:---|:----------|:---------|:------------------------|:----|:------------|:-----------|
|  1 | Prasanna  | venkatsh | prasanna@freshclass.com |  21 | 2001-01-20  | Tech       |
|  2 | Vimal     | raj      | vimal@freshclass.com    |  20 | 2002-01-20  | Design     |

###### 2 rows in set (0.00 sec)
*  *  *

### IN

```syntax
SELECT * FROM studentslist WHERE Department IN ('Tech');
```
| Id | Firstname | Lastname | Email                   | Age | dateofbirth | Department |
|:---|:----------|:---------|:------------------------|:----|:------------|:-----------|
|  1 | Prasanna  | venkatsh | prasanna@freshclass.com |  21 | 2001-01-20  | Tech       |

###### 1 row in set (0.01 sec)
*  *  *

### LIKE

```syntax
SELECT * FROM studentslist WHERE Firstname LIKE 'Vi%';
```

| Id | Firstname | Lastname | Email                | Age | dateofbirth | Department |
|:---|:----------|:---------|:---------------------|:----|:------------|:-----------|
|  2 | Vimal     | raj      | vimal@freshclass.com |  20 | 2002-01-20  | Design     |

###### 1 row in set (0.00 sec)

```syntax
SELECT * FROM studentslist WHERE Firstname LIKE '%a';
```

| Id | Firstname | Lastname | Email                   | Age | dateofbirth | Department |
|:---|:----------|:---------|:------------------------|:----|:------------|:-----------|
|  1 | Prasanna  | venkatsh | prasanna@freshclass.com |  21 | 2001-01-20  | Tech       |

###### 1 row in set (0.00 sec)

*  *  *