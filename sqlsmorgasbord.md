#SQL servers, queries, things, shit.
---

* mysql server show users: 'SELECT User FROM mysql.user;'
* show permissions for user: 'SHOW GRANTS FOR 'user'@'host';'
* create user: 'CREATE USER 'user'@'ipaddr' identified by 'passwd' password;'
* user permission: 'GRANT (PRIVS) ON (DBASE).* TO 'user'@'ipaddr';

* *postgres* create database: 'CREATE DATABASE name;';
* *postgres* list databases: '\l';
* *postgres* list users: '\du';
* *postgres* list tables: '\dt';
* *postgres* use dbase: '\c database';
* *postgres* create user: 'CREATE USER user WITH PASSWORD 'password'';
