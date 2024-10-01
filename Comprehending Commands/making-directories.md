# making directories
In this problem we learn about `mkdir` which is used to create directories

as instructed I first create a directory called `/tmp/pwn` and then change directory `cd /tmp/pwn` before creating a file called college using `touch college`
finally executing `/challenge/run`
```bash
root@DESKTOP-MPJ395R:~# ssh -i ./key hacker@dojo.pwn.college
Connected!
hacker@commands~making-directories:~$ mkdir /tmp/pwn
hacker@commands~making-directories:~$ cd /tmp/pwn
hacker@commands~making-directories:/tmp/pwn$ touch college
hacker@commands~making-directories:/tmp/pwn$ /challenge/run
Success! Here is your flag:
pwn.college{U2KIikRnkTpltiKfyxSBF1mdCQa.dFzM4QDLzgTN0czW}
hacker@commands~making-directories:/tmp/pwn$
```
