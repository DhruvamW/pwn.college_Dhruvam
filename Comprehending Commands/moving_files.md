# MOVING FILES
In this challenge I have to move a file in from a particular directory to another directory to get the flag.

## My solve
**Flag:** `pwn.college{4BjyWMz72IMJnODxQV9qhqtehQF.0VOxEzNxwiN4EzNzEzW}`

It was mentioned in the problem statement that I have to move the '/flag' file to '/tmp' directory under the file name 'hack-the-world'. I used the 'mv' command to move the file and then executed '/challenge/check' to get my flag.
```bash
hacker@commands~moving-files:~$ mv /flag /tmp/hack-the-planet
Correct! Performing 'mv /flag /tmp/hack-the-planet'.
hacker@commands~moving-files:~$ /challenge/check
Congrats! You successfully moved the flag to /tmp/hack-the-planet! Here it is:
pwn.college{4BjyWMz72IMJnODxQV9qhqtehQF.0VOxEzNxwiN4EzNzEzW}
```

## What I learned
Through this challenge I learnt that 'mv' command is used to move a file to a new directory under a new file name.

## References 
No references used.

