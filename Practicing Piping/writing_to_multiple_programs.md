# writing to multiple programs
## introduction
This Program introduces process substitution allowing us, to directly send stuff from stdout or stderr to the stdin of a program, the general syntax is `>(program)`
## approach
- first we hook up a pipe to `/challenge/the` stdin using path substitution
- this pipe is t splitted into `/challenge/planet` directly as an argument
- now we have `/challenge/hack` write its stdout through the pipes
- the overall command is `/challenge/hack | tee >(/challenge/the) | /challenge/planet`
## code
```bash
root@DESKTOP-MPJ395R:~# ssh -i ./key hacker@dojo.pwn.college
Connected!
hacker@piping~writing-to-multiple-programs:~$ /challenge/hack | tee >(/challenge/the) | /challenge/planet
Congratulations, you have duplicated data into the input of two programs! Here
is your flag:
pwn.college{Ae2CSNZ9KT5mDWENsPh7LsX3K0h.dBDO0UDLzgTN0czW}
hacker@piping~writing-to-multiple-programs:~$
```
