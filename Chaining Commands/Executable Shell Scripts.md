# Executable Shell Scripts
## Introduction
In this problem, we learn of an alternative way to run a script instead of using the bash command
## Approach
- first I use `nano script.sh` to make the script as per the details of the problem, i.e, execute `/challenge/solve`
- then I give the script permissions to execute using `chmod u=rwx,g=rwx,o=rwx script.sh`
- Finally I run the script using its absolute path `/home/hacker/script.sh`
## Code
### script.sh
```bash
#!/bin/bash
/challenge/solve
```
### Main Terminal 
```bash
Connected!
hacker@chaining~executable-shell-scripts:~$ nano script.sh
hacker@chaining~executable-shell-scripts:~$ chmod u=rwx,g=rwx,o=rwx script.sh
hacker@chaining~executable-shell-scripts:~$ nano script.sh
hacker@chaining~executable-shell-scripts:~$ /home/hacker/script.sh
Congratulations on your shell script execution! Your flag:
pwn.college{cGwlqhbQoNEwv0rRwnoT-W809Xx.dRzNyUDLzgTN0czW}
```
