# Forwarder (triple)

[flow]

Forwards all 3 received signals in the order of the names of the ports.

Used for two purposes:
* Ensuring that any of a node's inputs may receive signals or be set as parameter.
* Ensuring the order in which signals are sent.

For examples, see `flow/Forwarder (double)`.

### Input ports:

* __1__: _any_

    Receives signal or takes parameter to be sent out first.



* __2__: _any_

    Receives signal or takes parameter to be sent out second.



* __3__: _any_

    Receives signal or takes parameter to be sent out third.



### Output ports:

* __1__: _any_

    Forwards signal received via `1` (input).



* __2__: _any_

    Forwards signal received via `2` (input). Does not send before `1` (output).



* __3__: _any_

    Forwards signal received via `3` (input). Does not send before `2` (output).



