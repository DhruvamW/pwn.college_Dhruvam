# REDIRECTING SCRIPT OUTPUT
In this challenge I have to pipe my script to another program.

## My solve
**Flag:** `pwn.college{YeBm34p18J_ubYRZUXz-gTWAmuU.QX4ETO0wiN4EzNzEzW}`

It was mentioned in the problem statement that I have to  create a script that calls the /challenge/pwn command followed by the /challenge/college command, and pipe the output of the script into a single invocation of the /challenge/solve command. I piped the output of bash pwn.sh (my script file) to /challenge/solve using |. 
```bash
hacker@chaining~redirecting-script-output:~$ cat > pwn.sh
/challenge/pwn
/challenge/college
^C
hacker@chaining~redirecting-script-output:~$ bash pwn.sh | /challenge/solve
Correct! Here is your flag:
pwn.college{YeBm34p18J_ubYRZUXz-gTWAmuU.QX4ETO0wiN4EzNzEzW}
```

## What I learned
Through this challenge I learnt that:
- script is just another command.
- you can redirect its input and output
- All of the various redirection methods work: > for stdout, 2> for stderr, < for stdin, >> and 2>> for append-mode redirection, >& for redirecting to other file descriptors, and | for piping to another command.

## References
No references used.

