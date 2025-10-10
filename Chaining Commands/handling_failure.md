# HANDLING FAILURE
In this challenge I have to chain two commands to get the flag.

## My solve
**Flag:** `pwn.college{4vebd-X7ZuZFPL5VY9QJAn96eyf.01M0MDOxwiN4EzNzEzW}`

It was mentioned in the problem statement that I have to to chain the programs /challenge/first-FAILURE and /challenge/second using the || operator.
```bash
hacker@chaining~handling-failure:~$ /challenge/first-failure || /challenge/second
Nice chaining! Flag: pwn.college{4vebd-X7ZuZFPL5VY9QJAn96eyf.01M0MDOxwiN4EzNzEzW}
```

## What I learned
Through this challenge I learnt that:
-  the || operator allows you to run a second command only if the first command fails (exits with a non-zero code).
- This is called the "OR" operator because either the first command succeeds OR the second command will run.
- command1 || command2
- The || operator is super useful for providing fallback commands or error handling

## References
No references used.

