# [⬅ Back	to Unix commands](unix.md)
# `ps`
Display the currently-running processes

`ps` (without any option) show all processes associated with this terminal

## Options
`-e` select all processes

`-G <group>` select by group ID or name

`-p <pid>` select by process ID

`-U <user>` select by user ID or name

`-o <format>` User-defined format. &lt;format&gt; is a single argument in the form of a blank-separated or comma-separated list. The recognized keywords are described in the *Standard Format Specifiers* section in the manual of command. E.g. it can be:
- `%cpu` cpu utilization of the process, expressed as a percentage
- `%mem` ratio of the process's resident set size to the physical memory on the machine, expressed as a percentage
- `bsdstart` time the command started
- `comm` command name
- `cputime` cumulative CPU time
- `pid` process ID
- `ppid` parent process ID

## Example
To see every process on the system using standard syntax:
- `ps -e`
- `ps -ef`
- `ps -eF`
- `ps -ely`

To see every process on the system using BSD syntax:
- `ps ax`
- `ps aux`

To print a process tree:
- `ps -ejH`
- `ps axjf`

To print every process on the system with memory and cpu usage
- `ps -eo pid,comm,%mem,%cpu`

## Comments
This command has long manual and many other options
