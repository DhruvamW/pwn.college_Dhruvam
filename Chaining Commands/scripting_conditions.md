# SCRIPTING WITH CONDITIONS
In this challenge I have to create a script which tests a condition.

## My solve
**Flag:** `pwn.college{4PWbv86lFkWTEoRZGU_Cc0yQrNd.0lNzMDOxwiN4EzNzEzW}`

It was mentioned in the problem statement that I have to  write a script at /home/hacker/solve.sh that takes one argument and if the argument is "pwn", output "college". For any other input, output nothing.
```bash
hacker@chaining~scripting-with-conditionals:~$ cat > ./solve.sh
if [ "$1" == "pwn" ]
then 
echo "college"
fi
^C
hacker@chaining~scripting-with-conditionals:~$ /challenge/run
Correct! Your script properly handles all the conditions.
Here's your flag:
pwn.college{4PWbv86lFkWTEoRZGU_Cc0yQrNd.0lNzMDOxwiN4EzNzEzW}
```

## What I learned
Through this challenge I learnt that:
- In bash, you can use if statements to make decisions
- you must have spaces after if, after [, and before ]
- if, then, and fi must all be on different lines
- the terminator of the if statement is fi


## References
No references used.

