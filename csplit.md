# [⬅ Back	to Unix commands](Unix.md)
# `csplit`
Split files based on context

Output  pieces  of  __file__ separated by __pattern(s)__ to files 'xx00', 'xx01', ..., and output byte counts of each piece

Each __pattern__ can be
* __integer__ - copy up to but not including specified line number
* __regexp__ - copy up to but not including a matching line

Additional
* {&lt;integer&gt;} repeat the previous pattern specified number of times

* {\*} repeat the previous pattern as many times as possible


`csplit <file> <pattern>`

## Options
`-f <prefix>` use __prefix__ instead of 'xx'

## Examples
`cat -n test.txt`
> 1	q
     2	w
     3	e
     4	r
     5	t
     6	y
     7	u
     8	i
     9	o
    10	p
    11	a
    12	s
    13	d
    14	f
    15	g
    16	h
    17	j
    18	k
    19	l


`csplit test.txt 10` → split before 10th line
>18
20

first file has 18 bytes and second has 20 bytes

`ls`
> test.txt
xx00
xx01

`cat -n xx00`
> 1	q
     2	w
     3	e
     4	r
     5	t
     6	y
     7	u
     8	i
     9	o

`cat -n xx01`
>   1	p
     2	a
     3	s
     4	d
     5	f
     6	g
     7	h
     8	j
     9	k
    10	l

`csplit -f test test.txt 10`
name of new files will be "test00" and "test01"
