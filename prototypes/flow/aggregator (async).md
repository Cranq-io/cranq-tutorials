---
description: flow]
---

# Aggregator (async)

Aggregates inputs into an array until released.

The `release` signal is received and processed independently from those received via `data`. (As opposed to `flow/Aggregator`.)

The output reflects the order as received through `data`. 

Example:
1. "a"@0 is received via `data`
2. "b"@1 is received via `data`
3. null@2 is received via `release`
5. ["a", "b"]@2 is sent via `aggregated`

### Input ports:

* __data__: `any`

    Receives data items to be aggregated.


* __release__: `any`

    Receives signal to release aggregated inputs. Independent of `data`.

### Output ports:

* __aggregated__: `any[]`

    Sends the aggregated data.

