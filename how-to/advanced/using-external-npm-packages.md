---
description: How to add external NPM packages to a code node.
---

# ✏ Using external NPM packages

_Keep in mind, that most use cases can be handled with a structure node. Please try to avoid creating new code nodes if possible._

## Create a code Node

1. Start out with a blank project: only the "start" and "log" nodes should be on the canvas.
2. Right click on the canvas, then select “Add node”.
3. In the bottom left corner of the pop up window, click “New Code Node”.

![](<../../.gitbook/assets/add\_code\_node (1).gif>)

## Add dependencies to the Node

1. Click on the new node to bing up the inspector panel (right sidebar). Make sure you click on the body of the node, and not one of the ports.
2. On the inspector panel, select the “Code” tab.
3. Type the names of NPM packages into the "Dependencies" field, one package name per line. When the project starts, (or any project that uses this node) CRANQ will install the latest version of these packages. Specifying package versions for dependencies is not yet available.

![](../../.gitbook/assets/add\_dependencies\_to\_the\_node.gif)

## Use the NPM package in the code

We'll go though the following example: our new code node will receive a date in the format "YYYYMMDD", and return number of years between that date and today.

1. First, add an input and an output port to the node.
2. Click to the "in" port.
3. In the inspector panel, select the "Code" tab add copy the following code into the editor:

```javascript
const moment = require('moment');
outputs.out(moment(data, "YYYYMMDD").fromNow(), tag);
```

![](../../.gitbook/assets/add\_code.gif)

## Test your new code node

1. Add a "data/Store" node via the repo, (green plus button) and set a date on its "data" port in the "YYYYMMDD" format.
2. Connect the "read" input of the "store" node to the "start" node.
3. Connect the "data" output of the "store" node to the "in" input our code node.
4. Connect the "out" output of our code node to the "data" input of the "log" node.
5. Click run

![](../../.gitbook/assets/working\_code.gif)

### How to check what NPM packages your CRANQ project uses

1. Compile your project. (Menu / Compile / NodeJs)
2. Uncompress the compiled "tgz" file, and look in the unzipped folder.
3. You'll find all NPM dependencies in the package.json file.

