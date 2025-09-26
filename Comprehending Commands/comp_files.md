# THE ROOT
In this challenge I have to read the flag after comparing two files.

## My solve
**Flag:** `pwn.college{UxCJR7Ubk9cxyEVrF2uUTsgoNbi.01MwMDOxwiN4EzNzEzW}`

It was mentioned in the problem statement that two files '/challenge/decoys_only.txt' and '/challenge/decoys_and_real.txt' are given where '/challenge/decoys_only.txt' contains 100 fake flags and '/challenge/decoys_and_real.txt' contains all 100 fake flags plus the one real flag. So I used the 'diff' command with both the file paths as arguments and it showed the extra real flag as a difference between the two files.
```bash
hacker@commands~comparing-files:~$ diff /challenge/decoys_only.txt /challenge/decoys_and_real.txt
68a69
> pwn.college{UxCJR7Ubk9cxyEVrF2uUTsgoNbi.01MwMDOxwiN4EzNzEzW}
```

## What I learned
Through this challenge I learnt that 'diff' commmand compares two files line by line and shows exactly what's different between them. '<' refers to first file. '>' refers to second file. 'a' means that a line has been added. 'c' means that a line has been changed.
## References 
No references used.
