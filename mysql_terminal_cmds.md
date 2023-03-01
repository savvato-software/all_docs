# Some useful mysql terminal commands

Command:

$ mysql -u root

Output:

Welcome to the MySQL monitor.  Commands end with ; or \g.
Your MySQL connection id is 22
Server version: 8.0.31 Homebrew

Copyright (c) 2000, 2022, Oracle and/or its affiliates.

Oracle is a registered trademark of Oracle Corporation and/or its
affiliates. Other names may be trademarks of their respective
owners.

Type 'help;' or '\h' for help. Type '\c' to clear the current input statement.

mysql>

Command:

mysql> use tribeapp_db;

Output:

**Reading table information for completion of table and column names
You can turn off this feature to get a quicker startup with -A**

Database changed

Command:

mysql> show tables;

Output:

| Database           |
| -------------------|
| information_schema |
| mysql              |
| performance_schema |
| sys                |
| tribeapp_db        |
5 rows in set (0.02 sec)

Command:

mysql> show tables;

Output:

| Tables_in_tribeapp_db |
| ----------------------|
| adverb                |
| DATABASECHANGELOG     |
| DATABASECHANGELOGLOCK |
| noun                  |
| preposition           |
| user                  |
| user_role             |
| user_user_role_map    |
| verb                  |
9 rows in set (0.00 sec)

**Database must be dropped when the database migration scripts are
changed**

Command:

mysql> drop database tribe_db;

Output (sample, results may vary):

Query OK, 13 rows affected (0.15 sec)
