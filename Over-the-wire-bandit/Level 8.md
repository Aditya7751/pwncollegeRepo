# Level 8
## Approach
first I used `sort data.txt`  as `uniq` can only identify unique elements in consecutive lines, I pipe that into `uniq -u` to find the only unique element, i.e, the password
## Code
```bash
bandit8@bandit:~$ sort data.txt | uniq -u
4CKMh1JI91bUIZZPXDqGanal4xvAg0JM
```
