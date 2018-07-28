# [⬅ Back	to Unix commands](unix.md)
# `strings`
Find printable strings in files

Prints the printable character sequences that are at least &lt;num&gt; characters long (4 characters by default) and are followed by an unprintable character

## Options
`-a` (default) scan the whole file, regardless of what sections it contains or whether those sections are loaded or initialized

`- <file(s)>` perform full scans of any &lt;file(s)&gt; that is/are mentioned after the `-` on the command line, even if the `-d` option has been specified

`-d` only print strings from initialized, loaded data sections in the file

`-f` print the name of the file before each string

`-n <num>` or `-<num>` print sequences of characters that are at least &lt;num&gt; characters long, instead of the default 4

`-e <encoding>` select the character encoding of the strings that are to be found. Possible values for &lt;encoding&gt; are:
- `s` = single-7-bit-byte characters (ASCII, ISO 8859, etc., default)
- `S` = single-8-bit-byte characters
- `b` = 16-bit bigendian
- `l` = 16-bit littleendian
- `B` = 32-bit bigendian
- `L` = 32-bit littleendian

`l` and `b` apply to, for example, Unicode UTF-16/UCS-2 encodings

## Example
`string -n 10 test`
print strings that are at least 10 characters long

## Comment
`strings` is mainly useful for determining the contents of non-text files
