**Git** is a [[Course/FrontEnd Dev/(3) Version Control/Module 1/The What|Distributed Version Control System]] which can be installed locally from the [official Git website](https://git-scm.com/downloads). 

**GitHub** is a UI, *User Interface*, for Git which has its own [[CLI]] called **GitHub CLI** which can be installed from its [official website](https://cli.github.com/).

<br>

<iframe src="https://www.github.com" style="height: 350px; width: 780px;"></iframe>

<br>

### Setup
Both of Git and GitHub require setup to work with them.
* ##### GitHub
It can be done by creating an account on [GitHub](https://www.github.com). 
<br>

* ##### GitHub CLI
For `gh`, the user must be authenticated via GitHub by executing the following command in GitHub CLI, itself, and proceeding with the inputs.
```shell
gh auth login
```
<br>

* ##### Git
	* First, create an SSH key-pair using `ssh-keygen`
	* Two files will be created, after entering the right input
	* Copy the contents of `<filename>.pub` 
	* Go to `GitHub > Menu > Settings > SSH and GPG keys > New SSH key`
	* Give it a name of choice
	* Paste the key and Add it
	* In the Git Bash, run the command `git config --global credential.helper store`
	* Done!

### Creating a Repository
A [[Course/FrontEnd Dev/(3) Version Control/Module 1/The What#^33d009|repository]] or ***repo*** for short contains some files and mainly [[The Why#Revision History|revision history]].

* Head over to the `New` button on the left panel.
* Add the name of your repository
* Choose for 
	* `Public` → Anyone can see it 
	* `Private` → Only you can see 
* Create the repository