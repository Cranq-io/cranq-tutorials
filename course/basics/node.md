# Node

_The_ unit of processing in CRANQ. It takes data from [signals](node.md#signal) and [parameters](node.md#parameter) through input [ports](node.md#port), processes the data, and sends the result via output [ports](node.md#port).

Most nodes have internal _structure_ made up of _child_ nodes and connections between them. Some nodes, especially the most fundamental ones, are implemented using text code, like JavaScript.

Nodes may or may not have internal _state_. The ones that do, like database connectors, are somewhat harder to test and debug, so it's a good idea to keep the number of stateful nodes to a minimum.

### Prototypes and instances

Nodes can be made reusable.

Reusing nodes is very important because that's how we speed up development both for ourselves and for others.

Reusable nodes are called _prototype_s.

When we [add a node from the repo](../../readme/102.md#step-2-add-nodes-from-the-repo), we're actually reusing a node. A node in the repo is therefore always a prototype - and when dragged to the canvas it becomes an _instance_ of a node.

Node instances inherit every property of the prototype - ports, data types, structure, and code - but in addition to these, they can also have parameter values (see [below](node.md#parameter)) set on input ports. Instances can only exist in the context of a parent node, whereas prototypes live in the repo without context.

{% hint style="info" %}
If you've used [Sketch](https://www.sketch.com/) or [Figma](https://www.figma.com/) before, this concept may already be familiar. In Sketch, reusable elements are called _symbols_; in Figma - _components_, and they work pretty much the same way as prototypes do in CRANQ.

In CRANQ, we also call prototypes components sometimes.
{% endhint %}
