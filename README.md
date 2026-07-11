# Anton

Anton is a lightweight SQL-like database written in Java. It is developed as a learning project to understand the internal mechanisms of database management systems, including query parsing, execution, and storage management.

## Features

The current implementation supports the following operations:

*   **Data Definition Language (DDL):**
    *   `CREATE TABLE`: Define tables with schemas including column names and data types.
    *   `DROP TABLE`: Remove existing tables and their associated data.
*   **Data Manipulation Language (DML):**
    *   `INSERT INTO`: Insert new records into tables.
    *   `SELECT`: Retrieve records. Supports selecting specific columns or all columns (`*`), and basic conditional filtering using the `WHERE` clause.
    *   `DELETE`: Remove records based on conditional filters using the `WHERE` clause.
*   **Query Processing:** Includes a custom parser and execution engine for a subset of SQL.
*   **Indexing:** Utilizes B+ Trees for efficient data retrieval and record lookups.
*   **Storage Management:** Handles basic file I/O, page management, and record serialization.

## Planned Features

*   Advanced filtering mechanisms
*   Query result caching
*   `UPDATE` statements with conditional filtering
*   Basic transaction support (commit and rollback)
*   Table joins

## Example Usage

Start the database engine and interact with it using standard SQL-like syntax:

```sql
CREATE TABLE users ('id' INT, 'name' STRING)
INSERT INTO users VALUES ('id' 1, 'name' 'Alice')
SELECT * FROM users
SELECT id, name FROM users WHERE id=1
DELETE FROM users WHERE id=1
DROP TABLE users
```

## Disclaimer

This project is built for educational purposes and is not intended for production environments.

## License

This project is licensed under the [MIT License](./LICENSE).
