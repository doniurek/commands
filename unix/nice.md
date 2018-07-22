# [⬅ Back	to Unix commands](unix.md)
# `nice`
Run a program with modified scheduling priority

`nice -n <num> <command>` Run &lt;command&gt; with niceness set to &lt;num&gt; value, where &lt;num&gt; is number from -20 (highest priority) to 19 (lowest priority), e.g. `nice -n 5 htop`

The default niceness for processes is inherited from its parent process and is usually 0.

`nice` Print the current niceness.

## Comments
Only the root may set the niceness to a lower value (set higher priority).
