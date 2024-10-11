# Changing Permissions 
## Introduction
In this problem, we have to change the permissions of the /flag file, and make it readable
## Approach
- I start by giving all users read permissions using `o+r /flag` roughly translating to add read permissions to others, for the file `/flag`
- I retrieve the flag using `cat /flag`
## Code
```bash
Connected!
hacker@permissions~changing-permissions:~$ chmod o+r /flag
hacker@permissions~changing-permissions:~$ cat /flag
pwn.college{M6kxyuQaPwefl78aVVJIyZ7MfsX.dNzNyUDLzgTN0czW}
```
