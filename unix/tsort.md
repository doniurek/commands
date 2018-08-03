# [⬅ Back	to Unix commands](unix.md)
# `tsort`
Perform topological sort

## Examples
`cat recipe.txt `
```
buy_bread slice_bread
slice_bread put_ham
buy_ham slice_ham
slice_ham put_ham
put_ham put_tomato
```
Notice, that you don't have to buy or even slice tomato - you have special GMO species of tomatoes in your garden which are self-slicing!

`tsort recipe.txt`
```
buy_bread
buy_ham
slice_bread
slice_ham
put_ham
put_tomato
```
