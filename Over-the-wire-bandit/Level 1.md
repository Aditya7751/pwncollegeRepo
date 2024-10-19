# Level 1
## Approach
In this one I first tried reading `-` directly, but after a few failed attempts I figured that you had to pipe `-` as input
## Code
```bash
bandit1@bandit:~$ cat readme
cat: readme: No such file or directory
bandit1@bandit:~$ ls
-
bandit1@bandit:~$ cd ./-
-bash: cd: ./-: Not a directory
bandit1@bandit:~$ cd /-
-bash: cd: /-: No such file or directory
bandit1@bandit:~$ cat < -
263JGJPfgU6LtdEvgfWU1XP5yac29mFx
```
## Reading Material
- https://stackoverflow.com/questions/47140193/linux-cat-inline-file-with-special-characters
