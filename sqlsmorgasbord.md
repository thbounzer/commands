#SQL servers, queries, things, shit.
---

##mysql
---

* mysql server show users: `SELECT User FROM mysql.user;`
* show permissions for user: `SHOW GRANTS FOR 'user'@'host';`
* create user: `CREATE USER 'user'@'ipaddr' identified by 'passwd' password;`
* user permission: `GRANT (PRIVS) ON (DBASE).* TO 'user'@'ipaddr`;

##postgres
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

##sqlite
---

* list tables: `.tables`
 
