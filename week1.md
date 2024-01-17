# CSE 15L - Lab Report 1 - Dylan Williams

## `cd` command
using the command with **no arguments**:
```
[user@sahara ~/lecture1}$ cd
[user@sahara ~]$
```
directory at time of command: `/home/lecture1`
I got this output because using `cd` with no arguments takes you to the home directory. The output reflects this change with the absence of `/lecture1` in the prompt.
No error is produced.

using the command with a path to a **directory** as an argument:
```
[user@sahara ~}$ cd lecture1/messages
[user@sahara ~/lecture1/messages]$
```
directory at time of command: `/home`
I got this output because using `cd` with a path to a directory as an argument takes you to the working directory specified by the path. The output reflects this change as `/lecture1/messages` is seen in the prompt.
No error is produced.

using the command with a path to a **file** as an argument:
```
[user@sahara ~/lecture1/messages]$ cd fr.txt
bash: cd: fr.txt: Not a directory
```
directory at time of command: `/home/lecture1/messages`
I got this output because using `cd` only works if the argument is a valid directory, which `file.txt` is not. This is reflected in the output as an error message is produced.


## `ls` command
using the command with **no arguments**:
```
[user@sahara ~/lecture1/messages]$ ls
en-us.txt  es-mx.txt  fr.txt  zh-cn.txt
```
directory at time of command: `/home/lecture1/messages`
I got this output because using `ls` lists the files and folders within the given path. With no arguments, `ls` refers to the current working directory.
No error is produced.

using the command with a path to a **directory** as an argument:
```
[user@sahara ~/lecture1/messages]$ ls /home
lecture1
```
directory at time of command: `/home/lecture1/messages`
I got this output because using `ls` while giving a path to a directory as an argument lists the files and folders within that directory. The output shows `lecture1` which is the only folder in the home directory.
No error is produced.

using the command with a path to a **file** as an argument:
```
[user@sahara ~/lecture1/messages]$ ls fr.txt
fr.txt
```
directory at time of command: `/home/lecture1/messages`
I got this output because using `ls` while giving a path to a file simply lists the file name.
No error is produced.


## `cat` command
using the command with **no arguments**:
```
[user@sahara ~/lecture1/messages]$ cat
        
```
directory at time of command: `/home/lecture1/messages`
I got this output because `cat` uses file names to read the contents inside the files. Using this command without arguments means there are no files to read from, which produces no output as well as an error.

using the command with a path to a **directory** as an argument:
```
[user@sahara ~]$ cat lecture1
cat: lecture1: Is a directory
```
directory at time of command: `/home`
I got this output because `cat` reads file contents of the given argument. An error message occurs, telling me that `lecture1` is a directory, so there are no file contents to be concatenated.

using the command with a path to a **file** as an argument:
```
[user@sahara ~]$ cat lecture1/messages/en-us.txt
Hello World!
```
directory at time of command: `/home`
I got this output because `cat` reads file contents of the given argument. The output correctly reads the contents of the `en-us.txt` file, which I gave as a path in the argument for the command.
No error is produced.


