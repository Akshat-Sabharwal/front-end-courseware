Simply put, lending a helping hand is **contribution**. 

On GitHub, there are numerous projects that are maintained by developers around the world called **Open Source Software**. These can be accessed, used or modified by anyone.
For instance, [Linux](https://www.linux.org) and [Python](https://www.python.org)

![[Pasted image 20231026145305.png|400]]

### Making a Contribution
Say a repository named `softdev` is an **Open Source** project created by `OpenTech`, *i.e.* it is a [[Git and GitHub#Creating a Repository|public]] repository. In order to *make a contribution* or change the *repo*, a series of steps must be implemented.
<br>
* ##### Forking the Repository
	Any *repo* cannot be accessed directly. It, first, must be [[Forking|forked]] into the personal account.
	```shell
	gh repo fork opentech/softdev
	```

* ##### Cloning the Repository
	***Cloning*** means installing a copy of the *repo* on the local device.
	```shell
	git clone https://www.github.com/SomeOrg/OpenTech
	```


* ##### Creating a Feature Branch
	To add a new feature and test it, a new branch is created. Such a branch is called a **feature branch**. 
	```shell
	git branch feature
	git checkout feature
	```

* ##### Making the changes 
	```shell
	%% Some code %%
	```


* ##### Pushing the changes
	```shell
	git push origin feature
	```


* ##### Making a Pull Request
	Simply, making the changes in a copy of the Open Source project won't work. The changes must be merged with the main project. 

	To do this, a request must be sent to the owner of the project to review and merge the changes. This is called a **Pull Request**. 

	```shell
	gh pr create
	```