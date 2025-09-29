# MATCHING WITH ?
In this challenge I have to change my directory using globbing.

## My solve
**Flag:** `pwn.college{MGFLdTFhHCR21f84xyxrmIjwNla.QXyIDO0wiN4EzNzEzW}`

It was mentioned in the problem statement that I have to change my directory to /challenge using cd command and using ? in place of c and l in challenge in my argument. I used globbing technique to pass the address of /challenge as the argument to cd command.
```bash
hacker@globbing~matching-with-:~$ cd /?ha??enge
hacker@globbing~matching-with-:/challenge$ ./run
You ran me with the working directory of /challenge! Here is your flag:
pwn.college{MGFLdTFhHCR21f84xyxrmIjwNla.QXyIDO0wiN4EzNzEzW}
```

## What I learned
Through this challenge I learnt that another glob is ?. When it encounters a ? character in any argument, the shell will treat it as a single-character wildcard. This works like *, but only matches one character.

## References
No references used.

