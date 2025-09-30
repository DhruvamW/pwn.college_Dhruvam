# MULTIPLE OPTIONS FOR TAB COMPLETION
In this challenge I have to tab-complete my command to get the flag.

## My solve
**Flag:** `pwn.college{kCLmrAhSvZwbWVAYW0LrSUdX9pf.0lN0EzNxwiN4EzNzEzW}`

It was mentioned in the problem statement that I have to cat the files starting with /challenge/pwncollege using tab-completion to get the flag. 
```bash
hacker@globbing~multiple-options-for-tab-completion:~$ cat /challenge/files/pwncollege-flag
pwn.college{kCLmrAhSvZwbWVAYW0LrSUdX9pf.0lN0EzNxwiN4EzNzEzW}
```

## What I learned
Through this challenge I learnt that by default bash will auto-expand until the first point when there are multiple options. When we hit tab a second time, it'll print out those options. Other shells and configurations, instead, will cycle through the options.

## References
No references used.

