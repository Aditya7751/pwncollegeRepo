# Level 9
## Approach
I use `strings data.txt` to print human readable strings only from that file, I pipe it into `grep "==="` as the hint suggests the password is preceeded by a lot of ='s
## Code
```bash
bandit9@bandit:~$ strings data.txt | grep "==="
}========== the
3JprD========== passwordi
~fDV3========== is
D9========== FGUW5ilLVJrxX9kMYMmlN4MgbpfMiqey
```
