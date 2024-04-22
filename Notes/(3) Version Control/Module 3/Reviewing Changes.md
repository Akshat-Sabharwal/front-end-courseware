The changes committed to a repository or file can be seen via the `git log` command. But ***what changes made***, ***who made them*** and at ***what time*** is accessed by the command `git blame`.

### Command
```shell
git blame filename 
```

#### Output Format
The `blame` command produces output in a specific format.
```shell
<Hash Id>
<Author>
<Timestamp>
<Content>
```
