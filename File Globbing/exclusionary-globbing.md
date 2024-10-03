# exclusionary globbing
## introduction
Contrary to the previous problems in this module, this problem requires you to exclude certain files in the glob, using the `^` or `!` character
## approach
- first I `cd` into `/challenge/files` using `cd /challenge/files`
- I do the same thing as in mixing globs but replace `[pwn]` with `[^pwn]`, executing `/challenge/run [^pwn]`
## code
```bash
Connected!
hacker@globbing~exclusionary-globbing:~$ cd /challenge/files
hacker@globbing~exclusionary-globbing:/challenge/files$ /challenge/run [^pwn]*
You got it! Here is your flag!
pwn.college{EWllLTKwQ6PMFFNe3klrpskPczI.dZjM4QDLzgTN0czW}
```
