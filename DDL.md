# MySQL Command Reference: Data Definition Language (DDL)

## Overview

The Data Definition Language (DDL) in MySQL is used to define and manipulate the structure of databases and tables. Here are the key commands along with their descriptions.

| **Command**                                                 | **Description**                                                                                               |
|-------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| `INT`                                                      | Integer value.                                                                                           |
| `FLOAT`                                                    | Floating-point number.                                                                                             |
| `DOUBLE`                                                   | Double-precision floating-point number.                                                                            |
| `DATE`                                                     | Date in the format "YYYY-MM-DD".                                                                                |
| `TIME`                                                     | Time in the format "HH:MM:SS".                                                                                |
| `DATETIME`                                                 | Timestamp with date and time.                                                                            |
| `CHAR(length)`                                             | Fixed-length character string.                                                                               |
| `VARCHAR(length)`                                          | Variable-length character string with a maximum length.                                                     |
| `BOOL`                                                     | Boolean value, TRUE or FALSE.                                                                                |
| `CREATE DATABASE database_name;`                          | Creates a new database.                                                                                 |
| `USE database_name;`                                      | Switches to the specified database.                                                                        |
| `DROP DATABASE database_name;`                            | Deletes a database permanently.                                                                             |
| `CREATE TABLE table_name ( );`                          | Creates a table.                                                                                        |
| `attribute1 datatype1, attribute2 datatype2,…, PRIMARY KEY(attribute1,…)` | Defines attributes and sets the primary key.                                      |
| `NOT NULL`                                                 | Disallows NULL values.                                                                                     |
| `AUTO_INCREMENT`                                           | Auto-incrementing sequential value.                                                                |
| `PRIMARY KEY`                                              | Defines the primary key.                                                                              |
| `RENAME TABLE old_table TO new_table;`               | Renames a table.                                                                                      |
| `DROP TABLE table_name;`                                | Deletes a table permanently.                                                                               |
| `ALTER TABLE table_name ADD attribute datatype;`        | Adds a new column to a table.                                                                   |
| `ALTER TABLE table_name DROP COLUMN attribute;`         | Removes an existing column from a table.                                                            |
| `ALTER TABLE table_name MODIFY attribute datatype;`     | Modifies the datatype of a column.                                                                           |
| `ALTER TABLE table_name ADD [CONSTRAINT name] FOREIGN KEY (foreign_key,…) REFERENCES table2(primary_key,…) [ON UPDATE CASCADE ON DELETE CASCADE];` | Establishes referential integrity with optional cascading. The `CONSTRAINT` name is optional; if omitted, MySQL assigns a name. |
| `ALTER TABLE table_name CHANGE old_column new_column datatype;` | Renames a column.                                                      |
| `INSERT INTO table_name VALUES (value1, value2,…),( …,…,…);` | Inserts complete records.                                                        |
| `INSERT INTO table_name (attribute1, attribute2,…) VALUES (value1, value2,…),( …,…,…);` | Inserts partial records; attribute list is specified before `VALUES`.               |
| `UPDATE table_name SET attribute1 = value1, attribute2 = value2,… WHERE condition;` | Updates specific columns of existing records based on conditions.         |
| `DELETE FROM table_name WHERE condition;`               | Deletes records based on specified conditions.                                                     |

## Tips for Usage

- **Clean Data Structure:** Plan your database structure in advance to minimize future changes.
- **Data Backup:** Create backups before making significant structural changes like `DROP` or `ALTER`.
- **Leverage Indexing:** Use primary keys and foreign keys to optimize relationships and performance.

With this reference, you have a useful foundation for defining and managing databases efficiently in MySQL.

