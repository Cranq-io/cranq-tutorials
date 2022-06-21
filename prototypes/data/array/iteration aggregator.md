# Iteration aggregator

[data/array]

### Input ports:

* __data__: _any_

    Receives data items to be aggregated.
    
    Signal tag is expected to have an index. (From iteration)



* __release__: _boolean_

    Receives flag whether to release aggregated inputs. Must be provided for each `data` input signal.
    
    Signal tag is expected to have an index. (From iteration)



### Output ports:

* __aggregated__: _any[]_

    Sends the aggregated data.
    
    Last index will be removed from the input's tag.



