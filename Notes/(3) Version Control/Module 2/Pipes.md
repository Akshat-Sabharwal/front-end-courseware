Pipe establishes connection between points. It takes the input from one and transports it to the other end as output.

Pipes, in CLI, act the same way. They take the output from a command as the input to another command.
![[Pasted image 20231021183853.png|400]]
### Example
To get the word count of a file, a way would be
```shell
cat textfile.txt
wc textfile.txt -w
```

Using a **pipe**, it can be done as follows.
```shell
cat textfile.txt | wc -w
```

* First, `textfile.txt` is printed out
* The printed text, then, is taken as the input for the next command
* Word count of the text is then printed