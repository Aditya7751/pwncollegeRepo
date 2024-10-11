# SUID Bit
## Introduction
Some Programs may be associated with SUID(set user id) Bits, which change the user to the owner of the file, upon execution, these can also be  safety vulnerabilities
## Approach
- I set a SUID ID by executing `chmod u+s /challenge/getroot`
- I run `/challenge/getroot` opening a root subshell in the process
- I retrieve the flag using `cat /flag`
## Code
```bash
Connected!
hacker@permissions~the-suid-bit:~$ chmod u+s /challenge/getroot
hacker@permissions~the-suid-bit:~$ /challenge/getroot
SUCCESS! You have set the suid bit on this program, and it is running as root!
Here is your shell...
root@permissions~the-suid-bit:~# cat /flag
pwn.college{ICvgIVJM5XKIyRPq1PNXHU6mVCM.dNTM2QDLzgTN0czW}
```
