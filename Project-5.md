## **Documentation for Project 5**

### Installing MySQL Server 
`sudo apt install mysql-server -y`
![MySQL-Server-Installed](./Images/My-SQL-Server-Installation.png)

### Enabling MySQL Server 
`sudo systemctl enable mysql`
![MySQL-Server-Enabled](./Images/Enabling-MySQL.png)

### Installing MySQL Client 
`sudo apt install mysql-client -y`
![MySQL-Server-Installed](./Images/MySQL-Client-Installation.png)

### Creating DB User and Database
`CREATE USER 'remote_user' @ '%';`

`CREATE DATABASE 'test_db';`

![Remote-user-and-database-creation](./Images/Creating-DB-and-USER.png)

### Granting and Flushing Privileges 
`GRANT ALL ON test_db.* TO 'remote_user'@'%' WITH GRANT OPTION;`

`FLUSH PRIVILEGES;`

![Granting-and-Flushing-Privileges](./Images/Granting-and-Flushing-Privileges.png)


### Binding IP Address
`sudo vi /etc/mysql/mysql.conf.d/mysqld.cnf`
![Bounded-IP-Address](./Images/IPAddress-Bounded.png)


### Connecting to Mysql server from Mysql Client
`sudo mysql -u remote_user -h 44.201.199.27`

![Connection-to-mysql server](./Images/Successful-Connection-to-Server.png)


### Showing databases Created on Server
`Show Databases;`

![Displaying-Databases-on-server-From-Client](./Images/Databases-on-Server.png)


### Displaying List of Users from Server
`select user,host from mysql.user;`

![Displaying-Users-From-Server](./Images/Users-list-populated-from-server.png)