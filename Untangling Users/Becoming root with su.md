# Becoming root with su
## Introduction
the `su`(switch user) command is used to switch to the root user, and is essentially the equivalent of getting admin permissions on linux, su is a more primitive version of sudo, due to a lot of potential security vulnerabilites
## Approach
- first I run `su` to switch to root, and enter the password `hack-the-planet`
- I follow it up by reading the flag using `cat /flag`
## Code
```bash
Connected!
hacker@users~becoming-root-with-su:~$ su
Password:
root@users~becoming-root-with-su:/home/hacker# cat /flag
pwn.college{kS4lUGS_l06txm0kAEeMVdRmT9N.dVTN0UDLzgTN0czW}
```
