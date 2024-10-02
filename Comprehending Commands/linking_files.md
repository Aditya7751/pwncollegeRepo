# linking files

This Problem Introduces the concepts of symlinking files, a file whose purpose is similar to a pointer that points to the right file

Steps:
- As the problem suggested I started off with `hacker@commands~linking-files:~$ ln -s /flag /home/hacker/not-the-flag`
- I then executed `/challenge/catflag` to retrieve the key
- I am not exactly sure why the file already exists in this case, But I tried an alternate implementation where I started with `rm ~/not-the-flag` and then create the symlink between `flag` and `~/not-the-flag` which also worked


```bash
root@DESKTOP-MPJ395R:~# ssh -i ./key hacker@dojo.pwn.college
Connected!
hacker@commands~linking-files:~$ ln -s /flag /home/hacker/not-the-flag
ln: failed to create symbolic link '/home/hacker/not-the-flag': File exists
hacker@commands~linking-files:~$ /challenge/catflag
About to read out the /home/hacker/not-the-flag file!
pwn.college{w7ktiJTZpMrVfAecV6WxPT9Zvfh.dlTM1UDLzgTN0czW}
```


## Additional Reading Material
- https://stackoverflow.com/questions/1951742/how-can-i-symlink-a-file-in-linux
