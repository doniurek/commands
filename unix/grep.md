# [⬅ Back	to Unix commands](unix.md)
# `grep`
Search text for a pattern (print lines matching a pattern)

`grep <pattern> <file>`

## Options
### Matcher selection
`-G` Interpret the pattern as a basic regular expression (BRE). This is the default.

`-E` Interpret the pattern as an extended regular expression (ERE). Same as `egrep`

`-F` Interpret the pattern as a list of fixed strings, separated by newlines, any of which is to be matched. Same as `fgrep`

`-e <pattern>` Use &lt;pattern&gt; as the pattern.This option can be used to protect a pattern beginning with “-”.

`-f <file>` Obtain patterns from &lt;file&gt;, one per line.

 If `-e` or `-f` option is used multiple times or they are combined together - search for all patterns given.

 `-v` Invert the sense of matching, to select non-matching lines.

`-w` Select only those lines containing matches that form whole words.

 `-x` Select only those matches that exactly match the whole line.

### General output control
`-c` Instead of normal output print a count of matching lines for each input file. With the `-v` option, count non-matching lines

`-L` Instead of normal output print the name of each input file which doesn't match

`-l` Instead of normal output print the name of each input file which match

In both cases (`-L` and `-l`) the scanning of each file stops on the first match.

`-m <num>` Stop reading a file after &lt;num&gt; matching lines.

`-s` Suppress error messages about nonexistent or unreadable files.

## Examples

## Comments
`grep` has many options and long manual - better check it out before use this command.
