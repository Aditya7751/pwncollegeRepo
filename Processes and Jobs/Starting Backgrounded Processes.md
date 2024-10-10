# Starting Backgrounded Processes
## Introduction
Till now we only backgrounded processes by suspending them first, but it is possible to background it straight away by appending `&` after the command
## Approach
- I run `/challenge/run &` to start `/challenge/run` in the background
## Code
```bash
Connected!
hacker@processes~starting-backgrounded-processes:~$ /challenge/run &
[1] 82
hacker@processes~starting-backgrounded-processes:~$


Yay, you started me in the background! Because of that, this text will probably
overlap weirdly with the shell prompt, but you're used to that by now...

Anyways! Here is your flag!
pwn.college{QxlN8jJYqZcoO-JI52BuH2bXR4W.dlDN4QDLzgTN0czW}
```
