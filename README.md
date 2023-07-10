# E-commerce Backend

![License Badge](https://shields.io/badge/license-MIT-green)

## Description

This E-commerce backend is built using express.js, Sequelize ORM, and MySQL and enables an owner of an internet retail company to store product information in a database, along with information like product tags and categories. The API enables the creation, updating, and deletion of products, categories, and tags, and can be extended to include other business objects.

## Table of Contents

- [Description](#description)
- [Installation](#installation)
- [Usage](#usage)
- [Contributing](#contributing)
- [Tests](#tests)
- [License](#license)
- [Questions](#questions)

## Installation

The prerequisite to using this app is to install Nodejs and MySql on your machine and setting environment variables with your DB creds in a .env file in the root of the directory, like so:

```
DB_PW=XXX
DB_USER=root
DB_NAME=ecommerce_db
```

To install and use this app, clone this repo and navigate to the root directory. Run `npm i` to install the necessary libraries used to run this app e.g. express, mysql, sequelize, etc. These libraries are specified in the package.json.

## Usage

To run this app, navigate to the project root.

You must login to MySql first to create the initial DB Schemas (defined in schema.sql) by running this

```
$ mysql -u root -p
Enter password: *********
Welcome to the MySQL monitor.  Commands end with ; or \g.
Your MySQL connection id is 17
Server version: 8.0.33 MySQL Community Server - GPL

Copyright (c) 2000, 2023, Oracle and/or its affiliates.

Oracle is a registered trademark of Oracle Corporation and/or its
affiliates. Other names may be trademarks of their respective
owners.

Type 'help;' or '\h' for help. Type '\c' to clear the current input statement.

mysql> source db/schema.sql
Query OK, 4 rows affected (0.09 sec)

Query OK, 1 row affected (0.00 sec)

mysql> show databases;
+--------------------+
| Database           |
+--------------------+
| books_db           |
| ecommerce_db       |
| employees          |
| information_schema |
| inventory_db       |
| mysql              |
| performance_schema |
| sys                |
+--------------------+
8 rows in set (0.02 sec)

mysql> exit
```

Next, to pre-populate the database with some seed data, you must run `npm run seed` which will load the database and get it working with example data.

After the db is populated, run the command `npm run start`. If you are actively developing, you can alternatively run `npm run watch` so that every time you save the file you don't need to restart the server (thanks to nodemon)

To see a walkthrough video of this, please view this Google Drive link: https://drive.google.com/file/d/1AQCmDLYoUTI_YGx71PTDew77HzDbdTxb/view?usp=sharing

## Contributing

To contribute, please clone or fork this repo and make a pull request for my review.

## Tests

There are currently no unit tests yet for this application.

## License

This application uses the MIT license. Please see
https://mit-license.org/ for more information on this license.

## Questions

You can find me [HERE](https://github.com/mslzbry) on Github.
Feel free to email me at m.slzbry@gmail.com if you have any additional questions.
