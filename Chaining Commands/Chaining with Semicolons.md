# Chaining with Semicolons
## Introduction
Sometimes the need for more complex commands arises, to tackle this one can chain commands, this problem focuses on doing so using semicolons
## Approach
- I chain `/challenge/pwn` and `/challenge/college` as `/challenge/pwn;/challenge/college` maintaining the order I was supposed to
## Code
```bash
root@DESKTOP-MPJ395R:~# ssh -i ./key hacker@dojo.pwn.college
Connected!
hacker@chaining~chaining-with-semicolons:~$ /challenge/pwn;/challenge/college
Yes! You chained /challenge/pwn and /challenge/college! Here is your flag:
pwn.college{w8gxaglmhc7xygsWv3E87f-Rv0X.dVTN4QDLzgTN0czW}
```
