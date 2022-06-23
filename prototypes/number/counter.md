# Counter

[number]

Counts the received input signals.

Example:

1. true@0 is received via `trigger`
2. 1@0 is sent via `count`
3. false@1 is received via `trigger`
4. 2@1 is sent via `count`

### Input ports:

* __trigger__: `any`
    The input signals to be counted



### Output ports:

* __count__: `number`
    Total count of the signals received.



