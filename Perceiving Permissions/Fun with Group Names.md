# Fun with Group Names
## Introduction
This problem is similar to the last one, but the group we are in this time is randomized, so we have to figure out which group we are in and its ID before proceeding with changing ownership
## Approach
- I use `id` to get some information about which group I may be in
- the group name grp21385 seems like it probably is the group we are in, hence 1000 will be the group id
- I execute `chgrp 1000 /flag` to change ownership of the flag to group with id 1000
- I retrieve the flag using `cat /flag`
## Code
```bash
Connected!
hacker@permissions~fun-with-groups-names:~$ id
uid=1000(hacker) gid=1000(grp21385) groups=1000(grp21385)
hacker@permissions~fun-with-groups-names:~$ chgrp 1000 /flag
hacker@permissions~fun-with-groups-names:~$ cat /flag
pwn.college{ogFcn27iqZ--FSviMWt-svjOkGe.dJzNyUDLzgTN0czW}
```
