# PRINTING VARIABLES
In this challenge I have to have my shell print out a variable.

## My solve
**Flag:** `pwn.college{QIdauQbKwrTIsA47YTtJ9yqMZCY.QX3UTN0wiN4EzNzEzW}`

It was mentioned in the problem statement that I have to have my shell print out the FLAG variable. For this I used echo $FLAG which in turn gave me the flag.
```bash
hacker@variables~printing-variables:~$ /challenge/run
You cannot solve this challenge using /challenge/run.
However, the flag is already in the FLAG variable in your shell.
Print it out!
hacker@variables~printing-variables:~$ echo $FLAG
pwn.college{QIdauQbKwrTIsA47YTtJ9yqMZCY.QX3UTN0wiN4EzNzEzW}
```

## What I learned
Through this challenge I learnt that:
- The Linux command line interface is actually a sophisticated programming language with which you can write actual programs.
- Programs written in this language are referred to as "shell scripts". 
- You can print out variables with echo, by prepending the variable name with a $.


## References
No references used.

