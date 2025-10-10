# READING SHELL SCRIPTS
In this challenge I have to read a script and figure out the password.

## My solve
**Flag:** `pwn.college{cQYGqLPZB_Ie2zl1fy1CFHxaso0.0lMwgDOxwiN4EzNzEzW}`

It was mentioned in the problem statement that I have to  read the script /challenge/run (using, say, cat), figure out the password, and get the flag.
```bash
hacker@chaining~reading-shell-scripts:~$ cat /challenge/run
#!/opt/pwn.college/bash

read GUESS
if [ "$GUESS" == "hack the PLANET" ]
then
        echo "CORRECT! Your flag:"
        cat /flag
else
        echo "Read the /challenge/run file to figure out the correct password!"
fi
hacker@chaining~reading-shell-scripts:~$ /challenge/run
hack the PLANET
CORRECT! Your flag:
pwn.college{cQYGqLPZB_Ie2zl1fy1CFHxaso0.0lMwgDOxwiN4EzNzEzW}
```

## What I learned
Through this challenge I learnt that:
-  scripts are very handy for doing simple "system-level" tasks, and are a common tool that developers and sysadmins reach for.
- In fact, a surprising fraction of the programs on a typical Linux machine are shell scripts.


## References
No references used.

