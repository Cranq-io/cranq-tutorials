---
description: >-
  This lesson establishes the basic concepts in CRANQ's flavor of dataflow
  programming: nodes, connections, signals, parameters, and tags. What they are,
  and how to use them.
---

# 103: Nodes & connections

CRANQ, as a visual programming language, is based on a special flavor of [dataflow programming](https://en.wikipedia.org/wiki/Dataflow\_programming).

:bulb: The simplest illustration of dataflow programming is doing laundry:

1. You take dirty clothes (signal) to the washing machine (node), where they get clean and wet (state changes).
2. Then you put the clean, wet clothes (output from previous node) into the dryer (another node), where they become dry and wrinkled (state changes again).
3. Finally, you iron (node) the dry, wrinkled clothes (last output), and end up with unwrinkled ones (final output).

## Node

_The_ unit of processing in CRANQ. It takes data from [signals](./#signal) and [parameters](./#parameter) through input [ports](./#port), processes the data, and sends the result via output [ports](./#port).

Complex nodes are sometimes referred to as _components_ throughout the documentation.

Most nodes have internal structure made up of _child_ nodes and connections between them. Some nodes, especially the most fundamental ones, are implemented using text code, like JavaScript.

We call the definition of a node the _prototype_. Prototypes describe a node's interface: input and output ports, including data types and other attibutes, as well as the implementation - structure or code, but _not_ its parameter values. When we place nodes inside other nodes as children, we call those _instances_. Instances inherit the interface and implementation of the underlying prototype, extended with parameter values set on input ports.

Nodes may or may not have internal state. Those that do, like database connectors, are somewhat harder to test and debug, so it's a good idea to keep them to a minimum.

:information\_source: Documenting statefulness of nodes is a planned feature of CRANQ, aimed at aiding testing and qualitative scoring of nodes in the [repository](../104/).

## Port

Where nodes receive and send data. Data enters nodes through _input_ ports, either as [signals](./#signal), or [parameters](./#parameter), then signals (and signals only) leave via _output_ ports.

Ports have data types associated with them, which helps determining whether a parameter or a connected port is compatible.

Data types in CRANQ must be compatible with [JSON](https://en.wikipedia.org/wiki/JSON), including strings, numbers, boolean (true / false), null, arrays, and dictionaries.

:information\_source: In the future, CRANQ will use data types to find compatible nodes for possible connections.

## Connection

Transmits [signals](./#signal) from an output port to the connected input port. It also propagates the [parameter](./#parameter) set on a parent node's input port to a connected child node's input port.

:bulb: Traffic flowing through connections can be observed by right clicking on the connection and selecting "Show traffic".

## Signal

A unit of data in flow. Signals traverse from output ports to connected input ports. Output ports emit signals, connections transmit them, and input ports receive them.

A signal is made up of JSON data and a [tag](./#tag). This is important because in CRANQ, signals are always assumed to be received asynchronously, ie. not in any particular order and with any particular delay, so signals must carry some other information that serves as a basis of concurrency.

## Parameter

A unit of static data. Instead of receiving them at runtime, parameters are applied once at at compile time. Because parameters have no role at runtime, they don't have tags associated with them.

Parameters set on parent nodes' input ports propagate via connections to child nodes' input ports.

:exclamation: Input ports can't have both a parameter set and receive signals through a connection. In the CRANQ app, setting a parameter will remove any connection on the affected input port, and likewise, making a connection will clear any parameter set on it.

## Tag

Identifies the origin of a signal.

The concept of the tag is the secret sauce in CRANQ's flavor of dataflow programming. Its primary purpose is [synchronization](../../how-to/synchronizing-signals.md) of signals that "go together". For instance, in the case of a node that adds two numbers together (eg. `number/Adder`), the two independent input signals must be recognized as a pair, so the node can calculate their sum. In cases like that, the output inherits the tag of the correspondig inputs.

:wrench: The tag serves other purposes, eg. indicating signal multiplicity at runtime. Typically, nodes that iterate over an array or dictionary, emit signals for each iteration with unique tags, so that synchronization of those signals remain consistent.
