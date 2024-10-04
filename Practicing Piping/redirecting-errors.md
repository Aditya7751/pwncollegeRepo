# Redirecting Errors
## Introduction
Instead of dealing with stdout like previous problems, this one deals with stderr, although the approach stays pretty similar to previous problems
## Approach
- As Suggested in the problem I use the `2>` operator to move along the stderr ,
- initally I tried giving arguments seperately , but that didnt work so I just put them in one argument `/challenge/run > myflag 2> instructions`
- I proceed to print the flag using `cat myflag`
## Code
```bash
Connected!
hacker@piping~redirecting-errors:~$ /challenge/run 2> instructions
hacker@piping~redirecting-errors:~$ /challenge/run > myflag
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge will check that output is redirected to a specific file path : myflag
[INFO] - the challenge will check that error output is redirected to a specific file path : instructions
[INFO] - the challenge will output a reward file if all the tests pass : /flag

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /flag file.

[TEST] You should have redirected my stdout to a file called myflag. Checking...

[PASS] The file at the other end of my stdout looks okay!

[TEST] You should have redirected my stderr to instructions. Checking...

[FAIL] You did not satisfy all the execution requirements.
[FAIL] Specifically, you must fix the following issue:
[FAIL]   You have not redirected anything for this process' stderr.
hacker@piping~redirecting-errors:~$ /challenge/run > myflag 2> instructions
hacker@piping~redirecting-errors:~$ cat myflag

[FLAG] Here is your flag:
[FLAG] pwn.college{IkpkmVehCZoshS-CdRLDKvdMvjB.ddjN1QDLzgTN0czW}
```
