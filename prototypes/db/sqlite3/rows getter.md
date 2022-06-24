---
description: [db/sqlite3]
---

# Rows getter

Retrieves multiple rows as a single array from the specified database.

### Input ports:

* __params__: 
    ```
    {"dbId" :string, "sql" :string, optional "params" :(string or number)[]}
    ```

### Output ports:

* __data__: ` {string: any}[] `


* __done__: ` null `


* __error__: ` string `

