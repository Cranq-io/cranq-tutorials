# ✏ Code node

You can implement custom code node in javascript language. _Most cases can be handled with a structure node. Please try to avoid creating new code nodes if possible._  &#x20;

## How to create a code Node

1. Right click on the canvas “Add node”.
2. On the pop up window bottom left click “New Code Node” button.

![](../../.gitbook/assets/add\_code\_node.gif)

## Add ports to the node

Add an input and an output port to the Node:&#x20;

![](../../.gitbook/assets/add\_ports\_to\_node.gif)

## Where to write code&#x20;

In case of code nodes you can add custom javascript to the node and to the input port(s).&#x20;

### Adding code to the node

When you add code to the node, you add code to the init function, or the the cleanup function.&#x20;

* Init will always run before the code of the port. It works like a constructor.&#x20;
* Cleanup will run after the input port(s) code executed. ???

![](../../.gitbook/assets/image.png)&#x20;

#### Parameters of the node functions

```javascript
(outputs, params, state, shared) => void
```

Each of the parameters are javascript object.

* outputs:  contains all output ports name as a key with an empty function as a value. Mostly use at the input ports.
* params:  all the input ports which are not receiving signal are represented here. key is the name of the input port, value is the value of it.
* state: common state of the node instance. During the execution and iteration it can store and keep data    Eg.: data/array/Reducer > reduce&#x20;
* shared: common state of the all the node which inherited from the same prototype.  ???

### Adding code to the port(s)

![](<../../.gitbook/assets/image (1).png>)

#### Parameters of the port(s) function

```javascript
(data, tag, outputs, params, state, shared) => void
```

* data: is the received data, it can came from the instance of the port, or with the signal.
* tag: this is the unique identifier of the signal. Check [this](../basics/103/#tag) for more details.
* outputs: contains all output ports name as a key with an empty function as a value. Mostly use at the input ports.
* params: all the input ports which are not receiving signal are represented here. key is the name of the input port, value is the value of it.
* state: common state of the node instance. During the execution and iteration it can store and keep data    Eg.: data/array/Reducer > reduce&#x20;
* shared: common state of the all the node which inherited from the same prototype.  ???



## Sample of a code node





