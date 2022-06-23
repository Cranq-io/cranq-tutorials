# Command runner

[scripting/actions]

Runs an OS command.

### Input ports:

* __state__: `any`

    Receives script state.


* __params__: 
    ```
    {"cwd" :(string or number)[], "result-path" :string, "message" :string, "command" :string}
    ```

### Output ports:

* __state__: `any`

    Sends updated script state.

