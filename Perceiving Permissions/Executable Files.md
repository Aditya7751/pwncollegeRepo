# Executable Files
## Introduction
While Last problem had us changing the permissions to make a file readable, in this one we have to make /challenge/run executable and then execute it to get the flag
## Approach
- I use `chmod u+x /challenge/run` to give the current user execute permissions
- I then execute `/challenge/run` and get the flag
## Code
```bash
Connected!
hacker@permissions~executable-files:~$ chmod u+x /challenge/run
hacker@permissions~executable-files:~$ /challenge/run
Successful execution! Here is your flag:
pwn.college{0F5j89poO61btdnaZl3RgYLsU4L.dJTM2QDLzgTN0czW}
```
