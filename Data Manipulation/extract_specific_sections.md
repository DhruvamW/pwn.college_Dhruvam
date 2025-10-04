# EXTRACTING SPECIFIC SECTIONS OF TEXT
In this challenge I have to extract flag characters from the text.

## My solve
**Flag:** `pwn.college{USUxZ5xRDb2Z1rsTkY9C4WDonkB.01NxEzNxwiN4EzNzEzW}`

It was mentioned in the problem statement that the /challenge/run program will give me a bunch of lines with random numbers and single characters (characters of the flag) as columns. I have to extract the character of flag from the text. I piped the data from /challenge/run to cut command with -d " " argument and -f 2 argument to extract the flag characters and used  tr -d "\n" to join them together into a single line.
```bash
hacker@data~translating-characters:~$ /challenge/run | cut -d " " -f 2 | tr -d "\n"
pwn.college{USUxZ5xRDb2Z1rsTkY9C4WDonkB.01NxEzNxwiN4EzNzEzW}
```

## What I learned
Through this challenge I learnt that:
- the cut command helps us to grab specific columns of data.
- -d argument specifies the column delimiter (how columns are separated).
- -f argument specifies the field number (which column to extract).
- 
## References
No references used.

