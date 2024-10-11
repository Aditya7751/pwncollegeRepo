# Groups and Files
## Introduction
While last problem had us dealing with user ownership, this one involves changing the group ownership of a file using `chgrp`(change group) which is somewhat analogous to `chown` and users
## Approach
- I check the groups id using `id`, it turns out to be 1000
- I change group ownership to group 1000 using `chgrp 1000 /flag`
- I read the flag using `cat /flag`
## Code
```bash
Connected!
hacker@permissions~groups-and-files:~$ id
uid=1000(hacker) gid=1000(hacker) groups=1000(hacker)
hacker@permissions~groups-and-files:~$ chgrp 1000 /flag
hacker@permissions~groups-and-files:~$ cat /flag
pwn.college{gQfvPK3P0f21YsCRHRI0Nt4gAib.dFzNyUDLzgTN0czW}
```
