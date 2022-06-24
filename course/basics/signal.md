# Signal

The signal is a unit of data _in flow_. Signals traverse from output [ports](port.md) to connected input ports. Output ports emit signals, connections transmit them, and input ports receive them.

A signal is made up of JSON data and a [tag](tag.md). This is important because in CRANQ, it doesn't matter in what order and when exactly are signals received. So in order to determine which signals belong together, we need some extra information - this is the tag.
