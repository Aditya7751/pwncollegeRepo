# Level 10
## Approach
I pipe the output `cat data.txt` into `base64 -d`

`base64 -d` decodes encrypted text into plaintext
## Code
```bash
bandit10@bandit:~$ cat data.txt | base64 -d
The password is dtR173fZKb0RRsDFSGsg2RWnpNVj3qRr
```
