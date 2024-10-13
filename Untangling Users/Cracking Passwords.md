# Cracking Passwords
## Introduction
In this problem we attempt to use the `john` command to get the password for the zardus user
## Approach
- I start by running `john /challenge/shadow-leak` to crack the password for zardus
- the password after decrypting turns out to be aardvark
- then I run `su zardus` to switch to the zardus user profile, with aardvark as the password
- I run `/challenge/run` to get the flag
## Code
```bash
Connected!
hacker@users~cracking-passwords:~$ john /challenge/shadow-leak
Loaded 1 password hash (crypt, generic crypt(3) [?/64])
Press 'q' or Ctrl-C to abort, almost any other key for status
aardvark         (zardus)
1g 0:00:00:20 100% 2/3 0.04835g/s 281.5p/s 281.5c/s 281.5C/s Johnson..buzz
Use the "--show" option to display all of the cracked passwords reliably
Session completed
hacker@users~cracking-passwords:~$ su zardus
Password:
zardus@users~cracking-passwords:/home/hacker$ /challenge/run
Congratulations, you have become Zardus! Here is your flag:
pwn.college{0AR5vLxi_mdWBJBlttTNQEoQZ7H.ddTN0UDLzgTN0czW}
```
Note:
John the Ripper is an Open Source software meant for password recovery which is also used for password cracking due to its extensive cipher cracking abilities
