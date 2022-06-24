# Finding bugs

Most bugs in CRANQ don't surface as errors. They are caused by nodes not sending the expected output in response to the input they receive. In other words, the most common symptom of buggy CRANQ code is signals being stuck.

Stuck signals are just as easy to localize as errors, but we're looking for different visual cues. Instead of red nodes, they're indicated by nodes that received input (green upstream connections), but did not send all of the expected output (some or all downstream connections are grey).
