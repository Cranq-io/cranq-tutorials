# Store (async)

[data]

Stores data and sends it via `data` when read. When the store is empty, read attempts will be buffered until the store gets initialized via `data`.

Example: late initialization
1. null@1 received via `read`
2. null@2 received via `read`
3. "hello"@3 received via `data`
4. "hello"@1 sent via `data` (output)
5. "hello"@2 sent via `data` (output)

### Input ports:

* __data__: `any`

    Receives contents of the store. San be set as parameter, or received as signal. When received as a signal, will complete previous read attempts.


* __read__: `any`

    Receives a signal that triggers the contents being sent via `data` (output). When store has no content yet, read signals will be buffered until a signal is received via `data`.

### Output ports:

* __data__: `any`

    Sends store contents.


* __written__: `null`

    Sends signal when contents were set in flow.


* __not found__: `null`

    Sends signal on read attempt while store has no content.

