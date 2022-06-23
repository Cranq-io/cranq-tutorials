# Delayer

[flow]

Forwards each signal received via `data` (input) after waiting as many milliseconds as received or specified by `delay`.

### Input ports:

* __data__: `any`

    Receives data to be forwarded.


* __delay__: `number`

    Receives / sets time to wait in milliseconds before forwarding the signal received via `data` (input).
    
    Can be both parameter or signal (For each input through `data`.)

### Output ports:

* __data__: `any`

    Data forwarded with a delay.

