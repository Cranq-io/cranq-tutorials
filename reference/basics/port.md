# Port

The port is where nodes receive and send data. Data enters nodes through _input_ ports, either as [signals](signal.md), or [parameters](parameter.md), then signals (and signals only) leave via _output_ ports.

![Ports on a node](<../../.gitbook/assets/Screenshot 2022-07-18 at 15.40.20.png>)

Ports have data types associated with them, which helps determining whether a parameter or a connected port is compatible. Connecting incompatible ports may lead to unexpected behavior (bugs).

![Port's data type on the prototype tab](<../../.gitbook/assets/Screenshot 2022-07-18 at 15.41.50.png>) ![Port's data type on the instance tab](<../../.gitbook/assets/Screenshot 2022-07-18 at 15.42.43.png>)

Data types in CRANQ must be compatible with [JSON](https://en.wikipedia.org/wiki/JSON), including strings (text), numbers, boolean (true / false), null (special value), arrays (lists), and dictionaries (records).
