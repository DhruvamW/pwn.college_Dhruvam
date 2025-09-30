# SPLIT PIPING STDERR AND STDOUT
In this challenge I have to redirect stdout to one program and stderr to another.

## My solve
**Flag:** `pwn.college{MvU96Rx_9Ljnlw8PZ0oAKlNvBdu.QXxQDM2wiN4EzNzEzW}`

It was mentioned in the problem statement that /challenge/hack: this produces data on stdout and stderr; /challenge/the: redirect hack's stderr to this program; /challenge/planet: redirect hack's stdout to this program. To redirect stdout I simply used > and to redirect stderr I used 2> and created named pipes for both the files.
```bash
hacker@piping~split-piping-stderr-and-stdout:~$ /challenge/hack > >( /challenge/planet ) 2> >( /challenge/the )
Congratulations, you have learned a redirection technique that even experts 
struggle with! Here is your flag:
pwn.college{MvU96Rx_9Ljnlw8PZ0oAKlNvBdu.QXxQDM2wiN4EzNzEzW}
```

## What I learned
Through this challenge I learnt that we can redirect stdout to one program and stderr to another by using named pipes and > and file descriptors.

## References
No references used.

