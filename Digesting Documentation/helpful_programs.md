# HELPFUL PROGRAMS
In this challenge I have to read the documentation of a command using --help and figure out how to get the flag.

## My solve
**Flag:** `pwn.college{wv0CFYCSb0DRwR-GfOIlYNHBqtT.QX3IDO0wiN4EzNzEzW}`

It was mentioned in the problem statement that I have to read the documentation of /challenge/challenge using the --help argument. On readinf the documentation I got to know that I have to get a secret value from -p command which I have to then use with -g argument to get the flag.
```bash
hacker@man~helpful-programs:~$ /challenge/challenge --help
usage: a challenge to make you ask for help [-h] [--fortune] [-v] [-g GIVE_THE_FLAG] [-p]

optional arguments:
  -h, --help            show this help message and exit
  --fortune             read your fortune
  -v, --version         get the version number
  -g GIVE_THE_FLAG, --give-the-flag GIVE_THE_FLAG
                        get the flag, if given the correct value
  -p, --print-value     print the value that will cause the -g option to give you the flag
hacker@man~helpful-programs:~$ /challenge/challenge -p
The secret value is: 3
hacker@man~helpful-programs:~$ /challenge/challenge -g 3
Correct usage! Your flag: pwn.college{wv0CFYCSb0DRwR-GfOIlYNHBqtT.QX3IDO0wiN4EzNzEzW}
```

## What I learned
Through this challenge I learnt that you can read the documentation of a command generally by using the --help or -h or -? argument.

## References 
No references used.

