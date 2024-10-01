# explicit relative path from /
This Problem is quite similar to the Last one, except for the fact that it requires us to use an explicit relative path like `./challenge/run` instead of an implicit
one like `challenge/run` where cwd(current working directory) is `/`

To Start Off:
- I execute `cd /` to switch to the `/` or root directory
- I run `./challenge/run` as stated in the problem's description

```bash
  root@DESKTOP-MPJ395R:~# ssh -i ./key hacker@dojo.pwn.college
Connected!
hacker@paths~explicit-relative-paths-from-:~$ cd /
hacker@paths~explicit-relative-paths-from-:/$ ./challenge/run
Correct!!!
./challenge/run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{EIRNyKqglDu6q_qOEejkdB3gJRU.dBTN1QDLzgTN0czW}
```
