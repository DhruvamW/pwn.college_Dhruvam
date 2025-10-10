# MULTIPLE CONDITIONS
In this challenge I have to create a script which tests multiple conditions.

## My solve
**Flag:** `pwn.college{knwCDNDU1AJcgcxxJBb09vps4wC.0FOzMDOxwiN4EzNzEzW}`

It was mentioned in the problem statement that I have to  write a script at /home/hacker/solve.sh that takes one argument and if the argument is "pwn", output "college". If the argument is "hack", output "the planet". If the argument is "learn", output "linux". For any other input, output nothing.
```bash
hacker@chaining~scripting-with-multiple-conditions:~$ touch ./solve.sh
hacker@chaining~scripting-with-multiple-conditions:~$ cat > ./solve.sh
if [ "$1" == "hack" ]
then
echo "the planet"
elif [ "$1" == "pwn" ]
then
echo "college"
elif [ "$1" == "learn" ]
then
echo "linux"
else
echo "unknown"
fi
^C
hacker@chaining~scripting-with-multiple-conditions:~$ /challenge/run
Correct! Your script properly handles all the conditions with elif.
Here's your flag:
pwn.college{knwCDNDU1AJcgcxxJBb09vps4wC.0FOzMDOxwiN4EzNzEzW}
```

## What I learned
Through this challenge I learnt that:
- You can use elif (short for else if) to check multiple conditions.


## References
No references used.

