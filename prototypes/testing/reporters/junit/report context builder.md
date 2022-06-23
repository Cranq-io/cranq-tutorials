# Report context builder

[testing/reporters/junit]

### Input ports:

* __assertion ID__: `any`

    Receives individual fields for syncing.


* __assertion__: `any`

    Receives individual fields for syncing.


* __pre-report__: `any`

    Receives individual fields for syncing.

### Output ports:

* __context__: 
    ```
    {"assertion ID" :any, "assertion" :any, "pre-report" :any}
    ```

    The report context identifies an individual assertion by suite ID, case ID, and assertion ID.
    It also contains the preprocessed report and the assertion record.

