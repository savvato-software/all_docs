
<p align="center">
    Getting started 
</p>

<p align="center">
    How to run tribe-app locally on your computer (mac)
</p>

## Install the following on your computer locally:

1. MySQL server and client (v8.0.30, or higher)
2. NodeJS along with npm (most recent)
3. Java 19
4. Maven (most recent)

5. Chrome or Firefox web browser
6. IntelliJ

It will help for you to install version managers for Java and NodeJS. Recommended are SDKMAN for Java, and Node Version Manager (nvm) for Node.

## The Code:

You will use github.com to share code with the rest of the team. You will need to fork the following repos, and clone your forks to your computer locally:

1. https://github.com/savvato-software/tribe-app-backend
2. https://github.com/savvato-software/tribe-app-frontend
3. https://github.com/savvato-software/savvato-javascript-services

Remember to FORK the above repos, otherwise you won't be able to submit your code changes. When you do your FORK, you will have the option to clone ONLY the **develop** branch. Clear this checkbox! You need to clone all of the branches!

## Setting up the database:

Now we need to log into the database. If you have not set mysql to run automatically, you will need to start it. See this article on starting up MySQL Server: https://www.mysqltutorial.org/mysql-adminsitration/start-mysql/.

Once the server is running, type:

    sudo mysql -u root

to log in. You should get the following response from the terminal:

```
    Welcome to the MySQL monitor. Commands end with ; or \g.
    Your MySQL connection id is 8
    Server version: 8.0.30 Homebrew
    Copyright (c) 2000, 2022, Oracle and/or its affiliates.
    Oracle is a registered trademark of Oracle Corporation and/or its affiliates. Other names may be trademarks of their respective owners.
    Type 'help;' or '\h' for help. Type '\c' to clear the current input statement.    
```
            
At the mysql prompt, type:

    show databases

You should get the following response from the terminal:

```
    +--------------------+
    | Database |
    +--------------------+
    | information_schema |
    | mysql |
    | performance_schema |
    | sys |
    +--------------------+
    4 rows in set (0.04 sec)
```
                            
If you see tribeapp_db listed above, it means you have run these instructions before. No worries, it is okay, we will be dropping any existing database.

Type:
        
    DROP DATABASE tribeapp_db;

    CREATE DATABASE tribeapp_db;

    CREATE USER 'tribeapp_db_user'@'localhost' IDENTIFIED BY 'supersecure';

    GRANT ALL PRIVILEGES on tribeapp_db.* TO 'tribeapp_db_user'@'localhost';

## Running the backend

Look in the `#getting-started` channel in Slack, and there is a file `application.properties`. You need to copy this file, and place it in your backend repo directory at `./src/main/resources/application.properties`.

Then, open a new terminal window and navigate to the tribe-app-backend folder and type:

    mvn spring-boot:run


## Running the frontend

Open a new terminal window and navigate to the tribe-app-frontend folder and type:

    cp src/app/_environments/environment.dev.ts  src/app/_environments/environment.ts 
    npm i -g @ionic/cli

This command will launch the front end
    
    ionic serve
    
    
----
If you run into any issues, please reach out in Slack! Also feel free to propose any improvement to this documentation. Thanks!
