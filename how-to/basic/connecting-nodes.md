# Connecting nodes

While dragging components on the canvas doesn't require much [explanation](../../readme/102.md), connecting components might get tricky when dealing with _iteration_ and _aggregation_.

{% hint style="info" %}
During iteration we break down lists or sets and send out each item as an individual signal. Aggregation is the opposite: we receive multiple signals, collect them, and send the result as a signle signal.
{% endhint %}

Not all pairs of output-input ports can be connected meaningfully. Connecting ports of incompatible data types (eg. the output sends a `string` but the input expects a record), or when the input's expectation about the signal's tag is not satisfied (eg. trying so sync an item from an iteration with the original list).

In most cases though, such as communicating with an API endpoint, we needn't worry about this.
