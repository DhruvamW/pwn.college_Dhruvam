# SEARCHING MANUALS
In this challenge I have to run a command with an argument as given in the manual of the command.

## My solve
**Flag:** `pwn.college{wE4XIC5e5WkTgUmDM8VsSujdwFo.QX1EDO0wiN4EzNzEzW}`

It was mentioned in the problem statement that I have to read the manual of the command '/challenge/challenge' by using the 'man' command and 'challenge' as the argument. I searched the manual for the argument to give the flag using '/flag' and navigated using 'n'. After finding the right argument I got to know that I have to use the argument '--puiyje' along with '/challenge/challenge' command to get the flag.
```bash
hacker@man~searching-manuals:~$ man challenge
hacker@man~searching-manuals:~$ /challenge/challenge --puiyje
Initializing...
Correct usage! Your flag: pwn.college{wE4XIC5e5WkTgUmDM8VsSujdwFo.QX1EDO0wiN4EzNzEzW}
```

## What I learned
Through this challenge I learnt that you can scroll man pages with the arrow keys (and PgUp/PgDn) and search with /. After searching, you can hit 'n' to go to the next result and 'N' to go to the previous result. Instead of /, you can use ? to search backwards.

## References 
No references used.

