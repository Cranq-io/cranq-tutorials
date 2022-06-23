# Opener-creator

[db/sqlite3]

Opens the specified SQLite database. When the database doesn't exist, creates it and runs the specified SQL script to create tables.

### Input ports:

* __params__: 
    ```
    {"dbId" :string, "filename" :string, "initSql" :string}
    ```

### Output ports:

* __done__: `null`


* __error__: `string`

