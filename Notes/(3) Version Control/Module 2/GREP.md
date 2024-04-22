Standing for **Global Regular Expression Print**, **GREP** is used to filter out the results as wanted.

Using the command `ls`, prints out a whole list of items. 
```shell
ls -l
```
To get what is needed, the results can be filtered using the command `grep` using [[Pipes|pipes]].
```shell
ls -l | grep resources
```

### Flags

| Flags | Usage |
|--|--|
| `-i` | Include partial results which may have the keyword wherever in the filename  |
| `-w` | Results which have the name specified |