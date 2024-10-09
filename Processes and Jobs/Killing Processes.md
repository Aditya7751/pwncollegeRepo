# Killing Processes
## Introduction
This Problem deals with terminating processes using the `kill` command
## Approach
To get the flag in this problem we need to kill the `/challenge/dont_run` process before running the `/challenge/run` command, to do this :
- I execute `ps aux` to find the PID of the `/challenge/dont_run` command
- then I use `kill /challenge/dont_run` to terminate that process
- then I finally run `/challenge/run` to get the flag
## Code
```bash
Connected!
hacker@processes~killing-processes:~$ ps aux
USER         PID %CPU %MEM    VSZ   RSS TTY      STAT START   TIME COMMAND
root           1  0.3  0.0   1056   640 ?        Ss   12:51   0:00 /sbin/docker-init -- /nix/var/nix/profiles/default/bi
root           7  0.0  0.0   5052  2240 ?        S    12:51   0:00 /run/dojo/bin/sleep 6h
root          71  0.0  0.0   4732  2880 ?        S    12:51   0:00 su -c /challenge/.launcher hacker
hacker        73  0.0  0.0   4976  3200 ?        Ss   12:51   0:00 /challenge/dont_run
hacker        74  0.0  0.0   5052  2240 ?        S    12:51   0:00 sleep 6h
hacker        75  0.2  0.0   5360  3840 pts/0    Ss   12:51   0:00 /run/dojo/bin/ssh-entrypoint
hacker        92  0.0  0.0   7868  3200 pts/0    R+   12:51   0:00 ps aux
hacker@processes~killing-processes:~$ kill 74
hacker@processes~killing-processes:~$ /challenge/run
Great job! Here is your payment:
pwn.college{s5-iziwpiy26npeVQwMhP3jfph9.dJDN4QDLzgTN0czW}
```
