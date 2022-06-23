---
description: [flow]
---

# Syncer

Bundles input signals that have the same tag. All inputs must receive exactly one signal for a given tag (or be a parameter) for the bundle (record or tuple, depending on the type of `fields`) to be sent.

Example A (record):
1. `fields` is set to ["a", "b"]
2. Inputs ports `a` and `b` get created
3. `a` receives "Foo"@0
4. `b` receives "Bar"@0
5. `synced` sends {"a": "Foo", "b": "Bar"}@0

Example B (tuple):
1. `fields` is set to [0, 1]
2. Inputs ports `0` and `1` get created
3. `0` receives "Foo"@0
4. `1` receives "Bar"@0
5. `synced` sends ["Foo", "Bar"]@0

More: https://github.com/Cranq-io/cranq-tutorials/blob/main/reference/1_application_flow/1_3_synchronization/README.md#example---synchronizing-node-inputs

### Input ports:

* __fields__: `(string[] or number[])`

    Sets a list of inupt port names matching property names in the data sent via `synced`.
    
    Must be parameter.
    
    Example values:
    * ["a", "b"] will result in record output
    * [0, 1] will result in a tuple output


* __unsynced__: `any`

    Receives individual item for syncing.

### Output ports:

* __synced__: `({string: any} or any[])`

    Sends synchronized inputs as a record or tuple indexed by the names of the ports they were received through.
    
    Example:
    {"a": "Foo", "b": "Bar"}

