# reading manuals

## introduction
This Problem introduces the `man` command, short for manual, it is used to display the manual for any command that is given to it as an argument(granted it has a manual page for said command)
## approach
- I start off by using `man challenge` as instructed in the problem
- in the manual I notice the --ircssv argument, that also has the number needed for it to return the flag
- I run `/challenge/challenge --ircssv 401 ` to retrieve the flag
## code
```bash
root@DESKTOP-MPJ395R:~# ssh -i ./key hacker@dojo.pwn.college
Connected!
hacker@man~reading-manuals:~$ man challenge

CHALLENGE(1)                                      Challenge Commands                                     CHALLENGE(1)

NAME
       /challenge/challenge - print the flag!

SYNOPSIS
       challenge OPTION

DESCRIPTION
       Output the flag when called with the right arguments.

       --fortune
              read a fortune

       --version
              output version information and exit

       --ircssv NUM
              print the flag if NUM is 401

AUTHOR
       Written by Zardus.

REPORTING BUGS
       The repository for this dojo: <https://github.com/pwncollege/linux-luminarium/>

SEE ALSO
       man(1) bash-builtins(7)

pwn.college                                            May 2024                                          CHALLENGE(1)
hacker@man~reading-manuals:~$ /challenge/challenge --ircssv 401
Correct usage! Your flag: pwn.college{UWi-rcsJsOvxEYvkGPySqhinQuE.dRTM4QDLzgTN0czW}
hacker@man~reading-manuals:~$
```
