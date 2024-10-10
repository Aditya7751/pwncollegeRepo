# Interrupting Processes
## Introduction
Interrupting processes is an alternative to killing them, usually done with a control code like Ctrl+C
## Approach
- I executed `/challenge/run`
- I would not able allowed to get the flag, until I interrupted the process, so I use Ctrl+C to interrupt the program, retrieving the flag
## Code
```bash
Connected!
hacker@processes~interrupting-processes:~$ /challenge/run
I could give you the flag... but I won't, until this process exits. Remember,
you can force me to exit with Ctrl-C. Try it now!
^C
Good job! You have used Ctrl-C to interrupt this process! Here is your flag:
pwn.college{w_M8WK8hNE5YakfweLFrVfUv-r4.dNDN4QDLzgTN0czW}
```
