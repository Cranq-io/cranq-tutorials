---
description: flow]
---

# Forked aggregator (async)

Aggregates data received via `data` into two output arrays, depending on whether a corresponding arbitrary input is received via `true` or `false`.

Releases both output arrays on receiving a signal on `release`.

The input `release` is independent from `data`, `true`, and `false`.

Example:
1. "foo"@0 is received via `data`
2. "bar"@1 is received via `data`
3. "baz"@2 is received via `data`
4. null@0 is received via `false`
5. null@1 is received via `true`
6. null@2 is received via `false`
7. null@3 is received via `release`
8. ["foo", "baz"]@3 is sent via `falses`, and ["bar"]@3 is sent via `trues`

### Input ports:

* __release__: `any`

    Receives signal to release aggregated inputs. Independent of `data`.


* __data__: `any`

    Receives the data to be forwarded to either output.


* __true__: `any`

    Receives signal that corresponding `data` should be aggregated into `trues`.


* __false__: `any`

    Receives signal that corresponding `data` should be aggregated into `falses`.

### Output ports:

* __trues__: `any[]`

    Sends the aggregated data, that was accompanied by signals via `true`.


* __falses__: `any[]`

    Sends the aggregated data, that was accompanied by signals via `false`.

