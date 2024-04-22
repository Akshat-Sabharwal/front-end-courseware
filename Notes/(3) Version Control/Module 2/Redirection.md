**Redirecting** means deviating something from its original path.
![[Pasted image 20231021191407.png|300]]
In CLI, it means the same but in context of the location of files. All the inputs and outputs of the commands in CLI go to the `stdout` standing for **Standard Output** and `stdin` standing for  **Standard Input** which are files to store the data.

The location or file where the data goes can be customized or in other words, *it can be **redirected***.

### Input
To accept input from the user, the `cat` command can be used. `Ctrl+D` can be used to stop accepting input.
```shell
cat 
```

**Redirecting** the input to a custom file can be done using `>` operator which can be then read out using the `<` operator.
```shell
%% Accepting input %%
cat > input.txt

%% Printing output %%
cat < input.txt
```

### Output
To store the output of a command, the `>` operator can be used here, as well. 
```shell
wc textfile.txt -w > output.txt
```

### Error
The `2>` can be used here to store any error caused by a command.
```shell
%% helloworld.txt does not exist %%
wc helloworld.txt -w 2> error.txt
```
