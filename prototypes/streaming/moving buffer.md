# Moving buffer

[streaming]

Stores the last N inputs received via `sample` and sends them via `buffer`.

Errors on invalid `size`.

Data sent via `buffer` is immutable.

Example:
1. `size` set to 2
2. "A"@0 received via `sample`
3. ["A"] sent via `buffer`
4. "B"@1 received via `sample`
5. ["A","B"] sent via `buffer`
6. "C"@2 received via `sample`
7. ["B", "C"] sent via `buffer`

### Input ports:

* __sample__: _any_

    Receives individual samples to be buffered.



* __size__: _number_

    Specifies the maximum number of samples stored in the buffer.
    
    Must be parameter.



### Output ports:

* __buffer__: _any[]_

    Sends current contents of moving buffer.



* __error__: _{"message" :string}_

    Sends error when:
    * size is equal or less than 0 or not set



* __bounced__: _any_

    Forwards input received via `sample` on error.


