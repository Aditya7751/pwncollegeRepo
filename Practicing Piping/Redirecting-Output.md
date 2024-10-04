# Redirecting Output
## Introduction
Piping is a feature that allows users to redirect input,output and errors to be used as input/output for other programs, this problem explores redirecting output
## Approach
- As Suggested in the Problem I used `echo PWN` that would return `PWN` and redirected it to `COLLEGE` by running `echo PWN > COLLEGE`
## Code
```bash
You have created the COLLEGE file and wrote the right value to it, but it
doesn't look like you did it via input redirection.
hacker@piping~redirecting-output:~$ echo PWN > COLLEGE
Correct! You successfully redirected 'PWN' to the file 'COLLEGE'! Here is your
flag:
pwn.college{4XCFKQ5sBNdL4NRsHWEaHLyb3YF.dRjN1QDLzgTN0czW}
```
