# catting absolute paths

Similarly to the Last Problem we have to use the `cat` command to view the contents of the flag,however this time we are instructed to use the absolute path of `/flag` as an argument 

As instructed I execute `cat /flag` to get the flag

```bash
root@DESKTOP-MPJ395R:~# ssh -i ./key hacker@dojo.pwn.college
Connected!
hacker@commands~catting-absolute-paths:~$ cat /flag
pwn.college{MSUDEE2hvBXAzO8iMfCg7TwIudf.dlTM5QDLzgTN0czW}
```
