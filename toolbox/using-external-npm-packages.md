---
description: How to add external NPM packages to a code node.
---

# 👩💻 Using external NPM packages

_Keep in mind, that most use cases can be handled with a structure node. Please try to avoid creating new code nodes if possible._

## Create a code Node

* Start out with a blank project: only the "start" and "log" nodes should be on the canvas.
* Right click on the canvas, then select “Add node”.
* In the bottom left corner of the pop up window, click “New Code Node”.

<figure><img src="../.gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>

## Add dependencies to the Node

* Click on the new node to bing up the inspector panel (right sidebar). Make sure you click on the body of the node, and not one of the ports.
* On the inspector panel, select the “Code” tab.
* Type the names of NPM packages into the "Dependencies" field, one package name per line. When the project starts, (or any project that uses this node) CRANQ will install the latest version of these packages. Specifying package versions for dependencies is not yet available.

<figure><img src="../.gitbook/assets/image (31).png" alt=""><figcaption></figcaption></figure>

## Use the NPM package in the code

We'll go though the following example: our new code node will receive a date in the format "YYYYMMDD", and return number of years between that date and today.

* First, add an input and an output port to the node. (Click the tiny "+" button on each side of the node.)
* Click to the "in" port.
* In the inspector panel, select the "Code" tab add copy the following code into the editor:

```javascript
const moment = require('moment');
outputs.out(moment(data, "YYYYMMDD").fromNow(), tag);
```

<figure><img src="../.gitbook/assets/image (32).png" alt=""><figcaption></figcaption></figure>

## Test your new code node

* Add a "data/Store" node via the repo, (green plus button) and set a date on its "data" port in the "YYYYMMDD" format.
* Connect the "read" input of the "store" node to the "start" node.
* Connect the "data" output of the "store" node to the "in" input our code node.
* Connect the "out" output of our code node to the "data" input of the "log" node.
* Click run

<figure><img src="../.gitbook/assets/image (39).png" alt=""><figcaption></figcaption></figure>

### How to check what NPM packages your CRANQ project uses

* Compile your project. (Menu / Compile / NodeJs)
* Uncompress the compiled "tgz" file, and look in the unzipped folder.
* You'll find all NPM dependencies in the package.json file.
