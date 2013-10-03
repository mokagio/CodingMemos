Postgresql Memos
================

##Database

####Create a new database

`CREATE DATABASE databasename;`

`CREATE DATABASE databasename OWNER ownername;`

[more info](http://www.postgresql.org/docs/8.1/static/manage-ag-createdb.html)

####Delete a database

`DROP DATABASE databasename;`

[more info](http://www.postgresql.org/docs/8.2/static/sql-dropdatabase.html)

####List all the databases on the server

`\l`

####Connect to a database

`\c databasename`

`\connect databasename`

##Roles and Users

####List all the roles

`\du`

####Create a role

`CREATE ROLE rolename;`

`CREATE ROLE rolename LOGIN;`

`CREATE ROLE rolename PASSWORD 'password';`

[more info](http://www.postgresql.org/docs/8.1/static/sql-createrole.html) and [even more](http://www.postgresql.org/docs/9.1/static/role-attributes.html)

####Delete a Role

`DROP ROLE rolename;`

[more info](http://www.postgresql.org/docs/8.3/static/sql-droprole.html)

####Alter a Role

`ALTER ROLE rolename WITH option;`

[more info](http://www.postgresql.org/docs/9.1/static/sql-alterrole.html)

##Tables

####List all the tables on the current database

`\dt`

####List all the columns of a table

`\d+ tablename`

##Queries

The usual SQL queries. And don'y forget the `;`!
