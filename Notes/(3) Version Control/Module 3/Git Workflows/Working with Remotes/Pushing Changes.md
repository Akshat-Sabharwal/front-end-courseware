Any changes made to the ***cloned*** repo must be, first, committed.

```shell
git stage file1 file2
git commit -m "Commit Message here"
```

Following that, these changes need to be pushed via the *pipeline* to the repository on GitHub. 

This can be done using the Git command `push`. 
```shell
git push pipeline from_where
```
Here, 
* `pipeline` → Name of the remote
* `from_where` → The branch in which the changes are committed

### Example
Pushing the changes to `OpenTech`
```shell
git push origin master
```
It means *push the changes from the master branch to the repo via origin*.
