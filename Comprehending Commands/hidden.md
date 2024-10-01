# hidden files

Here we are introduced to the concept of hidden files, files that start with `.`

Steps:
- I start by changing the directory to `/` using `cd /`
- I list all files(including hidden ones) using `ls -a`
- I view the contents of the flag using `cat .flag-10939540922445` retrieving the flag

```bash
root@DESKTOP-MPJ395R:~# ssh -i ./key hacker@dojo.pwn.college
Connected!
hacker@commands~hidden-files:~$ cd /
hacker@commands~hidden-files:/$ ls -a
.   .dockerenv            bin   challenge  etc   lib    lib64   media  nix  proc  run   srv  tmp  var
..  .flag-10939540922445  boot  dev        home  lib32  libx32  mnt    opt  root  sbin  sys  usr
hacker@commands~hidden-files:/$ cat .flag-10939540922445
pwn.college{IfjXQ26HGy9QCaE4C8DUDYQN6pX.dBTN4QDLzgTN0czW}
```

Note: These hidden files are called dotfiles and are usually used for config files
