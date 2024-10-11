# Changing File Ownership
## Introduction
This Module deals with handling permissions, this specific problem deals with ownership of files
## Approach
- I change the owner of `/flag` to the `hacker` user using `chown hacker /flag`
- I read the flag using `cat /flag`
## Code
```bash
Connected!
hacker@permissions~changing-file-ownership:~$ chown hacker /flag
hacker@permissions~changing-file-ownership:~$ cat /flag
pwn.college{Ypzw1zUpj2vuh-SDHCR6cHnmGXa.dFTM2QDLzgTN0czW}
```
