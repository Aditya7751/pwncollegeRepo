# Helpful Programs
## introduction
A lot of commands might not have `man` pages, but these usually come with some argument along the lines of `--help`, that tell you how to run them
## approach
- I start by `/challenge/challenge --help` as instructed in the program
- I follow it with `/challenge/challenge -p` as that gives me the value for `-g`
- lastly, I use `/challenge/challenge -g 124` to retrieve the key
## code
```bash
root@DESKTOP-MPJ395R:~# ssh -i ./key hacker@dojo.pwn.college
Connected!
hacker@man~helpful-programs:~$ /challenge/challenge --help
usage: a challenge to make you ask for help [-h] [--fortune] [-v] [-g GIVE_THE_FLAG] [-p]

optional arguments:
  -h, --help            show this help message and exit
  --fortune             read your fortune
  -v, --version         get the version number
  -g GIVE_THE_FLAG, --give-the-flag GIVE_THE_FLAG
                        get the flag, if given the correct value
  -p, --print-value     print the value that will cause the -g option to give you the flag
hacker@man~helpful-programs:~$ /challenge/challenge -p
The secret value is: 124
hacker@man~helpful-programs:~$ /challenge/challenge -g 124
Correct usage! Your flag: pwn.college{IYUK1HFY2bwFqYJSFOUaJ-b4ur5.ddjM4QDLzgTN0czW}
```
