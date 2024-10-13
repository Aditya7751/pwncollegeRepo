# Other Users with su
## Introduction
`su` can also be used to switch to other users, if another username is specified as an argument, in this problem we attempt to switch to zardus to get the flag
## Approach
- I run `su zardus` to switch user to zardus, the password is `dont-hack-me`
- then I execute `/challenge/run` to get the flag
## Code
```bash
Connected!
hacker@users~other-users-with-su:~$ su zardus
Password:
zardus@users~other-users-with-su:/home/hacker$ /challenge/run
Congratulations, you have become Zardus! Here is your flag:
pwn.college{Yx8L3ajIgZobja_gUPBl-pwj2F-.dZTN0UDLzgTN0czW}
```
