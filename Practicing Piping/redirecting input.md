# redirecting input
## Introduction
This Problem has us dealing with stdin , similar to previous problems which had us deal with stdout and stderr
## Approach
- I first have `PWN` contain `COLLEGE` in it `echo COLELGE > PWN`
- I then redirect `PWN` redirect to `/challenge/run` as input `/challenge/run < PWN`
## Code
```bash
hacker@piping~redirecting-input:~$ echo COLLEGE > PWN
hacker@piping~redirecting-input:~$ /challenge/run < PWN
Reading from standard input...
Correct! You have redirected the PWN file into my standard input, and I read
the value 'COLLEGE' out of it!
Here is your flag:
pwn.college{080Okrpb5OlFcGleRr4RZNn2hR3.dBzN1QDLzgTN0czW}
hacker@piping~redirecting-input:~$
```
