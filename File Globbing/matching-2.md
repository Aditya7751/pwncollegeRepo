# matching with ?

## introduction
This Problem Further Introduces the `?` character for globbing, it acts as a single character wildcard
## Approach
- As Problem Suggests I first cd into `/challenge` by using `/?ha??enge` with all the characters mentioned to be omitted are covered by the wildcards
- I use `./run` to retrieve the flag

## Code
```bash
Connected!
This challenge resets your working directory to /home/hacker unless you change
directory properly...
hacker@globbing~matching-with-:~$ cd /?ha??enge
hacker@globbing~matching-with-:/challenge$ ./run
You ran me with the working directory of /challenge! Here is your flag:
pwn.college{8LHweJyp7SsNcSeS-aQuP2npMw9.dJjM4QDLzgTN0czW}
```
