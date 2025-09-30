# STORING COMMAND OUTPUT
In this challenge I have to store the output of a command in a variable.

## My solve
**Flag:** `pwn.college{EUm0biLdwgKjYhDfrVJ647B--oR.QX5UTN0wiN4EzNzEzW}`

It was mentioned in the problem statement that I have to store the output of the /challenge/run command directly into a variable called PWN, and it will contain the flag.
```bash
hacker@variables~storing-command-output:~$ PWN=$(/challenge/run)
Congratulations! You have read the flag into the PWN variable. Now print it out 
and submit it!
hacker@variables~storing-command-output:~$ echo $PWN
pwn.college{A3NwUoyYoYD4hTCnsE9W3lIz2La.QX1cDN1wiN4EzNzEzW}
```

## What I learned
Through this challenge I learnt that:
- You can store the output of some command into a variable using Command Substitution.
- example: FLAG=$(cat /flag)


## References
No references used.

