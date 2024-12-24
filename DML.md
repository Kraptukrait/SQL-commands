# MySQL Command Reference: Data Manipulation Language (DML)

## Overview

The Data Manipulation Language (DML) in MySQL is used to query, insert, update, and delete data within the database. Here are the key commands along with their descriptions.

| **Command**                                                                                     | **Description**                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `SELECT attribute1 AS alias, attribute2, … FROM table WHERE condition ORDER BY attribute [ASC][DESC],…` | Queries a table, selecting specified attributes. Conditions can be combined with `AND`, `OR`, or `NOT`. Sorting is controlled with `ORDER BY` in ascending (ASC) or descending (DESC) order. Sorting by multiple attributes is possible. |
| `… WHERE attribute LIKE pattern`                                                               | Comparison: the attribute is compared to a pattern, using `%` or `_` as wildcards.                                                                                                             |
| `… WHERE attribute BETWEEN start AND end`                                                      | The attribute value is between `start` and `end` inclusively.                                                                                                                                 |
| `… WHERE attribute IN (value1, value2, …)`                                                    | The attribute value is within the set `value1`, `value2`, etc.                                                                                                                                |
| `MAX(attribute)`                                                                              | Aggregates the maximum value of the column.                                                                                                                                                    |
| `MIN(attribute)`                                                                              | Aggregates the minimum value of the column.                                                                                                                                                    |
| `SUM(attribute)`                                                                              | Aggregates the sum of all column values.                                                                                                                                                       |
| `COUNT(*)`                                                                                   | Counts all rows, including `NULL` values.                                                                                                                                                      |
| `COUNT(attribute)`                                                                            | Counts all non-`NULL` values in the specified column.                                                                                                                                          |
| `AVG(attribute)`                                                                              | Aggregates the average value of the column.                                                                                                                                                    |
| `DISTINCT …`                                                                                  | Outputs all unique records, suppressing duplicates.                                                                                                                                           |
| `SELECT attribute1, SUM(attribute2) FROM table WHERE … GROUP BY attribute1 HAVING SUM(attribute2) > threshold ORDER BY …;` | Aggregation with grouping: sums values of `attribute2`, groups by `attribute1`, and restricts groups with `HAVING`.                                                                   |
| `SELECT t1.attribute1, t2.attribute2, … FROM table1 t1 JOIN table2 t2 ON t1.fk1 = t2.pk1;`     | Inner Join: includes all records from `table1` that have matching entries in `table2`. A self-join can be performed by joining a table with itself.                                           |
| `SELECT ht.attribute1, nt.attribute2, … FROM main_table ht LEFT JOIN secondary_table nt ON join_condition;` | Left Join: includes all records from the left table `ht`, adding unmatched rows from the right table `nt` as `NULL`. A right join is the reverse. |
| `SELECT attribute1, attribute2 FROM table WHERE attribute >= (SELECT * FROM … )`              | Conditions can be `=`, `<>`, `>`, `<`, `>=`, `<=`; `[IN]` checks if an attribute is in a subquery, `[EXISTS]` checks if a comparison value from the subquery is in the main query, `[ANY]` checks any value, `[ALL]` checks all values. |
| `CREATE VIEW view_name AS SELECT … ;`                                                         | Creates a view.                                                                                                                                                                               |
| `SHOW CREATE VIEW view_name;`                                                                 | Displays the syntax of a view.                                                                                                                                                                |
| `DROP VIEW view_name;`                                                                        | Deletes a view.                                                                                                                                                                               |

## Tips for Usage

- **Filtering Data:** Use the `WHERE` clause effectively to limit results to only relevant data.
- **Aggregation Functions:** Combine functions like `SUM`, `AVG`, and `COUNT` with `GROUP BY` for powerful analysis.
- **Joins:** Use joins to relate data across multiple tables for comprehensive queries.
- **Performance Optimization:** Optimize queries with indexing and avoid unnecessary subqueries.

