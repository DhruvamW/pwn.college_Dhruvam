# TRANSLATING CHARACTERS
In this challenge I have to swap the case of the given flag.

## My solve
**Flag:** `pwn.college{MgFfAtg6S98_uydEAdaNnRSb_uk.01MxEzNxwiN4EzNzEzW}`

It was mentioned in the problem statement that /challenge/run will print the flag but will swap the casing of all characters. I have to swap the case to get the correct flag.
```bash
hacker@data~translating-characters:~$ /challenge/run | tr abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz
yOUR CASE-SWAPPED FLAG:
pwn.college{MgFfAtg6S98_uydEAdaNnRSb_uk.01MxEzNxwiN4EzNzEzW}
```

## What I learned
Through this challenge I learnt that:
- tr, which translates characters it receives over standard input and prints them to standard output.
- Its most basic usage: tr translates the character provided in its first argument to the character provided in its second argument.

## References
No references used.

