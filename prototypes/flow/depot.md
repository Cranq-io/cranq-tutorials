# Depot

[flow]

Forwards signal received through `data` when corresponding signal was received via `trigger`.

Example:
1. "A"@0 received via `data` (input)
2. Wait 1s
3. null@0 received via `trigger`
4. "A"@0 is sent through `data` (output)

### Input ports:

* __data__: _any_

    Receives data to be forwarded on trigger signal.



* __trigger__: _any_

    Receives a signal indicating that the corresponding `data` input signal may be forwarded.



### Output ports:

* __data__: _any_

    Sends signal as received through `data` (input).


