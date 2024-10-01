# implicit relative path from /

While The Last Few Problems focused on using absolute paths, this one relies on us using an implicit relative path `challenge/run` rather than `/challenge/run`

To Start Off:

*I started by using `~` to find out my current location
*I ran `/challenge/run` to get information about the target directory
*I used `cd /` to switch to the `/` or root directory
*executed `challenge/run` to find the flag

```bash
root@DESKTOP-MPJ395R:~# ssh -i ./key hacker@dojo.pwn.college
Connected!
hacker@paths~implicit-relative-paths-from-:~$ ~
ssh-entrypoint: /home/hacker: Is a directory
hacker@paths~implicit-relative-paths-from-:~$ /challenge/run
Incorrect...
You are not currently in the / directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~implicit-relative-paths-from-:~$ cd /
hacker@paths~implicit-relative-paths-from-:/$ challenge/run
Correct!!!
challenge/run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{8-DDvFLqp8AfHaWg9KAvDAe1hEa.dlDN1QDLzgTN0czW}
```
Note: The Location of a Directory in the relative path is taken with reference to the cwd(current working directory), so on running `challenge/run`
it is essentially the same as writing `/challenge/run` when the cwd is `/`
