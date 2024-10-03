# File Globbing with *
## Introduction
File Globbing allows users to reference files without having to type the complete path, in this problem we explore using `*`, which matches any files that match the pattern
## Approach
- The Problem specifies that arguments should not exceed 4 characters, knowing that I use `cd /c*` to cd into `/challenge` , as `/c*` here matches with `/challenge`
- now since I want to run the command `run` I execute `./r*` which matches with `run`
## Code
```bash
hacker@globbing~matching-with-:/challenge$ cd /c*
hacker@globbing~matching-with-:/challenge$ ./r*
You ran me with the working directory of /challenge! Here is your flag:
pwn.college{QnaL3s1GmKuhqxQpAUPk7Cp1_hA.dFjM4QDLzgTN0czW}
```
