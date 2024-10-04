# Redirecting more Output

## Introduction
This Problems builds on the concepts taught in the last one , but requires one to understand the working of the commands

## Approach

- Similarly to the Last Problem I just redirect `/challenge/run` output to `myflag` by executing `/challenge/run > myflag`
- I then read the contents of `myflag` using `cat myflag`


## Code
```bash
Connected!
hacker@piping~redirecting-more-output:~$ /challenge/run > myflag
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge will check that output is redirected to a specific file path : myflag
[INFO] - the challenge will output a reward file if all the tests pass : /flag

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /flag file.

[TEST] You should have redirected my stdout to a file called myflag. Checking...

[PASS] The file at the other end of my stdout looks okay!
[PASS] Success! You have satisfied all execution requirements.
hacker@piping~redirecting-more-output:~$ cat myflag

[FLAG] Here is your flag:
[FLAG] pwn.college{cM62ELjAgnxjoW3nP2yEFI7AQ2a.dVjN1QDLzgTN0czW}
```
