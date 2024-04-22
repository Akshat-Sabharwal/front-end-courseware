***Remotes*** can be added using Git command in the Bash.

##### List the Remotes
To look for any *pipelines* or remotes currently linked, the Git command `remote` is used.
```shell
git remote -v
```

##### Add a Remote
A **remote** is created between one directory of the computer to a repository on GitHub

```mermaid 
flowchart LR
A[Directory] --> |Remote| B[Repository]
```


```shell
git remote add name_of_the_pipeline url_of_the_repo
```

Here, 
* `name_of_the_pipeline` → Name of the remote or *an alias to the remote* .
* `url_of_the_repo` → URL of the repository which is
`https://www.github.com/<username>/<repository>`.

##### Remove a Remote
After the work is done, the remote ***can***, not necessarily, be removed using the `remote remove` command.
```shell
git remote remove name_of_the_connection
```

### Example
Add a remote or *pipeline* for a repository named `OpenTech`.
```shell
git remote add origin https://www.github.com/SomeOrg/OpenTech
git remote -v
```