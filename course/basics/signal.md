# Signal

A unit of data in flow. Signals traverse from output ports to connected input ports. Output ports emit signals, connections transmit them, and input ports receive them.

A signal is made up of JSON data and a [tag](signal.md#tag). This is important because in CRANQ, it doesn't matter in what order and when exactly are signals received. So in order to determine which signals belong together, we need some extra information - this is the tag.
