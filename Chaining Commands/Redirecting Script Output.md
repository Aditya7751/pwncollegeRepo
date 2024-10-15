# Redirecting Script Output
## Introduction
This Problem is similar to the last one, but also combines elements from the Practicing Piping Module, with us redirecting script output to `/challenge/solve`
## Approach
- I use nano to make the script using `nano script.sh`
- the script is identical to the last problem `/challenge/pwn;/challenge/college`
- I then pipe the output of script using `bash script.sh | /challenge/solve` thereby piping it into `/challenge/solve` as an argument
## Code
### script.sh
```bash
#!bin/bash
/challenge/pwn;/challenge/college
```
### Main Terminal
```bash
Connected!
hacker@chaining~redirecting-script-output:~$ nano script.sh
hacker@chaining~redirecting-script-output:~$ bash script.sh | /challenge/solve
Correct! Here is your flag:
pwn.college{MZgbrXCH7zEgcZgdq6yvRFzGQxo.dhTM5QDLzgTN0czW}
```
