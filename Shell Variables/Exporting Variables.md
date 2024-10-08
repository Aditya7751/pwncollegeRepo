# Exporting Variables
## Introduction
Exporting Variables is essential when you want to use them in another shell process, because variables by themselves are set to a local scope by default
## Approach
- As the Problem I started by assigning `PWN=COLLEGE`
- Then I proceeded to assign `COLLEGE=PWN`
- the problem made it pretty clear I only had to export the `PWN` variable, so I executed `export PWN`
- finally to retrieve the flag `/challenge/run` after all the conditions were met
## Code
```bash
Connected!
hacker@variables~exporting-variables:~$ PWN=COLLEGE
You've set the PWN variable to the proper value!
hacker@variables~exporting-variables:~$ COLLEGE=PWN
You've set the PWN variable to the proper value!
You've set the COLLEGE variable to the proper value!
hacker@variables~exporting-variables:~$ export PWN
You've set the PWN variable to the proper value!
You've set the COLLEGE variable to the proper value!
hacker@variables~exporting-variables:~$ /challenge/run
CORRECT!
You have exported PWN=COLLEGE and set, but not exported, COLLEGE=PWN. Great
job! Here is your flag:
pwn.college{Ur_f6phlAiP-0HqNd9Aa1Hm6KOA.dJjN1QDLzgTN0czW}
You've set the PWN variable to the proper value!
You've set the COLLEGE variable to the proper value!
```
