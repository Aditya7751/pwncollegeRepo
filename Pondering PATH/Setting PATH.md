# Setting PATH
## Introduction
This Problem Has us introduce a new command to PATH, `win`, but
## Approach
- I start by executing `PATH=$PATH:/challenge/more_commands/` essentially appending a new directory to the previous PATH
- after the path is updated I run `/challenge/run` to get the flag
## Code
```bash
Connected!
hacker@path~setting-path:~$ ls /challenge/more_commands/
win
hacker@path~setting-path:~$ export PATH=$PATH:/challenge/more_commands/
hacker@path~setting-path:~$ /challenge/run
Invoking 'win'....
Congratulations! You properly set the flag and 'win' has launched!
pwn.college{cZhMK1VAFaRFyGQx8o3fXKdc9C1.dVzNyUDLzgTN0czW}
```
## Additional Reading
https://askubuntu.com/questions/109381/how-to-add-path-of-a-program-to-path-environment-variable
