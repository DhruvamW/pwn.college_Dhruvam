# FUN WITH GROUPS NAMES
In this challenge I have to change group of a file to read the flag.

## My solve
**Flag:** `pwn.college{gNvqImUS2eBOwIlJFYqkNIs327I.QXycjM1wiN4EzNzEzW}`

It was mentioned in the problem statement that I have to change the group ownership of the flag file, and read the flag. I first checked what gorup I am a part of using the id command. Then I used chgrp to change the group to grp12024 which I was a part of. Then I read the flag.
```bash
hacker@permissions~fun-with-groups-names:~$ id
uid=1000(hacker) gid=1000(grp12024) groups=1000(grp12024)
hacker@permissions~fun-with-groups-names:~$ chgrp grp12024 /flag
hacker@permissions~fun-with-groups-names:~$ cat /flag
pwn.college{gNvqImUS2eBOwIlJFYqkNIs327I.QXycjM1wiN4EzNzEzW}
```

## What I learned
Through this challenge I learnt that:
-  we can use id command to check what all groups we are a part of in the system.

## References
No references used.

