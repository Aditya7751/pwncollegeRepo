# searching manuals

## introduction
This Problem heavily relies around searching manuals, with a hidden argument in there that will meet the conditions required
## approach
- I start by opening the manual using `man challenge`
- after a lot of reading I find the argument `--zvevr`
- I executed `/challenge/challenge --zvevr` to retrieve the key
## code
```bash
hacker@man~searching-manuals:~$ man challenge
hacker@man~searching-manuals:~$
hacker@man~searching-manuals:~$ /challenge/challenge  --zvevr
Initializing...
Correct usage! Your flag: pwn.college{gqk5Z3b4-argHujy7zVDB7OH_yA.dVTM4QDLzgTN0czW}
hacker@man~searching-manuals:~$
```
