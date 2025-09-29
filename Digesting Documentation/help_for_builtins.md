# HELP FOR BUILTINS
In this challenge I have to see what a builtin command does and figure out ow to get the flag.

## My solve
**Flag:** `pwn.college{8MwvtkBbENfTtOs6DnMO1eCnsOS.QX0ETO0wiN4EzNzEzW}`

It was mentioned in the problem statement that I have to read the manual of a builtin command 'challenge' using the help command and challenge as an argument. Then I got the secret value in the manual that helped me get the flag.
```bash
hacker@man~help-for-builtins:~$ help challenge
challenge: challenge [--fortune] [--version] [--secret SECRET]
    This builtin command will read you the flag, given the right arguments!

    Options:
      --fortune         display a fortune
      --version         display the version
      --secret VALUE    prints the flag, if VALUE is correct

    You must be sure to provide the right value to --secret. That value
    is "8MwvtkBb".
hacker@man~help-for-builtins:~$ challenge --secret 8MwvtkBb
Correct! Here is your flag!
pwn.college{8MwvtkBbENfTtOs6DnMO1eCnsOS.QX0ETO0wiN4EzNzEzW}
```

## What I learned
Through this challenge I learnt that some commands, rather than being programs with man pages and help options, are built into the shell itself. These are called builtins. Builtins are invoked just like commands, but the shell handles them internally instead of launching other programs. We can get help on a specific one by passing it to the help builtin.
## References 
No references used.

