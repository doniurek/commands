# [⬅ Back	to Unix commands](unix.md)
# `grep`
Search text for a pattern (print lines matching a pattern)

`grep <pattern> <file>`

## Options
### Matcher selection
`-G` Interpret the pattern as a basic regular expression (BRE). This is the default

`-E` Interpret the pattern as an extended regular expression (ERE). Same as `egrep`

`-F` Interpret the pattern as a list of fixed strings, separated by newlines, any of which is to be matched. Same as `fgrep`

`-e <pattern>` Use &lt;pattern&gt; as the pattern.This option can be used to protect a pattern beginning with “-”

`-f <file>` Obtain patterns from &lt;file&gt;, one per line

 If `-e` or `-f` option is used multiple times or they are combined together - search for all patterns given

 `-v` Invert the sense of matching, to select non-matching lines

`-w` Select only those lines containing matches that form whole words

 `-x` Select only those matches that exactly match the whole line

### General output control
`-c` Instead of normal output print a count of matching lines for each input file. With the `-v` option, count non-matching lines

`-L` Instead of normal output print the name of each input file which doesn't match

`-l` Instead of normal output print the name of each input file which match

In both cases (`-L` and `-l`) the scanning of each file stops on the first match

`-m <num>` Stop reading a file after &lt;num&gt; matching lines

`-s` Suppress error messages about nonexistent or unreadable files

### Output line prefix control
`-H` Print the file name for each match. Default when there is more than one file to search

`-h` Do not print the file name. Default when there is only one file to search

`-n` Prefix each line of output with the 1-based line number

`-T` Initial tab before output lines

### Context line control
`-A <num>` Print &lt;num&gt; lines of trailing context after matching lines

`-B <num>` Print  &lt;num&gt; lines of leading context before matching lines

`-C <num>` Print &lt;num&gt; lines of output context

### File and directory selection
`-D [read / skip]` If an input file is a device,  FIFO or socket treat them just as if they were ordinary files (`read`) or `skip` them

`-d [read / skip / recurse]` If an input file is a directory treat them just as if they were ordinary files (`read`) or `skip` them or read all files under each directory, recursively (`recurse`)

`--exclude <pattern>` Skip files whose base name matches  &lt;pattern&gt;

`--exclude-dir <pattern>` Exclude directories matching the  &lt;pattern&gt; from recursive searches

`--include <pattern>` Search only files whose base name matches &lt;pattern&gt;

`-r` Read all files under each directory, recursively

## Comments
`grep` has many options and long manual - better check it out before use this command.
