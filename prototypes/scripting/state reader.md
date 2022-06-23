# State reader

[scripting]

Reads the contents of "state.json", or, when absent, forwards the received `state`. The initial state is required to contain the current working directory (cwd) on the specified path.

### Input ports:

* __state__: `any`

    Receives initial script state.


* __config__: `{"working-folder" :string}`


* __params__: `{"cwd-path" :(string or number)[]}`

### Output ports:

* __state__: `any`

    Receives script state read from path.

