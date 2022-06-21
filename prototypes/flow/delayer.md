# Delayer

[flow]

Forwards each signal received via `data` (input) after waiting as many milliseconds as received or specified by `delay`.

### Input ports:

* __data__: _any_

    Receives data to be forwarded.



* __delay__: _number_

    Receives / sets time to wait in milliseconds before forwarding the signal received via `data` (input).
    
    Can be both parameter or signal (For each input through `data`.)



### Output ports:

* __data__: _any_

    Data forwarded with a delay.



