# touching files
In this problem we are introduced to the `touch` command, which allows us to create new files

Steps:
- I change my directory using `cd /tmp`
- I create two new files using `touch pwn` and `touch college` as was instructed
- I run `/challenge/run`

 ```bash
root@DESKTOP-MPJ395R:~# ssh -i ./key hacker@dojo.pwn.college
Connected!
hacker@commands~touching-files:~$ cd /tmp
hacker@commands~touching-files:/tmp$ touch pwn
hacker@commands~touching-files:/tmp$ touch college
hacker@commands~touching-files:/tmp$ /challenge/run
Success! Here is your flag:
pwn.college{EimDh8BwbKKnSPVNfyO1wKIFk20.dBzM4QDLzgTN0czW}
```
