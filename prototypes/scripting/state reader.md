# State reader

[scripting]

Reads the contents of "state.json", or, when absent, forwards the received `state`. The initial state is required to contain the current working directory (cwd) on the specified path.

### Input ports:

* __state__: _any_

    Receives initial script state.



* __config__: _{"working-folder" :string}_



* __params__: _{"cwd-path" :(string or number)[]}_



### Output ports:

* __state__: _any_

    Receives script state read from path.



