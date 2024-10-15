# The Path Variable
## Introduction
the PATH variable is an environmental variable that specifies a set of directories of where executable programs are found, in this problem we mess with the PATH variable so that it cant find the rm command
## Approach 
- I set the PATH variable to nothing using `PATH=""`
- then I run `/challenge/run` since the `rm` command should not be found anymore by the program,retrieving the flag
## Code
```bash
hacker@path~the-path-variable:~$ PATH=""
hacker@path~the-path-variable:~$ /challenge/run
Trying to remove /flag...
/challenge/run: line 4: rm: No such file or directory
The flag is still there! I might as well give it to you!
pwn.college{sp-82RzubJHRG35fN_i9QXe10QP.dZzNwUDLzgTN0czW}
```
