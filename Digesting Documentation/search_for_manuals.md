# SEARCHING FOR MANUALS
In this challenge I have to run a command with an argument as given in the manual of the command. But this time the name of the manual of the command is randomized which I have to find too using the manpage of man.

## My solve
**Flag:** `pwn.college{wE4XIC5e5WkTgUmDM8VsSujdwFo.QX1EDO0wiN4EzNzEzW}`

It was mentioned in the problem statement that I have to read the manpage of man to find the randomized name of manpage of /challenge/challenge. I opened the manpage of man using man man. Then I found that -k argument which takes name of the argument as an argument. After running man -k challenge I got to know the randomized name. Then I read the man of /challenge/challenge from where I got to know the argument I had to use along with /challenge/challenge to get the flag.
```bash
hacker@man~searching-for-manuals:~$ man man
hacker@man~searching-for-manuals:~$ man -k challenge
vrrzdtcvsx (1)       - print the flag!
hacker@man~searching-for-manuals:~$ man vrrzdtcvsx
hacker@man~searching-for-manuals:~$ /challenge/challenge  --vrrzdt 763
Correct usage! Your flag: pwn.college{AvrO7GGrOSzdtc6D3vZs2NxLRmp.QX2EDO0wiN4EzNzEzW}
```

## What I learned
Through this challenge I learnt that you can search for manpages using the man command with -k argument.

## References 
No references used.

