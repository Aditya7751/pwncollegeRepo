# Grepping Live Error
## Introduction
This Problem also has us grepping for the flag, however the last problem had a intermediate step where we redirected the output to `/tmp/data.txt`, this one introduces the pipe operator `|` which can be conceptualized as very similar to an actual plumbing pipe(the `tee` command also helps prove this), but the problem wants us to redirect the output of `/challenge/run` to the grep argument through pipes
## Approach
- `/challenge/run |` effectively pipes whatever the output of the program is to `grep pwn.college` as an argument
## Code
```bash
Connected!
hacker@piping~grepping-live-output:~$ /challenge/run | grep pwn.college
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge checks for a specific process at the other end of stdout : grep
[INFO] - the challenge will output a reward file if all the tests pass : /challenge/.data.txt

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /challenge/.data.txt file.

[TEST] You should have redirected my stdout to another process. Checking...
[TEST] Performing checks on that process!

[INFO] The process' executable is /nix/store/xpq4yhadyhazkcsggmqd7rsgvxb3kjy4-gnugrep-3.11/bin/grep.
[INFO] This might be different than expected because of symbolic links (for example, from /usr/bin/python to /usr/bin/python3 to /usr/bin/python3.8).
[INFO] To pass the checks, the executable must be grep.

[PASS] You have passed the checks on the process on the other end of my stdout!
[PASS] Success! You have satisfied all execution requirements.
pwn.college{0D7VtydG8XcoP-plxYs2tTE_Oux.dlTM4QDLzgTN0czW}
```
