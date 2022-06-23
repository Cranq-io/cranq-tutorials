---
description: flow]
---

# Queued forwarder

Forwards data received via `data` in the order defined by the tags of the signals received via `reference`.

Queues `reference` inputs until the first N signals have all received matching inputs via `data` then releases them one-by-one via `data` (output).

Used to signal sequence after asynchronous transformations.

Example:
1. "A"@0 received via `reference`
2. "B"@1 received via `reference`
3. "b"@1 received via 

### Input ports:

* __data__: `any`

    Receives data to be forwarded.


* __reference__: `any`

    Receives signals that define the order of the forwarded signals, based on their tags.

### Output ports:

* __data__: `any`

    Sends forwarded data.

