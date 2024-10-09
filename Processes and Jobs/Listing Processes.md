# Listing Processes
## Introduction
This Module focuses on introducing processes, which as the name suggests, are operations that occur in the background which are key to running essential parts of the system
## Approach
- I use ps aux, to display the procceses,as I know the flag will be one of them `ps aux`
- after finding the right process, I execute the command `/challenge/3037-run-30008` to retrieve the flag
## Code
```bash
Connected!
hacker@processes~listing-processes:~$ ps aux
USER         PID %CPU %MEM    VSZ   RSS TTY      STAT START   TIME COMMAND
root           1  0.2  0.0   1056   640 ?        Ss   12:42   0:00 /sbin/docker-init -- /nix/var/nix/profiles/default/bi
root           7  0.0  0.0   5052  2560 ?        S    12:42   0:00 /run/dojo/bin/sleep 6h
root          68  0.0  0.0   4132  2560 ?        S    12:42   0:00 /challenge/3037-run-30008
root          72  0.0  0.0   2744  1600 ?        S    12:42   0:00 sleep 6h
hacker        73  0.3  0.0   5360  3840 pts/0    Ss   12:42   0:00 /run/dojo/bin/ssh-entrypoint
hacker        90  0.0  0.0   7868  3200 pts/0    R+   12:42   0:00 ps aux
hacker@processes~listing-processes:~$ /challenge/3037-run-30008
Yahaha, you found me! Here is your flag:
pwn.college{I2T6uRvRMzo_9yrtwfphiFiqmZb.dhzM4QDLzgTN0czW}
Now I will sleep for a while (so that you could find me with 'ps').
```
