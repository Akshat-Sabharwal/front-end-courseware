**Command Line Interface** or **CLI** is a **GUI** (*goo-ey*) or **Graphical User Interface** used to interact with the computer. It can be used to *command* the computer through an *interface* to perform numerous tasks.

### Setup
The **Git Bash** program is a CLI which can be installed from the [Git website](https://git-scm.com/downloads). It is, generally, used to make Git commands.

### Some actions
Some of the tasks that can be done via the **bash**.
##### Creating a Directory
A directory, essentially a folder, named `userdata` can be created using the `mkdir` command in the **bash**.
```shell
%% Make a directory named userdata %%
mkdir userdata
```

##### Changing Directory
Changing the current working directory to the previously created `userdata` using the `cd` command.
```shell
%% Change current directory to userdata %%
cd userdata
```

##### Create a File
A JavaScript file named `index` can be created using the `touch` command.
```shell
touch index.js
```


### Flags
Often, simply using the commands doesn't suit our needs. **Flags** are the options and choices that are specified with the command to get the desired result.

For instance, while ordering a sandwich in Subway, you might customize the sandwich by providing your choices as 

| Ingredient | Preference |
|--|--|
| Mustard Sauce | Yes |
| Lettuce | No |
| Bread | Whole Wheat |

These are flags which in **bash** could be written as

```shell
order -mustardSauce y -lettuce n -bread whole-wheat
```

>[!warning]
>This is only an example and not an actual instance of the usage of flags in the bash or terminal.

