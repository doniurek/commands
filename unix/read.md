# [⬅ Back	to Unix commands](unix.md)
# `read`
Allows scripts to catch information entered by users interactively

The read command is used to get a line of input into a variable. Each argument must be a variable name without the leading "$". The built in command reads a line of input and separates the line into individual words. Each word in the line is stored in a variable from left to right. The first word is stored in the first variable, the second word to the second variable and so on. If there are fewer variables than words, then all remaining words are then assigned to the last variable. If you have more variables than words defined, then any excess variables are set to null. If no variable names are supplied to the read line, then the read uses the default variable REPLY.

## Options
`-n <num>`	read returns after reading &lt;num&gt; characters

`-r`	Backslash does not act as an escape character

`-s`	Silent Mode. Characters are not echoed coming from a Terminal

`-t <num>`	read will timeout after &lt;num&gt; of seconds. Only from a Terminal

`-u <0/1/2>` read input from Filed Descriptor
- 0 - standard input
- 1 - standard output
- 2 - standard error

## Example
script.sh
```shell
#!/bin/bash
echo "Please enter your name and surname and press ENTER:"
read name surname
echo "Hello $name $surname"
```

`./script.sh`
>Please enter your name and surname and press ENTER:\
Nicalas Cage\
Hello Nicalas Cage

script2.sh
```shell
#!/bin/bash
read -u 0 name surname
echo "Hello $name $surname"
```

`echo Barbara Streisand | ./script2.sh`
>Hello Barbara Streisand
