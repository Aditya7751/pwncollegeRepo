# Resuming Processes
## Introduction
While last problem had us suspending processes, this one has us resume them with the `fg` (foreground) command
## Approach
- I execute `/challenge/run` and then get prompted to suspend the process
- I resume it by executing `fg`, retrieving the flag
## Code
```bash
Connected!
hacker@processes~resuming-processes:~$ /challenge/run
Let's practice resuming processes! Suspend me with Ctrl-Z, then resume me with
the 'fg' command! Or just press Enter to quit me!
^Z
[1]+  Stopped                 /challenge/run
hacker@processes~resuming-processes:~$ fg
/challenge/run
I'm back! Here's your flag:
pwn.college{Iux-NM05qiPK8NCTlqdwIZfKj0z.dZDN4QDLzgTN0czW}
```
