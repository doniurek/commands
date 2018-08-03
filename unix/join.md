# [⬅ Back	to Unix commands](unix.md)
# `join`
Merges the lines of two sorted text files based on the presence of a common field.

The default join field is the first, delimited by blanks.

## Options
`-a <filenumber>` also print unpairable lines from file &lt;filenumber&gt;, where &lt;filenumber&gt; is 1 or 2, corresponding to &lt;file1&gt; or &lt;file2&gt;

`-t <character>` use &lt;character&gt; as input and output field separator

`-1 <field>` join on this &lt;field&gt; of file 1

`-2 <field>` join on this &lt;field&gt; of file 2

## Examples
`cat test1.txt`
```
ann,158,67,158
bob,189,88,120
john,175,100,148
```

`cat test2.txt`
```
ann,white,pizza,tea
john,green,dumplings,coke
simon,blue,nuggets,coffee
```

`join -t , test_joina.txt test_joina2.txt`
```
ann,158,67,158,white,pizza,tea
john,175,100,148,green,dumplings,coke
```

## Comments
&lt;file1&gt; and &lt;file2&gt; must be sorted on the join fields!
