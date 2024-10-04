# Grepping Stored Results
## Introduction
This problem reintroduces grepping(taught in module 2), it helps us manipulate and search strings in large text file
## Approach
- First I have `/challenge/run` output redirected to `/tmp/data.txt` as the problem requires
- I then `grep` for pwn.college as that is present in all keys `grep pwn.college /tmp/data.txt`
## Code
```bash
hacker@piping~grepping-stored-results:~$ /challenge/run > /tmp/data.txt
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge will check that output is redirected to a specific file path : /tmp/data.txt
[INFO] - the challenge will output a reward file if all the tests pass : /challenge/.data.txt

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /challenge/.data.txt file.

[TEST] You should have redirected my stdout to a file called /tmp/data.txt. Checking...

[HINT] File descriptors are inherited from the parent, unless the FD_CLOEXEC is set by the parent on the file descriptor.
[HINT] For security reasons, some programs, such as python, do this by default in certain cases. Be careful if you are
[HINT] creating and trying to pass in FDs in python.

[PASS] The file at the other end of my stdout looks okay!
[PASS] Success! You have satisfied all execution requirements.
hacker@piping~grepping-stored-results:~$ grep pwn.college /tmp/data.txt
pwn.college{81NcCNzOU71MlAEXMr7o-IdP_06.dhTM4QDLzgTN0czW}
```
