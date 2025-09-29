# MATCHING PATHS WITH []
In this challenge I have to expand entire paths with globbed arguments.

## My solve
**Flag:** `pwn.college{4yclb1tg6VfAQAWbCgoxyuxTQNN.QX0IDO0wiN4EzNzEzW}`

It was mentioned in the problem statement that starting from my home directory, I have to run /challenge/run with a single argument using bracket-globs into the absolute paths to the file_b, file_a, file_s, and file_h files. The files were placed in  /challenge/files directory.
```bash
hacker@globbing~matching-paths-with-:~$ /challenge/run /challenge/files/file_[absh]
You got it! Here is your flag!
pwn.college{4yclb1tg6VfAQAWbCgoxyuxTQNN.QX0IDO0wiN4EzNzEzW}
```

## What I learned
Through this challenge I learnt that globbing happens on a path basis, so we can expand entire paths with our globbed arguments.

## References
No references used.

