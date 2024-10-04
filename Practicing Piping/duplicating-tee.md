# Duplicating Piped Data with tee 
## Introduction
This problem introduces the `tee` command, which allows us to parallelize how output moves through pipes(think t splitting pipe connectors), this is very insightful when debugging
## Approach
- after reading the example and seeing how the tee command works, I use a dummy file `output` to store the debug info
- on reading `output` using `cat output` I realize `/challenge/pwn` needs a secret argument to pass properly
- I execute `/challenge/pwn --secret "4tfLWu_k" | /challenge/college` to retrieve the flag
## Code
```bash
hacker@piping~duplicating-piped-data-with-tee:~$ /challenge/pwn |tee output | /challenge/college
Processing...
WARNING: you are overwriting file output with tee's output...
The input to 'college' does not contain the correct secret code! This code
should be provided by the 'pwn' command. HINT: use 'tee' to intercept the
output of 'pwn' and figure out what the code needs to be.
hacker@piping~duplicating-piped-data-with-tee:~$ cat output
Usage: /challenge/pwn --secret [SECRET_ARG]

SECRET_ARG should be "4tfLWu_k"
hacker@piping~duplicating-piped-data-with-tee:~$ /challenge/pwn --secret "4tfLWu_k"
Processing...
You must pipe the output of /challenge/pwn into /challenge/college (or 'tee'
for debugging).
hacker@piping~duplicating-piped-data-with-tee:~$ /challenge/pwn --secret "4tfLWu_k" | /challenge/college
Processing...
Correct! Passing secret value to /challenge/college...
Great job! Here is your flag:
pwn.college{4tfLWu_k7adZwApNrJqngrg7-GO.dFjM5QDLzgTN0czW}
```
