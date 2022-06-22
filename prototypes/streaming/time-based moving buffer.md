# Time-based moving buffer

[streaming]

Stores the "value" property of samples received in the last `length` seconds and sends them via `buffer`.

Errors on invalid `size`.

Expects samples to be received in ascending order of "timestamp".

Data sent via `buffer` is immutable.

Example:
1. `size` set to 2 (seconds)
2. {value: "A", timestamp: 0}@0 received via `sample`
3. [{value: "A", timestamp: 0}]@0 sent via `buffer`
4. {value: "B", timestamp: 1}@1 received via `sample`
5. [{value: "A", timestamp: 0}, {value: "B", timestamp: 1}]@1 sent via `buffer`
6. {value: "C", timestamp: 3}@2 received via `sample`
7. [{value: "B", timestamp: 1}, {value: "C", timestamp: 3}]@1 sent via `buffer`

### Input ports:

* __sample__: _{"value" :any, "timestamp" :number}_

    Receives individual samples to be buffered.



* __size__: _number_

    Size of the buffer in seconds.



### Output ports:

* __buffer__: _{"value" :any, "timestamp" :number}["value"][]_

    Sends current contents of moving buffer.



* __error__: _{"message" :string}_

    Sends error when:
    * size is equal or less than 0 or not set



* __bounced__: _{"value" :any, "timestamp" :number}_

    Forwards input received via `sample` on error.


