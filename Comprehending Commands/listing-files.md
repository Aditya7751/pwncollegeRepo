# listing files

In this problem we are introduced to the ls command, which lists all the contents of the current working directory we are in

To Start Off:
- I invoke `ls /challenge` to find all the contents present in the `challenge` directory
- I figure out `run` is renamed to `27583-renamed-run-22148`, noting that as my path
- Finally I wrap it all up invoking `/challenge/27583-renamed-run-22148` getting the flag in the process

```bash
root@DESKTOP-MPJ395R:~# ssh -i ./key hacker@dojo.pwn.college
Connected!
hacker@commands~listing-files:~$ ls /challenge
27583-renamed-run-22148  DESCRIPTION.md
hacker@commands~listing-files:~$ /challenge/27583-renamed-run-22148
Yahaha, you found me! Here is your flag:
pwn.college{AZ_H_fue3MDRrZMz7ZOrCE48KNp.dhjM4QDLzgTN0czW}
```
