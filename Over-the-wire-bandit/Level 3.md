# Level 3
## Approach
I use `ls` to see the contents of the home directory, using `cd` to get into `inhere`, I use `ls` again but see nothing, guessing it must be hidden files, I use `ls -a` to see hidden files
## Code
```bash
bandit3@bandit:~$ ls
inhere
bandit3@bandit:~$ cd inhere
bandit3@bandit:~/inhere$ ls
bandit3@bandit:~/inhere$ ls -a
.  ..  ...Hiding-From-You
bandit3@bandit:~/inhere$ cat ...Hiding-From-You
2WmrDFRmJIq3IPxneAaMGhap0pFhF3NJ
```
