# Splitter

[flow]

Splits data received via `unsplit` by fields / indexes.

Do not use splitters to access optional record fields. Opt for a `data/dictionary/Item getter` in those cases instead.

Example A (record input):
1.`fields` is set to ["a", "b"]
2. Output ports `a` and `b` get created.
3. {"a": "foo", "b": "bar"}@0 received by `unsplit`
4. "foo"@0 is sent via `a`
5. "bar"@0 is sent via `b`

Example B (tuple input):
1.`fields` is set to [0, 1]
2. Output ports `0` and `1` get created.
3. ["foo", "bar"]@0 received by `unsplit`
4. "foo"@0 is sent via `0`
5. "bar"@0 is sent via `1`

More: https://github.com/Cranq-io/cranq-tutorials/blob/main/reference/1_application_flow/1_3_synchronization/README.md#example---synchronizing-node-inputs.

### Input ports:

* __fields__: `(string[] or number[])`

    Sets a list of output port names matching property names in the data received via `unsplit`.
    
    Must be parameter.
    
    Example:
    ["a", "b"]


* __unsplit__: `({string: any} or any[])`

    Receives records or tuples to be split into individual items.
    
    Examples:
    * {"a": 5, "b": 2}
    * [5, 2]

### Output ports:

* __split__: 
    ```
    (({string: any} or any[])[string] or ({string: any} or any[])[number])
    ```

    Sends input data split into individual fields.

