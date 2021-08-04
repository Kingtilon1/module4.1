# module4.1
My sql database was a  table that stored the id, username, password and email of the user. 
The operating system being used is Ubuntu.
//create the sql server 
 sudo mysql -u root -p
 
 //all sql statements ends with a ; or \g
 
 //create a database, the file name linuxhint can be replaced by a name of your choice
 
 create database linuxhint;
 
 //command to access the database
 
 use linuxhint;
 
 //command to create the table, *CREATE TABLE TableName(Col1 Datatype, Col2 Datatype, ….);
 
CREATE TABLE  user(id int(11) ,username varchar(25),passwd varchar(25),email varchar(40));

//Now that a table is created you can insert values *

mysql> INSERT INTO user VALUES (2100, 'Kingty', 'theone8080', 'theone@ gmail.com');

//to view you table so far you type the command  SELECT * FROM user; and this is the output

+------+----------+------------+------------------+

| id   | username | passwd     | email            |

+------+----------+------------+------------------+

| 2100 | Kingty   | theone8080 | theone@gmail.com |

+------+----------+------------+------------------+

//To insert a value

 INSERT INTO user VALUES(1001, 'princebobb', 'passwd25', 'thetwo@yahoo.com');
 
 //output after using the same *SELECT * FROM user
 
+------+------------+------------+------------------+

| id   | username   | passwd     | email            |

+------+------------+------------+------------------+

| 1001 | princebobb | passwd25   | thetwo@yahoo.com |

| 2100 | Kingty     | theone8080 | theone@gmail.com |

+------+------------+------------+------------------+ 

// command to update a record in your table

 UPDATE user SET username='princessty', passwd='7474' WHERE id=1001;
 
 //new output 
 
 +------+------------+------------+------------------+
 
| id   | username   | passwd     | email            |

+------+------------+------------+------------------+

| 1001 | princessty | 7474       | thetwo@yahoo.com |

| 2100 | Kingty     | theone8080 | theone@gmail.com |

+------+------------+------------+------------------+

//command to alter your table

ALTER TABLE user DROP COLUMN email;

//new output

+------+----------+------------+

| id   | username | passwd     |

+------+----------+------------+

| 2100 | Kingty   | theone8080 |

+------+----------+------------+

//command to drop a table, This erases the table

DROP TABLE user;

//now the table is gone

