# Position yet elsewhere

# Position Elsewhere

This Problem has very Similar Motifs to `Postion Thyself` and `Position Elsewhere`, using a similar approach I followed these steps:

- in this problem I start off by determining my current position by using `~`
- I then follow it by using the `/challenge/run` command to figure out the target destination, which is `/etc/apt/sources.list.d`
- I utilize the `cd` command to reach this directory, finishing it off by rerunning `/challege/run`




```bash
root@DESKTOP-MPJ395R:~# ssh -i ./key hacker@dojo.pwn.college
Connected!
hacker@paths~position-yet-elsewhere:~$ ~
ssh-entrypoint: /home/hacker: Is a directory
hacker@paths~position-yet-elsewhere:~$ /challenge/run
Incorrect...
You are not currently in the /etc/apt/sources.list.d directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~position-yet-elsewhere:~$ cd /etc
hacker@paths~position-yet-elsewhere:/etc$ cd apt
hacker@paths~position-yet-elsewhere:/etc/apt$ cd sources.list.d
hacker@paths~position-yet-elsewhere:/etc/apt/sources.list.d$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{4PUbGklppW9LvFv4MmYulLm-fU6.dhDN1QDLzgTN0czW}
```
