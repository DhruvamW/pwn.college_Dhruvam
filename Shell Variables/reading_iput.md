# READING INPUT
In this challenge I have to read the value of a variable.

## My solve
**Flag:** `pwn.college{8uk7uZ_XyO4g9WvBvFEaAy5W-0B.QX4cTN0wiN4EzNzEzW}`

It was mentioned in the problem statement that I have to use read to set the PWN variable to the value COLLEGE.
```bash
hacker@variables~reading-input:~$ read -p "INPUT: " PWN
INPUT: COLLEGE
You've set the PWN variable properly! As promised, here is the flag:
pwn.college{8uk7uZ_XyO4g9WvBvFEaAy5W-0B.QX4cTN0wiN4EzNzEzW}
```

## What I learned
Through this challenge I learnt that:
- You can read the input from user by using the read command.
- the -p argument, lets you specify a prompt.


## References
No references used.

