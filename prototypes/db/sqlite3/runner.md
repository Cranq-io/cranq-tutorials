---
description: [db/sqlite3]
---

# Runner

Runs a single SQL statement on the specified SQLite database, with the specified parameters.

Further on SQLite3 syntax:
https://www.sqlite.org/syntax.html

### Input ports:

* __params__: 
    ```
    {"db-id" :string, "sql" :string, optional "params" :(string or number)[]}
    ```

### Output ports:

* __done__: `string`


* __last ID__: `string`


* __changes__: `number`


* __error__: `string`

