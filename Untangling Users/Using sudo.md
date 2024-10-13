# Using sudo
## Introduction
While the Last few problems had us using `su`, this one focuses on the more robust `sudo` command,normally defaulting to running a command as root
## Approach
- I need to have root access to read the flag, I can accomplish this by starting my command with `sudo` knowing this I run `sudo cat /flag`
## Code
```bash
Connected!
hacker@users~using-sudo:~$ sudo cat /flag
pwn.college{8iHNEvbD4fUkg_ugWSTMBRBQM-G.dhTN0UDLzgTN0czW}
```
