---
description: [flow]
---

# Multiplexer

Forwards data received via dynamic inputs to `multiplexed`, wrapped in a record which carries both the data and the ID of the port (field) that it was received through.

Example:
1. `fields` is set to ["a", "b"]
2. Input ports `a` and `b` get created
3. The number 5 received via `b`
4. {"field": "b", "data": 5} will be sent via `multiplexed`.

### Input ports:

* __fields__: `(string[] or number[])`

    Receives a list of input port names to accept data payload through.


* __demultiplexed__: `any`

    Receives data payload for multiplexing.

### Output ports:

* __multiplexed__: `{"field" :string, "data" :any}`

    Sends multiplexed data.

