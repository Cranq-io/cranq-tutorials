# Parameter

A parameter is a value assigned to an input [port](port.md). This is one of the two ways input ports can receive data - the other is getting it through a connection at runtime.

![Setting a parameter value on an input port](<../../.gitbook/assets/Screenshot 2022-07-18 at 15.35.59 (1).png>)

{% hint style="warning" %}
Input ports can't have both a parameter set and receive signals through connections. In the CRANQ app, setting a parameter will remove any connection on the affected input port, and likewise, making a connection will clear any parameter set on it.
{% endhint %}

Parameters are set once and can't be changed during the running of the program.

Parameters set on an input port of a parent node can be inherited by its children through connections.
