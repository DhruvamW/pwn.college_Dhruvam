# MULTI WORD VARIABLES
In this challenge I have to assign a multi word value to my variable.

## My solve
**Flag:** `pwn.college{Ic8mFtZk5JXsH1yiFnHCf12Be5h.QXwYTN0wiN4EzNzEzW}`

It was mentioned in the problem statement that I have to set the variable PWN to COLLEGE YEAH. I used PWN='COLLEGE YEAH'.
```bash
hacker@variables~multi-word-variables:~$ PWN='COLLEGE YEAH'
You've set the PWN variable properly! As promised, here is the flag:
pwn.college{Ic8mFtZk5JXsH1yiFnHCf12Be5h.QXwYTN0wiN4EzNzEzW}
```

## What I learned
Through this challenge I learnt that: 
- When the shell sees a space, it ends the variable assignment and interprets the next word as a command
- To set a variable to multiple words we need to quote them.

## References
No references used.

