# [⬅ Back	to Unix commands](unix.md)
# `renice`
Change priority of running processes (one or more)

`nice -n <num> <-g/-p/-u identifier>` Set niceness to &lt;num&gt; value for the process (`-p` default), process group (`-g`) or user (`-u`).

&lt;num&gt; is number from -20 (highest priority) to 19 (lowest priority)

## Example
`renice -n 15 -p 7314`
Change the priority of the process with ID 7314 to 15

`renice +1 987 -u daemon root -p 32`
Change the priority of the processes with PIDs 987 and 32, plus all processes owned by the users daemon and root

`sudo renice -n --5 -g staff`
Change (increase) the priority of all processes belonging to the group "staff"

## Comments
Only the root may set the niceness to a lower value (set higher priority).
