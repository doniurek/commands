# [⬅ Back	to Unix commands](unix.md)
# `xargs`
Convert input from standard input into arguments to a command

By default `xargs` reads items from standard input as separated by blanks and executes a &lt;command&gt; once for each argument. Default &lt;command&gt; is `echo`.

## Options
`-0` Input items are terminated by a null  character  instead of by whitespace, and the quotes and backslash are not special (every character is  taken  literally)

`-a <file>` read items from &lt;file&gt; instead of standard input

`-d <delimiter>` input items are terminated by the specified character

`-L <max-lines>` use at most &lt;max-lines&gt; nonblank input lines per command line

`-n <max-args>` use at most &lt;max-args&gt; arguments per command line

`-P <max-procs>` run up to &lt;max-procs&gt; processes at a time; the default is  1. If max-procs is 0, xargs will run as many processes as possible at a time

`-r` if the standard  input does not contain any nonblanks, do not run the command. Normally, the  command is run once even if there is no input.

## Example
`ls`
```
git.md  README.md  unix
```

`ls | echo`
```

```

`ls | xargs echo`
```
git.md README.md unix
```

`ls | xargs -n 1 echo`
```
git.md
README.md
unix
```
