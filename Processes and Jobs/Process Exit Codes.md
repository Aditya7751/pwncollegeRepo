# Process Exit Codes
## Introduction
Every Program executed in the shell has exit codes associated with them, they are key for debugging and error handling, with common ones like 0
indicating success and non-zero values typically representing errors of some kind
## Approach
- I run `/challenge/get-code` to get the shell to return an error code
- I read this error code using `echo $?`, which turns out to be 173 in this case
- I run `/challenge/submit-code 173` as stipulated by the problem, retrieving the flag
## Code
```bash
Connected!
hacker@processes~process-exit-codes:~$ /challenge/get-code
Exiting with an error code!
hacker@processes~process-exit-codes:~$ echo $?
173
hacker@processes~process-exit-codes:~$ /challenge/submit-code 173
CORRECT! Here is your flag:
pwn.college{guDGnk8u5wKrf860Nxm5SKjuCYD.dljN4UDLzgTN0czW}
```
