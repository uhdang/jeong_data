# How to Postgresql

```
$ pg_ctl -D /usr/local/var/postgres start       # Start postgresql server
$ pg_ctl -D /usr/local/var/postgres stop        # Stop the server

$ psql -l                                       # list databases
```

## Help
```
$ psql --help
```

## Connect to the database
```
$ psql -d [DATABASE] -u [USERNAME]

i.e.
$ psql -d postgres
```

## Access inside Databse from terminal (outside the shell)
```
$ psql [DATABASE] -c [POSTGRESQL COMMAND]

i.e.
$ psql postgres -c "\du"
```



## Inside the Database
```
$ \c [database_name]        # connect to a specific database
$ \du                       # list all postgresql user 
$ \l                        # list all databases in the PostgreSQL database server
$ \dn                       # list all schemas
$ \df                       # list all stored procedures and functions 
$ \dv                       # list all views
$ \dt                       # list all tables
$ \q                        # quit psql

```

## Ref
http://www.postgresqltutorial.com/postgresql-cheat-sheet/


# Using SQL Editors
## pyAdmin
ref: http://www.postgresqltutorial.com/connect-to-postgresql-database/

## VSCode
- You can add a PostgreSQL connection in the explorer or via the command palette command "PostgreSQL: Add Connection"
