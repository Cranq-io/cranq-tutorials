# Sqlite3

[db/sqlite3]

Generic SQLite 3 integration node.
This is an internal node. Use specific SQLite nodes instead.

### Input ports:

* __action__: 
    ```
    {"id" :string, "type" :("open" or "run" or "get" or "all" or "each" or "close"), "options" :{"sql" :string, optional "options" :{string: any}}}
    ```



### Output ports:

* __data__: `any`


* __done__: `null`


* __error__: `string`


