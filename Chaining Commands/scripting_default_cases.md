# SCRIPTING WITH DEFAULT CASES
In this challenge I have to create a script which tests a condition.

## My solve
**Flag:** `pwn.college{8tPaEbKYjs5YBv5dj4y4tcc3Amz.01NzMDOxwiN4EzNzEzW}`

It was mentioned in the problem statement that I have to  write a script at /home/hacker/solve.sh that takes one argument and if the argument is "pwn", output "college". For any other input, output nope.
```bash
hacker@chaining~scripting-with-default-cases:~$ cat > ./solve.sh
if [ "$1" == "pwn" ]
then
echo "college"
else
echo "nope"
fi
^C
hacker@chaining~scripting-with-default-cases:~$ /challenge/run
Correct! Your script properly handles the if/else conditions.
Here's your flag:
pwn.college{8tPaEbKYjs5YBv5dj4y4tcc3Amz.01NzMDOxwiN4EzNzEzW}
```

## What I learned
Through this challenge I learnt that:
- The else clause executes when the if condition is false


## References
No references used.

