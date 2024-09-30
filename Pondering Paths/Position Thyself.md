# Position Thyself

This Problem Introduces the `cd` command(Change Directory), allowing users to pass paths as arguments

- in this problem I start off by determining my current position by using `~`
- I then follow it by using the `/challenge/run` command to figure out the target destination, which is `/etc/apt/sources.list.d`
- I utilize the `cd` command to reach this directory, finishing it off by rerunning `/challege/run`
```bash
root@DESKTOP-MPJ395R:~# ssh -i ./key hacker@dojo.pwn.college
Connected!
hacker@paths~position-thy-self:~$ ~
ssh-entrypoint: /home/hacker: Is a directory
hacker@paths~position-thy-self:~$ /challenge/run
Incorrect...
You are not currently in the /etc/apt/sources.list.d directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~position-thy-self:~$ cd /etc
hacker@paths~position-thy-self:/etc$ cd apt
hacker@paths~position-thy-self:/etc/apt$ cd sources.list.d
hacker@paths~position-thy-self:/etc/apt/sources.list.d$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{A2Dp7-Q-ay1-96GqbfNrOJX8a77.dZDN1QDLzgTN0czW}
hacker@paths~position-thy-self:/etc/apt/sources.list.d$
```
