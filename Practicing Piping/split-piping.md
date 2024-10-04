# Split-piping stderr and stdout
## introduction
The crux of this problem lies within the understanding of these file descriptor operators, and also how they interact with each other
## approach
- since the stderr of `/challenge/hack` has to go to `/challenge/the` as input, I use `2>` to send stderr and `>(/challenge/the)` as the process substitution of it that takes input
- similarly the stdout of `/challenge/hack` has to go to `/challenge/planet` as input, I use `>` to send stdout and `>(/challenge/planet` as the process substitution of it that takes input
## code
```bash
Connected!
hacker@piping~split-piping-stderr-and-stdout:~$ /challenge/hack 2> >(/challenge/the) > >(/challenge/planet)
Congratulations, you have learned a redirection technique that even experts
struggle with! Here is your flag:
pwn.college{UmUy2jHPwsMIwxMyxMzWDHE37FV.dFDNwYDLzgTN0czW}
hacker@piping~split-piping-stderr-and-stdout:~$
```
