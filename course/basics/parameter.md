# Parameter

A unit of static data. Instead of receiving them at runtime, parameters are applied once at compile time. Because parameters have no role at runtime, they don't have tags associated with them.

Parameters set on parent nodes' input ports propagate via connections to child nodes' input ports.

{% hint style="warning" %}
Input ports can't have both a parameter set and receive signals through a connection. In the CRANQ app, setting a parameter will remove any connection on the affected input port, and likewise, making a connection will clear any parameter set on it.
{% endhint %}
