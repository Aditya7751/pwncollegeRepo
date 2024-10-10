# Suspending Processes
## Introduction
This Module deals with suspending processes, it is similar to interrupting processes but less drastic, using Ctrl+Z to execute 
## Approach
- I run `/challenge/run` and am met with a prompt to suspend the process
- I suspend the process using Ctrl+Z
- I run `/challenge/run` again as instructed, to get 2 instances running at the same time, retrieving the flag
## Code
```bash
Connected!
hacker@processes~suspending-processes:~$ /challenge/run
I'll only give you the flag if there's already another copy of me running in
this terminal... Let's check!

UID          PID    PPID  C STIME TTY          TIME CMD
root          82      65  0 13:59 pts/0    00:00:00 bash /challenge/run
root          84      82  0 13:59 pts/0    00:00:00 ps -f

I don't see a second me!

To pass this level, you need to suspend me and launch me again! You can
background me with Ctrl-Z or, if you're not ready to do that for whatever
reason, just hit Enter and I'll exit!
^Z
[1]+  Stopped                 /challenge/run
hacker@processes~suspending-processes:~$ /challenge/run
I'll only give you the flag if there's already another copy of me running in
this terminal... Let's check!

UID          PID    PPID  C STIME TTY          TIME CMD
root          82      65  0 13:59 pts/0    00:00:00 bash /challenge/run
root          89      65  0 14:00 pts/0    00:00:00 bash /challenge/run
root          91      89  0 14:00 pts/0    00:00:00 ps -f

Yay, I found another version of me! Here is the flag:
pwn.college{QpF5a-HvHIXvQPt3ta8EmISCcK6.dVDN4QDLzgTN0czW}
```
