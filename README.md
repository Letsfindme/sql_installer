# sql_installer
Mysql installation guide for linux Ubuntu 18

# Introduction
MySQL is an open-source database management system.



# Step 1 — verification:
  to verify if it's already instaled
  
  $ mysql v--    
  
  
# Step 2 — Installing MySQL
update the package index with apt:

$ sudo apt update

Then install the default package:

$ sudo apt install mysql-server


# Step 3 — Configuring MySQL
This changes some of the less secure default options for things like remote root logins and sample users.
$ sudo mysql_secure_installation
you can press Y and then ENTER to accept the defaults for all the subsequent questions.
This will remove some anonymous users and the test database, disable remote root logins.

# Step 4 — Testing MySQL
service mysql status
or
systemctl status mysql.service

You'll see output similar to the following:

Output
● mysql.service - MySQL Community Server
   Loaded: loaded (/lib/systemd/system/mysql.service; enabled; vendor preset: en
   Active: active (running) since Wed 2018-04-23 21:21:25 UTC; 30min ago
 Main PID: 3754 (mysqld)
    Tasks: 28
   Memory: 142.3M
      CPU: 1.994s
   CGroup: /system.slice/mysql.service
           └─3754 /usr/sbin/mysqld
