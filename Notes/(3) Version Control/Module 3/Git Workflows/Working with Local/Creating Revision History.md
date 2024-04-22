One of the most common and basic [[Tools and Strategies#Workflow|workflows]] in Git to maintain the [[The Why#Revision History|revision history]] of a repository involves four states of a file. 

The status of a repo can be verified using the `status` command.

```shell
git status 
```

### Untracked
Any new file created in an initialized [[Accessibility#Local|local repo]] is **untracked**. In other words, Git doesn't have the ability to *track* the changes made in it. 

To give this right to Git, the command `add` is used. 
```shell
git add .
```

>[!info]
>`.` is used to track all the files for every Git command.

>[!info]
>Any changes made to Untracked files can be reverted using the command `git reset --hard HEAD`


<br>

### Modified
Whenever a file is renamed, deleted or updated, it is considered **modified** in Git terminology.
```shell
cd my-repo
touch readme.md
```

### Staged
After any changes in the file that need to be saved, the file is *brought onto the stage*. 
Just like some subject brought onto the stage to get a photo clicked.

```shell
git stage readme.md
```

To remove the file from being **staged**, the `restore` command with the `--stage` flag.
```shell
git restore --stage readme.md
```

### Committed
If the changes need to be saved, the changes in the files are **committed** or in other words, their photograph is finally clicked.

```shell
%% Adding some text in the file via input %%
cat > readme.md

git commit readme.md
```

This *photograph* or **commit** of the changes made goes to the `.git` folder where the **revision history** is stored.

## Example
As a developer, you are assigned the task to write a JS program in a repository and **commit** it.

1.  ##### Create a Repository
```shell
%% Changing directory (if needed) %%
cd myprojects

git init
```
2. ##### Create a file and Write the Program
```shell
touch index.js
cat > index.js
```
3. ##### Add, Stage and Commit
```shell
%% Add %%
git add index.js

%% Stage %%
git stage index.js

%% Commit %%
git commit -m "Created a JS program called index" index.js
```


> [!warning]
> Note that `add` command is to be used only once for a file and for every subsequent change made, use the `stage` followed by `commit` command.


> [!note]
> Here, the `-m` [[CLI#Flags|flag]] is used to add a message to the commit made to indicate what change has been made.

