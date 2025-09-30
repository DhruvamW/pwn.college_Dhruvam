# MIXING GLOBS
In this challenge I have to reference multiple files using multiple globs in a single command.

## My solve
**Flag:** `pwn.college{YsvS9V_byXk1VD71U9VhHmuJTno.QX1IDO0wiN4EzNzEzW}`

It was mentioned in the problem statement that I have to provide a single argument to /challenge/run which is 6 characters using * and [] globs in it that will match the files "challenging", "educational", and "pwning".
```bash
hacker@globbing~mixing-globs:~$ cd /challenge/files
hacker@globbing~mixing-globs:/challenge/files$ /challenge/run [cep]*
You got it! Here is your flag!
pwn.college{YsvS9V_byXk1VD71U9VhHmuJTno.QX1IDO0wiN4EzNzEzW}
```

## What I learned
Through this challenge I learnt we can mix globs and use them together in a single command.

## References
No references used.

