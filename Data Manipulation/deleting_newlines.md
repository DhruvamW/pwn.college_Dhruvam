# DELETING NEWLINES
In this challenge I have to delete new line characters in my flag..

## My solve
**Flag:** `Your line-split flag: pwn.college{IG47xX47cItzJ8JIkQVVzce2eub.0VNxEzNxwiN4EzNzEzW}`

It was mentioned in the problem statement that I have to remove new line (\n) characters present in the flag to get the correct flag.
``` bash
hacker@data~deleting-newlines:~$ /challenge/run | tr -d "\n"
Your line-split flag: pwn.college{IG47xX47cItzJ8JIkQVVzce2eub.0VNxEzNxwiN4EzNzEzW}
```

## What I learned
Through this challenge I learnt that:
- the backslash (\) signifies that the character that follows it is a standin for a character that's hard to input into the shell normally. 
-  \\ will be treated as a backslash.

## References
No references used.

