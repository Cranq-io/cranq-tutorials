# Node

The node is _the_ unit of processing in CRANQ. It takes data from [signals](signal.md) and [parameters](parameter.md) through input [ports](port.md), processes the data, and sends the result via output ports.

Most nodes have internal _structure_ made up of _child_ nodes and [connections](connection.md) between them. Some nodes are implemented using text code (like JavaScript), but we rarely need to [create or edit them](../../how-to/advanced/code-node.md).

### Prototypes and instances

Nodes can be made [reusable](../../how-to/basic/reusing-nodes.md).

Reusing nodes is very important because that's how we speed up development both for ourselves and for others.

Reusable nodes are called _prototype_s.

When we [add a node from the repo](../../how-to/basic/finding-nodes.md), we're actually reusing a node. A node in the repo is therefore always a prototype - and when dragged to the canvas it becomes an _instance_ of a node.

Node instances inherit every property of the prototype - ports, data types, structure, and code - but in addition to these, they can also have [parameter](parameter.md) values set on input ports. Instances can only exist in the context of a parent node, whereas prototypes live in the repo without context.

{% hint style="info" %}
If you've used [Sketch](https://www.sketch.com/) or [Figma](https://www.figma.com/) before, this concept may already be familiar. In Sketch, reusable elements are called _symbols_; in Figma - _components_, and they work pretty much the same way as prototypes do in CRANQ.

In CRANQ, we also call prototypes components sometimes.
{% endhint %}
