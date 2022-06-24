# Port

Where nodes receive and send data. Data enters nodes through _input_ ports, either as [signals](port.md#signal), or [parameters](port.md#parameter), then signals (and signals only) leave via _output_ ports.

Ports have data types associated with them, which helps determining whether a parameter or a connected port is compatible.

Data types in CRANQ must be compatible with [JSON](https://en.wikipedia.org/wiki/JSON), including strings, numbers, boolean (true / false), null, arrays, and dictionaries.
