# Storing Command Output
## Introduction
Somewhat similarly to Process substitution, command substitution allows us to directly store a programs output in a variable
## Approach
- I first use command substitution to store `/challenge/run` output in `PWN` , executing `PWN=$(/challenge/run)`
- I print `PWN` using `echo $PWN`
## Code
```bash
Connected!
hacker@variables~storing-command-output:~$ PWN=$(/challenge/run)
Congratulations! You have read the flag into the PWN variable. Now print it out
and submit it!
hacker@variables~storing-command-output:~$ echo $PWN
pwn.college{smu0zgA-g12-2KHJUqf73lVePCP.dVzN0UDLzgTN0czW}
```
