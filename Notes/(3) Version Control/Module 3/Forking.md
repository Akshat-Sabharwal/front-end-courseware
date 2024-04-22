Any repository, [[Git and GitHub#Creating a Repository|public]] or [[Git and GitHub#Creating a Repository|private]], can be *copied* onto the personal GitHub account, including its contents. This is called ***forking***.

### Command
There is no Git command for ***forking***. Instead, it can be done using the `gh` command which accesses the [[Git and GitHub#Setup|GitHub CLI]]. 
```shell
gh repo fork URL_of_repo 
```

### Application
Say Microsoft's *repo* `vscode` is to be forked into your account. The *repo* name can be copied from the `GitHub CLI` tab besides the `HTTPS` tab.

```shell
gh repo fork microsoft/vscode
```