# [⬅ Back	to Unix commands](unix.md)
# `diff`
Compare files line by line

## Options
`-c <num>` output <num> (default 3) lines of copied context
 
`-y` output in two columns

`-r` recursively compare any subdirectories found


## Examples
`cat test1.txt`
> lol\
kek\
xD\
hehehe\
huehue\
lel

`cat test2.txt`
> lol\
xD\
hihihi\
huehue\
lel\
lel

`diff test1.txt test2.txt`
>2d1\
< kek\
4c3\
< hehehe\
\---\
\> hihihi\
6a6,7\
\> lel\
\>

* left digit - line in first file
* right digit - line in second file
* characters:
  * d - deletion
  * c - change
  * a - addition

`diff -c test1.txt test2.txt`
>\*\*\* test1.txt	2018-07-08 17:44:45.076553899 +0200\
--- test2.txt	2018-07-08 17:45:34.461019622 +0200\
\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\
\*\*\* 1,6 \*\*\*\*\
  lol\
\- kek\
   xD\
! hehehe\
  huehue\
  lel\
--- 1,7 ----\
  lol\
  xD\
! hihihi\
  huehue\
  lel\
\+ lel\
\+
