# more catting practice
Similar to the Last Problem we have to use an absolute path as an argument for the `cat` command
however we are forbidden from using the cd command, and hence have to give the whole absolute path as an argument, as the program is deep within a couple of directories

I solve this by using the path `/opt/binaryninja/signatures/flag` as the path, invoking `cat /opt/binaryninja/signatures/flag`

```bash
root@DESKTOP-MPJ395R:~# ssh -i ./key hacker@dojo.pwn.college
Connected!
You cannot use the 'cd' command in this level, and must retrieve the flag by
absolute path. Plus, I hid the flag in a different directory! You can find it
in the file /opt/binaryninja/signatures/flag. Go cat it out **without** cding
into that directory!
hacker@commands~more-catting-practice:~$
```
