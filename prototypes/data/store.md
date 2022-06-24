---
description: [data]
---

# Store

Stores data and sends it via `data` when read. When the store is empty, any attempt to read the contents will result in a signal sent out via `not found`.

Example:
1. `data` set to "hello"
2. null@1 received via `read`
3. "hello"@1 sent via `data` (output)

### Input ports:

* __data__: ` any `

    Receives contents of the store. San be set as parameter, or received as signal.


* __read__: ` any `

    Receives a signal that triggers the contents being sent via `data` (output), or `not found` when has no content.

### Output ports:

* __data__: ` any `

    Sends store contents.


* __written__: ` null `

    Sends signal when contents were set in flow.


* __not found__: ` null `

    Sends signal on read attempt while store has no content.

