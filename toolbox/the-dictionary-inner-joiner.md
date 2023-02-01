---
description: Want to merge two Dictionaries?
---

# 👬 The Dictionary Inner Joiner

You’ll learn about the quickest way to adapt environment variables; rename and filter them to match connector requirements, using the dictionary “Inner Joiner”.

Most CRANQ nodes that deal with data (that is more complex than a simple number or string), receive and send signals as Dictionaries.  But sometimes we need to adjust the Values or Keys of those Dictionaries, for example, changing them from camel-case to uppercase.

The Inner Joiner takes the values of Dictionary A, and looks for the same values among the keys of Dictionary B. For each matching pair, an item will be added to the result - where the key is the corresponding key from A, and the value is the corresponding value from B.

The matched values on the inside here will disappear from the result as if they were pinched out. This is why it's called an Inner Joiner. &#x20;

Anyhow, let's follow Dan in this video where he explains the Inner Joiner, especially in regards to Environment Variables, where it's often used.&#x20;

{% embed url="https://youtu.be/_qjt2sdD9Go" %}
