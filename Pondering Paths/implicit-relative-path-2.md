# implicit relative path

This Problem requires us to run the `run` command directly from the `challenge` directory using `./run` which acts as an relative path for linux to run the program

Steps:
- I start by switching over to the `/` or root directory
- I then switch over to the `challenge directory` using `cd challenge`, as its a relative path equivalent to `/challenge`
- as the problem suggests, we have to explicitly give a path to `run` for linux to execute it, hence I execute `./run`

```bash
root@DESKTOP-MPJ395R:~# ssh -i ./key hacker@dojo.pwn.college
Connected!
hacker@paths~implicit-relative-path:~$ cd /
hacker@paths~implicit-relative-path:/$ cd challenge
hacker@paths~implicit-relative-path:/challenge$ ./run
Correct!!!
./run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{QW_rG5bzrDY2_1rKJltkFIqlSvE.dFTN1QDLzgTN0czW}
```
Note: Linux Doesnt automatically run `run` as a safety measure, as accidentally executing programs may have undesired consequences
