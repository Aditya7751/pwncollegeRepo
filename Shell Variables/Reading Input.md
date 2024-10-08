# Reading Input
## Introduction
the `read` builtin is pretty self explanatory, allowing the user to give input.
## Approach
- I execute `read -p "Enter Value:" PWN` to read input into the `PWN` Variable
- I enter `COLLEGE` as directed and retrieve the flag
## Code
```bash
Connected!
hacker@variables~reading-input:~$ read -p "Enter Value:" PWN
Enter Value:COLLEGE
You've set the PWN variable properly! As promised, here is the flag:
pwn.college{Iw91Iqm8Vp0a6clq45IzQc96sa4.dhzN1QDLzgTN0czW}
```
