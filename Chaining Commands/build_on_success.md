# BUILDING ON SUCCESS
In this challenge I have to chain two commands to get the flag.

## My solve
**Flag:** `pwn.college{YWlBU_VJUxzZeBPVvtvv-LfW_7w.0lM0MDOxwiN4EzNzEzW}`

It was mentioned in the problem statement that I have to to chain the programs /challenge/first-success and /challenge/second using the && operator.
```bash
hacker@chaining~building-on-success:~$ /challenge/first-success
hacker@chaining~building-on-success:~$ /challenge/second
Error: /challenge/first-success must be successfully chained with 
/challenge/second using &&
hacker@chaining~building-on-success:~$ /challenge/first-success && /challenge/second
Nice chaining! Flag: pwn.college{YWlBU_VJUxzZeBPVvtvv-LfW_7w.0lM0MDOxwiN4EzNzEzW}
```

## What I learned
Through this challenge I learnt that:
-  && operator allows you to run a second command only if the first command succeeds
- This is called the "AND" operator because both conditions must be true: the first command must succeed AND then the second command will run.

## References
No references used.

