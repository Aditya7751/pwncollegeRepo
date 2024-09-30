# Position Elsewhere

This Problem has very Similar Motifs to `Postion Thyself`, using a similar approach I followed these steps:

- in this problem I start off by determining my current position by using `~`
- I then follow it by using the `/challenge/run` command to figure out the target destination, which is `/usr/share/doc`
- I utilize the `cd` command to reach this directory, finishing it off by rerunning `/challege/run`




```bash
root@DESKTOP-MPJ395R:~# ssh -i ./key hacker@dojo.pwn.college
Connected!
hacker@paths~position-elsewhere:~$ ~
ssh-entrypoint: /home/hacker: Is a directory
hacker@paths~position-elsewhere:~$ /challenge/run
Incorrect...
You are not currently in the /usr/share/doc directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~position-elsewhere:~$ cd /usr
hacker@paths~position-elsewhere:/usr$ cd share
hacker@paths~position-elsewhere:/usr/share$ cd doc
hacker@paths~position-elsewhere:/usr/share/doc$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{E9SFiKSeYSUEtLrpFEAQS3cJFtp.ddDN1QDLzgTN0czW}
```
