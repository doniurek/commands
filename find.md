# [⬅ Back	to Unix commands](Unix.md)
# `find`
Find files

`find` searches the  directory tree rooted at each given starting-point. If  no  starting-point  is specified, '.' (current directory) is assumed.

`find [-H / -L / -P] <path> [expression]`
The three options control how the `find` command should treat symbolic links. The default behaviour is never to follow symbolic links. This can be explicitly specified using the `-P` flag. The `-L` flag will cause the find command to follow symbolic links. The `-H` flag will only follow symbolic links while processing the command line arguments.

Expression elements are whitespace-separated and evaluated from left to right. They can contain logical elements such.

## Options
`group <gname>` File belongs to group &lt;gname&gt;
`name <pattern>` Base of file name matches shell pattern &lt;pattern&gt;.
`iname <pattern>` Like -name, but the match is case insensitive.  For  example,  the patterns 'fo\*' and 'F??' match the file names 'Foo', 'FOO', 'foo', 'fOo', etc.   The pattern '\*foo\*' will also match  a  file  called '.foobar'.
`amin <n>` File was last accessed &lt;n&gt; minutes ago.
`atime <n>` File was last accessed &lt;n&gt;\*24 hours ago.  When find figures out  how many  24-hour  periods  ago  the file was last accessed, any fractional part is ignored, so to match -atime +1, a file has to  have been accessed at least two days ago.
`cmin <n>` File's status was last changed &lt;n&gt; minutes ago.
`ctime <n>` File's status was last changed &lt;n&gt;\*24 hours ago.
`mmin <n>` File's data was last modified &lt;n&gt; minutes ago.
`mtime <n>` File's data was last modified &lt;n&gt;\*24 hours ago.
`perm <mode>` File's permission bits are exactly  &lt;mode&gt; (octal  or  symbolic).
`size <n>[cwbkMG]`


## Examples

## Comments
