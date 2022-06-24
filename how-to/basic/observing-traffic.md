# Observing traffic

Where the visual nature of CRANQ really shines, is monitoring and debugging running programs.

CRANQ code is a graph - so it seems natural for all kinds of data to be overlaid on top of it. The first, and perhaps most useful overlay shows what happens in the graph while the program is running. As soon as you click "Run" or hit Cmd / Ctrl + R, the app switches into "Activity" view, and the entire graph turns grey. Grey indicates inactivity in nodes and connections. As the program starts however, nodes that got activated turn green. As the program continues to run, you can _see_ nodes activating in realtime.

Moreover, the data flowing through connections can also be observed by opening a "Traffic viewer" window from the connection's context menu, displaying the last signal transmitted over that particular connection (data and tag). By having a few of these traffic viewers open you can monitor the transformation of data through the nodes in view.

{% hint style="info" %}
[Currently](../../roadmap.md#typed-traffic-viewers), traffic viewers can only display data as JSON.
{% endhint %}
