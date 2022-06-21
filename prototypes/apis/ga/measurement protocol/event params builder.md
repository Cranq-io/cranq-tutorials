# Event params builder

[apis/ga/measurement protocol]

Builds raw "event" parameter set for Google Analytics Measurement Protocol request.

### Input ports:

* __tracking ID__: _any_



* __client ID__: _any_



* __category__: _any_



* __action__: _any_



* __label__: _any_



* __value__: _any_



### Output ports:

* __params__: _{string: ({string: any} and {string: any})}_

    Measurement Protocol parameters for "event" hit type. Key-value pairs, must be serialized to be passed as payload.



