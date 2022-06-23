# Demultiplexer

[flow]

Forwards the data property of the received multiplexed signal to the output port matching the corresponding port ID (field).

Example:
1. `fields` is set to ["a", "b"]
2. Output ports `a` and `b` get created
3. {"field": "b", "data": 5} received via `multiplexed`
4. The number 5 will be sent via `b`.

### Input ports:

* __fields__: `(string[] or number[])`

    Receives a list of output port names to send multiplexed data payload to.
    
    Must be parameter.


* __multiplexed__: `{"field" :string, "data" :any}`

    Receives multiplexed data.

### Output ports:

* __demultiplexed__: `{"field" :string, "data" :any}["data"]`

    Sends demultiplexed payload data.

