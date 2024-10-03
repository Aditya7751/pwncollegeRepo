# mixing globs

## introduction
this problem ups the difficulty but having the user deal with multiple forms of globbing to get the right answer
## approach
- first I switch to the `/challenge/files` directory as the problem requires
- I guess that since the `[]` glob cycles through all the elements as single characters, and combining that with `*` would work as the perfect wildcard, so I executed `/challenge/run [cep]*`

## code
```bash
hacker@globbing~mixing-globs:~$ cd /challenge/files
hacker@globbing~mixing-globs:/challenge/files$ /challenge/run [cep]*
You got it! Here is your flag!
pwn.college{k4lTjTo6rMHkzvlEB4rRr8cb9J3.dVjM4QDLzgTN0czW}
hacker@globbing~mixing-globs:/challenge/files$
```
