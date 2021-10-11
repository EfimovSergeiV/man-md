https://dev.mysql.com/downloads/

# CREATE DATABASE

mysql -u root -p
create database dbase_name;

SHOW DATABASES;

create user 'db_user'@'localhost' identified by 'pass';
GRANT ALL PRIVILEGES ON dbase_name. * to 'db_user'@'localhost';


mysql -u db_user -p
source backup/dbase_name.sql


# REMOVE DATABASE

DROP DATABASE productsdb;