# [⬅ Back	to Unix commands](unix.md)
# `stty`
Change or print terminal line settings

`stty [-F <device>] [setting(s)]`

`stty -a` print all current settings in human-readable form

`stty -g` print all current settings in a stty-readable form

## Options
`-F <device>` open and use the specified &lt;device&gt; instead of standard input

`kill <character>`	&lt;character&gt; will erase the current line

`stop <character>`	&lt;character&gt; will stop the output

`* werase <character>`	&lt;character&gt; will erase the last word typed

`speed`	print the terminal speed

`echo` echo input characters

`-echo` do not echo input characters

## Comment
This command has long manual and many options. Options mentioned above are only example
