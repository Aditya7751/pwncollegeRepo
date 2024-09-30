# Program and absolute paths

This Problem Builds on `The Root`, However it has some added complexity, due to the fact that our program `run` is situated in another directory `/challenge`
To Solve this, We need to note that the path to `run` would be `/challenge/run`, as we Enter the `challenge` directory first from the root directory `/`, and then finally execute `run`

```bash
root@DESKTOP-MPJ395R:~# ssh -i ./key hacker@dojo.pwn.college
Connected!
hacker@paths~program-and-absolute-paths:~$ /challenge/run
Correct!!!
/challenge/run is an absolute path! Here is your flag:
pwn.college{MYdauGkoPTxHAZGjpRuTlruPDLs.dVDN1QDLzgTN0czW}
```
