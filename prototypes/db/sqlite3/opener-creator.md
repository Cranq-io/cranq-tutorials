# Opener-creator

[db/sqlite3]

Opens the specified SQLite database. When the database doesn't exist, creates it and runs the specified SQL script to create tables.

### Input ports:

* __params__: _{"dbId" :string, "filename" :string, "initSql" :string}_



### Output ports:

* __done__: _null_



* __error__: _string_



