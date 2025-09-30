# EXPORTING VARIABLES
In this challenge I have to export one variable and not export the other.

## My solve
**Flag:** `pwn.college{gL2f2ATHb5KGibYkNg7EzSKQ1fG.QXyYTN0wiN4EzNzEzW}`

It was mentioned in the problem statement that I have to set the variable PWN to COLLEGE and export it and set the varibale COLLEGE to PWN and not export it.
```bash
hacker@variables~exporting-variables:~$ export PWN=COLLEGE
You've set the PWN variable to the proper value!
hacker@variables~exporting-variables:~$ COLLEGE=PWN
You've set the PWN variable to the proper value!
You've set the COLLEGE variable to the proper value!
hacker@variables~exporting-variables:~$ /challenge/run
CORRECT!
You have exported PWN=COLLEGE and set, but not exported, COLLEGE=PWN. Great 
job! Here is your flag:
pwn.college{gL2f2ATHb5KGibYkNg7EzSKQ1fG.QXyYTN0wiN4EzNzEzW}
You've set the PWN variable to the proper value!
You've set the COLLEGE variable to the proper value!
```

## What I learned
Through this challenge I learnt that: 
- The $ prompt is the prompt of sh, a minimal shell implementation that is invoked as a child of the main shell process.
- When you export your variables, they are passed into the environment variables of child processes.
- You export variables using export command and the variable name as an argument to that.

## References
No references used.

