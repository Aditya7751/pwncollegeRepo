# Your First Shell Script
## Introduction
One alternative to chaining commands straightaway into the terminal, is using shell scripts, files that can contain these commands, and run them on execution
## Approach
- First I use nano to create the `x.sh` file using `nano x.sh`
- I use the `#!/bin/bash` to specify it is a shell script
- Similar to the last problem I write `/challenge/pwn;/challenge/college` chaining these two commands
- I exit and then run this script using `bash x.sh`
## Code
### x.sh script
```bash
#!/bin/bash
/challenge/pwn;/challenge/college
```
### challenge terminal
```bash
Connected!
hacker@chaining~your-first-shell-script:~$ nano x.sh
hacker@chaining~your-first-shell-script:~$ bash x.sh
Great job, you've written your first shell script! Here is the flag:
pwn.college{cyatI9hWjXpT9hEy21xm5bMGl37.dFzN4QDLzgTN0czW}
```
## Additional Reading
- https://linuxize.com/post/how-to-use-nano-text-editor/
- https://www.geeksforgeeks.org/nano-text-editor-in-linux/
