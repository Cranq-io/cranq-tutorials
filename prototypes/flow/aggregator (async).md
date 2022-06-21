# Aggregator (async)

[flow]

Aggregates inputs into an array until released.

The `release` signal is received and processed independently from those received via `data`. (As opposed to `flow/Aggregator`.)

The output reflects the order as received through `data`. 

Example:
1. "a"@0 is received via `data`
2. "b"@1 is received via `data`
3. null@2 is received via `release`
5. ["a", "b"]@2 is sent via `aggregated`

### Input ports:

* __data__: _any_

    Receives data items to be aggregated.



* __release__: _any_

    Receives signal to release aggregated inputs. Independent of `data`.



### Output ports:

* __aggregated__: _any[]_

    Sends the aggregated data.



