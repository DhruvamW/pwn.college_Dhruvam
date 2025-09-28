# LINKING FILES
In this challenge I have to link a file to another file with the flag in it.

## My solve
**Flag:** `pwn.college{YLMv4Q7nuiQfL1i-lC81OKe6Dxc.QX5ETN1wiN4EzNzEzW}`

It was mentioned in the problem statement that I have to trick the'/challenge/catflag' to read '/flag' instead of reading the
  '/home/hacker/not-the-flag' that it originally reads. To link '/flag' with '/home/hacker/not-the-flag' I first deleted '/home/hacker/not-the-flag' using the 'rm' command. Then I created a symbolic link using 'ln -s' of '/home/hacker/not-the-flag' to '/flag' and finally invoked the '/challenge/catflag' to get the flag. 
```bash
hacker@commands~linking-files:~$ rm ~/not-the-flag
hacker@commands~linking-files:~$ ln -s /flag ~/not-the-flag
hacker@commands~linking-files:~$ /challenge/catflag
About to read out the /home/hacker/not-the-flag file!
pwn.college{YLMv4Q7nuiQfL1i-lC81OKe6Dxc.QX5ETN1wiN4EzNzEzW}
```

## What I learned
Through this challenge I learnt that 'ln' command links one file to another. There are two types of linking: hard links and soft/symbolic links. Hard Linking is basically just creating another file with the same data as the orignal file. There is virtually no difference in referencing the orginal file or the hard-linked file. Soft/Symbolic Linking is when a file just contains the link to the orignal file but no data. To soft link a file the following command is used: ln -s (-s stands for symbolic) <orignal_file_path>  <link_to_path>

## References 
https://www.youtube.com/watch?v=m55AtwjBXpE&list=PL-ymxv0nOtqqRAz1x90vxNbhmSkeYxHVC

