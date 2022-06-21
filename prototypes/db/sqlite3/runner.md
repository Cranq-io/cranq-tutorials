# Runner

[db/sqlite3]

Runs a single SQL statement on the specified SQLite database, with the specified parameters.

Further on SQLite3 syntax:
https://www.sqlite.org/syntax.html

### Input ports:

* __params__: _{"db-id" :string, "sql" :string, optional "params" :(string or number)[]}_



### Output ports:

* __done__: _string_



* __last ID__: _string_



* __changes__: _number_



* __error__: _string_



