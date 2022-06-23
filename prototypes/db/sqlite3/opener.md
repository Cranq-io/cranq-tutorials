---
description: db/sqlite3]
---

# Opener

Opens the specified SQLite database.
Mode is normally 6.
(More on modes: https://www.sqlite.org/c3ref/c_open_autoproxy.html)

### Input ports:

* __params__: 
    ```
    {"dbId" :string, "filename" :string, "mode" :number}
    ```

### Output ports:

* __done__: `null`


* __error__: `string`

