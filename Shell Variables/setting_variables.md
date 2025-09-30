# SETTING VARIABLES
In this challenge I have to set a variable to a particular value.

## My solve
**Flag:** `pwn.college{EUm0biLdwgKjYhDfrVJ647B--oR.QX5UTN0wiN4EzNzEzW}`

It was mentioned in the problem statement that I have to set the PWN variable to the value COLLEGE. I used PWN=COLLEGE.
```bash
hacker@variables~setting-variables:~$ PWN=COLLEGE
You've set the PWN variable properly! As promised, here is the flag:
pwn.college{EUm0biLdwgKjYhDfrVJ647B--oR.QX5UTN0wiN4EzNzEzW}
```

## What I learned
Through this challenge I learnt that:
- Value can be assigned to a variable using =
- If you put spaces (e.g., VAR = 1337), the shell won't recognize a variable assignment and will, instead, try to run the VAR command (which does not exist).
- This uses VAR and not $VAR: the $ is only prepended to access variables.


## References
No references used.

