---
description: >-
  You can implement custom code nodes in CRANQ using the JavaScript language.
  Keep in mind, that most use cases can be handled with a structure node. Please
  try to avoid creating new code nodes if possi
---

# Creating code nodes

## Create a code Node

* Start out with a blank project: only the "start" and "log" nodes should be on the canvas.
* Right click on the canvas, then select “Add node”.
* In the bottom left corner of the pop up window, click “New Code Node”.

<figure><img src="../.gitbook/assets/image (9).png" alt=""><figcaption></figcaption></figure>

## Add ports to the node

Add one input and one output port to the node by clicking the "add port" buttons on both sides.&#x20;

<figure><img src="../.gitbook/assets/image (36).png" alt=""><figcaption></figcaption></figure>

## Where to write your JS code

You can implement input ports using JavaScript, as well as the initialization and cleanup of entire nodes. Note that once you've added code to a new node, it becomes a "code node", and you won't be able to add internal structure to it anymore. (Ie. it can't be converted to a "structure node".)

In each case, you only type in the body of a function. The arguments are pre-defined for each case below, and the return value is always `void`.

### Implementing initialization and cleanup

These are lifecycle hooks that every node in a CRANQ program will run. After activating a node by clicking on its body (center), you'll find its code editor fields on the "Code" tab of the ispector panel.

* `init` runs on creating the node instance. This is where you initialize the node's state, or register things in the node's shared (static) state. "Init" is similar to a class' constructor.
* `cleanup` is not used at the moment. It's reserved for cleaning up resources on live recompilation of a project.

![](<../.gitbook/assets/image (1).png>)

#### Function arguments

The signature for both `init` and `cleanup` is:

```javascript
(outputs, params, state, shared) => void
```

Where

* `outputs` gives you access to the output ports in case you need to send a signal right away, eg. signalling some error. This example assumes your node has an output port called "out": \`outputs.out("Hello", null)\`.
* `params` lists all input ports that have a value assigned to them, indexed by the name of the input, so initialization / cleanup can take those value into account. You can assign values to input ports on the "Instance" tab of the inspector panel.
* `state` an object that is accessible throughout the entire life cycle of the node instance. It's the place where you typically accumulate or cache data. It's especially important when converting spatial signals to temporal and vice versa, eg. aggregation, mapping, reducing, etc.
* `shared` an object that is accessible to all instances of the same prototype throughout their entire life cycle. It's mostly used when integrating NPM packages with an OOP SDK, for looking up class instances by ID.

### Implementing input ports

Most of the actual (JS) code in a CRANQ app resides in input ports of code nodes. This is where nodes do their processing and invoke other nodes by sending signals through their outputs.

After activating an input port by clicking on it, you'll find its code editor field on the "Code" tab of the inspector panel.

![](<../.gitbook/assets/image (38).png>)

#### Function arguments

```javascript
(data, tag, outputs, params, state, shared) => void
```

* `data` is the data part of the received signal
* `tag` is the tag part of the received signal. The tag identifies a signal's origin.
* `outputs` gives you access to the output ports. It's an object of functions, indexed by the name of the output port. Each output function sends data through the corresponding output. The arguments of output functions are:
  * `data` the data part of the signal being sent
  * `tag` the tag part of the signal being sent
* `params` lists all input ports that have a value assigned to them, indexed by the name of the input.
* `state` an object that is accessible throughout the entire life cycle of the node instance
* `shared` an object that is accessible to all instances of the same prototype throughout their entire life cycle

In case of spread ports there is one more parameter in the list called `input`. It contains the unique name of the port in the spread group.

## Target

Code can compile to different targets. Right now CRANQ supports the following targets:&#x20;

* ES6 (browser)
* ES6 (vanilla)
* ES6 (node.js)

<img src="../.gitbook/assets/image (8).png" alt="" data-size="original">

When creating code nodes, be mindful of what targets you want your node to work in. CRANQ programs that incorporate your code can only be compiled to targets you provided implementation for. Otherwise CRANQ will raise an error at compile time.

<figure><img src="../.gitbook/assets/image.png" alt=""><figcaption></figcaption></figure>

The default target is Vanilla.
