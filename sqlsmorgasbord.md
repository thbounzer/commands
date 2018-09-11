# SQL servers, queries, things, shit.
---

## mysql
---

* mysql server show users: `SELECT User FROM mysql.user;`
* show permissions for user: `SHOW GRANTS FOR 'user'@'host';`
* create user: `CREATE USER 'user'@'ipaddr' identified by 'passwd' password;`
* user permission: `GRANT (PRIVS) ON (DBASE).* TO 'user'@'ipaddr`;
* show databases: `SHOW DATABASES;`
* show tables: `SHOW TABLES`;
* engine stats: `SHOW ENGINE INNODB STATUS`;
* show stored procedure list: `SHOW PROCEDURE STATUS`;
* show stored procedure: `SHOW CREATE PROCEDURE procedurename;`

## postgres
---

* create database: `CREATE DATABASE name;';
* list databases: `\l`;
* list users: `\du`;
* list tables: `\dt`;
* use dbase: `\c database`;
* create user: `CREATE USER user WITH PASSWORD 'password'`;
* dump: `pg_dump dbname > outfile`
* restore: `psql dbname < infile`
* grant: `GRANT { { CREATE | CONNECT | TEMPORARY | TEMP } [,...] | ALL [ PRIVILEGES ] }
    ON DATABASE database_name [, ...]
    TO { [ GROUP ] role_name | PUBLIC } [, ...] [ WITH GRANT OPTION ]`;

* grant read only to a user on a database: 
    `GRANT CONNECT ON DATABASE mydb TO xxx;
    -- This assumes you're actually connected to mydb..
    GRANT USAGE ON SCHEMA public TO xxx;
    GRANT SELECT ON mytable TO xxx;`

## sqlite
---

* list tables: `.tables`
 
