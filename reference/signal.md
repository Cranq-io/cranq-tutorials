# Signal

The signal is a unit of data _in flow_. Signals traverse from output [ports](port.md) to connected input ports. Output ports emit signals, connections transmit them, and input ports receive them.

![Signal contents](<../../.gitbook/assets/Screenshot 2022-07-18 at 15.52.37.png>)

A signal is made up of JSON data and a [tag](tag.md). This is important because in CRANQ, it doesn't matter in what order and when exactly are signals received. So in order to determine which signals belong together, we need some extra information - this is the tag.

![Signal's data](<../../.gitbook/assets/Screenshot 2022-07-18 at 15.54.43 copy.png>) ![Signal's tag](<../../.gitbook/assets/Screenshot 2022-07-18 at 15.54.43.png>)
