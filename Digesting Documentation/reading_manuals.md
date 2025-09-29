# READING MANUALS
In this challenge I have to run a command with an argument as given in the manual of the command.

## My solve
**Flag:** `pwn.college{ghEX3CMH1JaxqHymnUF3wUrzASB.QX0EDO0wiN4EzNzEzW}`

It was mentioned in the problem statement that I have to read the manual of the command '/challenge/challenge' by using the 'man' command and 'challenge' as the argument. After reading the manual I got to know that I have to use the argument '--ghaxqy 313' along with '/challenge/challenge' command to get the flag.
```bash
hacker@man~reading-manuals:~$ man challenge
hacker@man~reading-manuals:~$ /challenge/challenge --ghaxqy 313
Correct usage! Your flag: pwn.college{ghEX3CMH1JaxqHymnUF3wUrzASB.QX0EDO0wiN4EzNzEzW}
```

## What I learned
Through this challenge I learnt man is short for manual, and will display (if available) the manual of the command I pass as an argument. I can scroll around the manpage with arrow keys and PgUp/PgDn. When done reading the manpage, I can hit q to quit. Manpages are stored in a centralized database. This database lives in the /usr/share/man directory, but you never need to interact with it directly: you just query it using the man command. The arguments to the man command aren't file paths, but just the names of the entries themselves.

## References 
No references used.

