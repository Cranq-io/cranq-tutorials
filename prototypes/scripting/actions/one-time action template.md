# One-time action template

[scripting/actions]

Template for creating actions that run only once during the execution of the script and record their result into the state. Once a result is recorded, the action will be skipped on the next run.

### Input ports:

* __state__: _any_

    Receives script state.



* __params__: _{"cwd" :string, "result-path" :string, "message" :string}_



### Output ports:

* __state__: _any_

    Sends updated script state.



