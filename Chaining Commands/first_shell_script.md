# YOUR FIRST SHELL SCRIPT
In this challenge I have to two commands in a shell script.

## My solve
**Flag:** `pwn.college{YWlBU_VJUxzZeBPVvtvv-LfW_7w.0lM0MDOxwiN4EzNzEzW}`

It was mentioned in the problem statement that I have to run /challenge/pwn and then /challenge/college, but this time in a shell script called x.sh, then run it with bash. I first made x.sh read the input through stdin using cat >. Then I ran x.sh shell script with bash. 
```bash
hacker@chaining~your-first-shell-script:~$ cat > x.sh
/challenge/pwn
/challenge/college
^C
hacker@chaining~your-first-shell-script:~$ bash x.sh
Great job, you've written your first shell script! Here is the flag:
pwn.college{0MzdaTtrO4ujeKgVkVMdtKYRfL7.QXxcDO0wiN4EzNzEzW}
```

## What I learned
Through this challenge I learnt that:
- we can put commands in a file, called a shell script, and run them by executing the file
- by convention, shell scripts are frequently named with a sh suffix
-  And then we can execute by passing it as an argument to a new instance of our shell (bash)

## References
No references used.

