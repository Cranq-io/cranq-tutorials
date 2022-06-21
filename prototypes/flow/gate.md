# Gate

[flow]

Forwards signal received via `data` when corresponding signal received via `open` is true.

Example A:
1. "A"@0 received via `data`
2. false@0 received via `open`
3. No signal is sent via `data` (output)

Example B:
1. true@0 received via `open`
2. "B"@0  received via `data`
3. "B"@0 is sent via `data` (output)

### Input ports:

* __data__: _any_

    Receives the signal to be forwarded / filtered.



* __open__: _boolean_

    Whether to forward the signal received via `data`.



### Output ports:

* __data__: _any_

    Forwarded / filtered signal



