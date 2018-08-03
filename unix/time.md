# [⬅ Back	to Unix commands](unix.md)
# `time`
Report the duration of execution of a particular command/program

`time <command>`

Users of the bash shell need to use an explicit path in order to run the external `time` command and not the shell builtin variant. On system where `time` is installed in /usr/bin syntax is:

`/usr/bin/time <command>`

## Options
`-o <file>` write the resource use statistics to &lt;file&gt; instead of to the standard error stream. By default, this overwrites the file, destroying the file's previous contents

`-a` append the resource use information to the output file instead of overwriting it

`--quiet` do not report the status of the program even if it is different from zero

`-f <format>` use &lt;format&gt; as the format string that controls the output of `time`. The default format is:
```
%Uuser %Ssystem %Eelapsed %PCPU (%Xtext+%Ddata %Mmax)k
%Iinputs+%Ooutputs (%Fmajor+%Rminor)pagefaults %Wswaps
```
Examples of possible format string:
`%E` Elapsed real time used by the process (in [hours:]minutes:seconds)\
`%S` Total number of CPU-seconds that the process spent in kernel mode\
`%U` Total number of CPU-seconds that the process spent in user mode\
`%P` Percentage of the CPU that this job got, computed as (%U + %S) / %E\
`%K` Average total (data+stack+text) memory use of the process, in Kilobytes\
`%W` Number of times the process was swapped out of main memory\
`%I` Number of filesystem inputs by the process\
`%O` Number of filesystem outputs by the process

## Examples
`time ls` (shell builtin variant of `time`)
```
git.md  README.md  unix

real	0m0.002s
user	0m0.000s
sys	0m0.000s
```

`/usr/bin/time ls` (external `time`)
```
git.md	README.md  unix
0.00user 0.00system 0:00.00elapsed 0%CPU (0avgtext+0avgdata 2400maxresident)k
0inputs+0outputs (0major+106minor)pagefaults 0swaps
```
`/usr/bin/time -f %E ls`
```
git.md	README.md  unix
0:00.00
```

`/usr/bin/time -f real_time\\t%E ls`
```
git.md	README.md  unix
real_time	0:00.00
```
