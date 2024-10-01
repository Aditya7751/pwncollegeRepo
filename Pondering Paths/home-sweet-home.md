# Home Sweet Home

This Problem explains how the `~` operator essentially returns an absolute path, in this case `/home/hacker`\

The Problem instructs us to run `/challenge/run` using argument that needs to meet a few constraints
> - Your argument must be an absolute path.
> - The path must be inside your home directory.
> - Before expansion, your argument must be three characters or less.

in lieu of these instructions and the previous discussion, I tried using the absolute path ~/~ as an argument since it would expand to /home/hacker/~

```bash
root@DESKTOP-MPJ395R:~# ssh -i ./key hacker@dojo.pwn.college
Connected!
hacker@paths~home-sweet-home:~$ /challenge/run ~/~
Writing the file to /home/hacker/~!
... and reading it back to you:
pwn.college{EnL8zEBLIz5ul1JA8nVXye5_5YU.dNzM4QDLzgTN0czW}
hacker@paths~home-sweet-home:~$
```
