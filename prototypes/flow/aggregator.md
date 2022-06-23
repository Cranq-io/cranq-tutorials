# Aggregator

[flow]

Aggregates inputs into an array until released.

A `release` signal must accompany each `data` signal, bearing the same tag.

The output reflects the order as received through `data`. Matching `release` signals may come in any order as long as each pairs up with a `data` signal.

Example:
1. true@1 is received via `release`
2. false@0 is received via `release`
3. "a"@0 is received via `data`
4. "b"@1 is received via `data`
5. ["a", "b"]@1 is sent via `aggregated`

### Input ports:

* __data__: `any`
    Receives data items to be aggregated.



* __release__: `boolean`
    Receives flag whether to release aggregated inputs. Must be provided for each `data` input signal.



### Output ports:

* __aggregated__: `any[]`
    Sends the aggregated data.



