# [⬅ Back	to Unix commands](Unix.md)
# `find`
Find files

`find` searches the directory tree rooted at each given starting-point. If no starting-point is specified, '.' (current directory) is assumed.

`find [-H / -L / -P] <path> [expression]`
The three options control how the `find` command should treat symbolic links. The default behaviour is never to follow symbolic links. This can be explicitly specified using the `-P` flag. The `-L` flag will cause the find command to follow symbolic links. The `-H` flag will only follow symbolic links while processing the command line arguments.

Expression elements are whitespace-separated and evaluated from left to right. They can contain logical elements.
An expression is composed of a sequence of things:
- Tests
- Actions
- Global options
- Positional options
- Logical operators

## Options
### Tests
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
E.g.
`find . -perm /220`
`find . -perm /u+w,g+w`
`find . -perm /u=w,g=w`
All three of these commands do the same thing - search for files which are writable by either their  owner or their group.

`size [+/-]<n>[c/w/b/k/M/G]`
File uses &lt;n&gt; units of space, rounding up. The  following  suffixes can be used:
- `b`    for  512-byte  blocks  (this is the default if no suffix is used)
- `c`    for bytes
- `w`    for two-byte words
- `k`    for Kilobytes (units of 1024 bytes)
- `M`    for Megabytes (units of 1048576 bytes)
- `G`    for Gigabytes (units of 1073741824 bytes)

The `+` and `-` prefixes signify greater than and less than.

`user <uname>` File is owned by user &lt;uname&gt;.

### Actions
`-delete` Delete files (in case you want use this option, you should also type `-depth` after `<path>`)

`-exec <command>` Execute command.

`-ok <command>` Like -exec  but  ask the user first.  If the user agrees, run the command.

`-fprint <file>` Print the full file name into file file.

### Global options
Global options take effect even for tests which occur earlier on the command line so they should be specified on the command-line just after `<path>`

`-depth` Process each directory's contents before the  directory itself.

`-maxdepth <level>` Descend at most &lt;level&gt; of directories below the starting-points, e.g. `-maxdepth 0` means only apply the tests and actions to the starting-points themselves.

`-mindepth <level>` Do not apply any tests or actions at levels less than &lt;level&gt;, e.g. `-mindepth 1` means process all files except the starting-points.

`-noleaf` Omit leaves.

## Examples
`find /var/ftp/mp3 -name '*.mp3' -type f -exec chmod 644 {} \;`
Changes the permissions of all regular files whose names end with .mp3 in the directory tree /var/ftp/mp3

`find . -size +100k -a -size -500k`
Searching files whose size is between 100 kilobytes and 500 kilobytes

`find . -size 0k`
Searching empty files

## Comments
`find` has many options and long manual - better check it out before use this command.
