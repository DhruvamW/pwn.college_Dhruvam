# FILTERING WITH GREP -V
In this challenge I have to filter out all the lines containing "DECOY" and reveal the real flag.

## My solve
**Flag:** `pwn.college{UQxvZ6d8Y_oKyWgtAQGxT-ktMrK.0FOxEzNxwiN4EzNzEzW}`

It was mentioned in the problem statement that /challenge/run will output the flag to stdout, but it will also output over 1000 decoy flags (containing the word DECOY somewhere in the flag) mixed in with the real flag. So I redirected the output of /challenge/run to grep command and used -v DECOY argument to filter out all the DECOY flags.
```bash
hacker@piping~filtering-with-grep-v:~$ /challenge/run | grep -v DECOY
pwn.college{UQxvZ6d8Y_oKyWgtAQGxT-ktMrK.0FOxEzNxwiN4EzNzEzW}
```

## What I learned
Through this challenge I learnt that we can us -v with grep to show lines that do NOT match a pattern.

## References
No references used.

