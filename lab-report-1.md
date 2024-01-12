# **Lab Report 1**

## `cd` Test Case findings:
```
[user@sahara ~]$ cd
[user@sahara ~]$ cd lecture1
[user@sahara ~/lecture1]$ cd Hello.java 
bash: cd: Hello.java: Not a directory
```
1. `cd` The working directory when the first command was run was just `/home`.
And the reason we got an empty output for cd was because we did not specify a directory to go to.
The output is not an error for the empty case.

2. `cd 1ecture1`
The working directory when we do `cd lecture1` changes our working directory to `/home/lecture1`.
The reason we got that was because we specified a directory after the command.
The output is not an error

3. `cd Hello.java`
The working directory is still `/home/lecture1`.
We got this output because `Hello.java` is a java file, and the cd command can only work between directories, not files.
I don't believe this output is an error because it makes sense as to why it didn't work.

## `ls` Test Case findings:
```
[user@sahara ~]$ ls
lecture1
[user@sahara ~]$ ls lecture1/
Hello.class  Hello.java  messages  README
[user@sahara ~]$ ls lecture1/Hello.ja
ls: cannot access 'lecture1/Hello.ja': No such file or directory
[user@sahara ~]$ ls lecture1/Hello.java 
lecture1/Hello.java
[user@sahara ~]$
```
1. `ls`
The working directory when this command is run is `/home`.
This output gives us all of the available files and directories in the current working directory.
The output is not an error

2. `ls lecture1`
The working directory is still /home after this command is run. 
We are changing our working directory, rather just checking to see what files are in the directory of our choosing,
in this case it is `lecture1`.
The output is not an error.

3. `ls Hello.java`
The working directory still has not changed and remains `/home`.
We get this output because we are checking to see if there are any files/directories past Hello.java, which there are none.
This output is not an error.

## `cat` Test Case findings:
```
[user@sahara ~]$ cd lecture1/
[user@sahara ~/lecture1]$ cat README 
To use this program:

javac Hello.java
java Hello messages/en-us.txt
[user@sahara ~/lecture1]$ cat messages/
cat: messages/: Is a directory
[user@sahara ~/lecture1]$ cat
exit
exit
```
1. `cat`
Now, our working directory was /home/lecture1 when I ran this command.
However, my output just stopped me from going any further and anything I typed did not seem to work which was interesting.
I think this **is** an error because `cat` needs a prompt and there was none, so maybe it crashed?

2. `cat messages`
The current working directory is `/home/lecture1` when this command was run.
I got this out which basically said that `messages` was a directory. I don't think that `cat` can output directories, only files.
This output is not an error.

3. `cat README`
The current directory when the command was run `/home/lecture1`.
The command stated the contents of the README file because thats how the `cat` commmand should be used.
This output is not an error.
