# CRACKING PASSWORDS
In this challenge I have to become zardus and get the flag.

## My solve
**Flag:** `pwn.college{oog5NyhlGvhKjANSESs_VbJCyCT.QX3UDN1wiN4EzNzEzW}`

It was mentioned in the problem statement that I have to crack the password of zardus and then su to zardus to invoke /challenge/run to get the flag. I first catted /challenge/shadow-leak which gave me a leak of /etc/shadow. There I saw the hashed password of zardus. Then I used John the Ripper to  find the real value of password which was aadvark. Then I used su to enter the password and became zardus.
```bash
hacker@users~cracking-passwords:~$ cat /challenge/shadow-leak
root:*:20182:0:99999:7:::
daemon:*:20182:0:99999:7:::
bin:*:20182:0:99999:7:::
sys:*:20182:0:99999:7:::
sync:*:20182:0:99999:7:::
games:*:20182:0:99999:7:::
man:*:20182:0:99999:7:::
lp:*:20182:0:99999:7:::
mail:*:20182:0:99999:7:::
news:*:20182:0:99999:7:::
uucp:*:20182:0:99999:7:::
proxy:*:20182:0:99999:7:::
www-data:*:20182:0:99999:7:::
backup:*:20182:0:99999:7:::
list:*:20182:0:99999:7:::
irc:*:20182:0:99999:7:::
gnats:*:20182:0:99999:7:::
nobody:*:20182:0:99999:7:::
_apt:*:20182:0:99999:7:::
systemd-timesync:*:20357:0:99999:7:::
systemd-network:*:20357:0:99999:7:::
systemd-resolve:*:20357:0:99999:7:::
mysql:!:20357:0:99999:7:::
messagebus:*:20357:0:99999:7:::
sshd:*:20357:0:99999:7:::
hacker::20357:0:99999:7:::
zardus:$6$qzYLilKuqXunAgAQ$WkMpAtGvBjRUq/ov2rcviA8A6bUbRf/maJj3znqZRJZS1Pe6Ulilbp38iC0cdaapLb8zQzicZ0hmepS4igioT.:20370:0:99999:7:::
hacker@users~cracking-passwords:~$ john /challenge/shadow-leak
Loaded 1 password hash (crypt, generic crypt(3) [?/64])
Press 'q' or Ctrl-C to abort, almost any other key for status
0g 0:00:00:16 1% 2/3 0g/s 316.9p/s 316.9c/s 316.9C/s katrina..karla
aardvark         (zardus)
1g 0:00:00:18 100% 2/3 0.05321g/s 309.8p/s 309.8c/s 309.8C/s Johnson..buzz
Use the "--show" option to display all of the cracked passwords reliably
Session completed
hacker@users~cracking-passwords:~$ su zardus
Password: 
zardus@users~cracking-passwords:/home/hacker$ /challenge/run
Congratulations, you have become Zardus! Here is your flag:
pwn.college{oog5NyhlGvhKjANSESs_VbJCyCT.QX3UDN1wiN4EzNzEzW}
 
```

## What I learned
Through this challenge I learnt that:
-  /etc/passwd is a globally-readable file, this is not good for passwords, these were moved to /etc/shadow.
- Separated by :s, the first field of each line is the username and the second is the password.
- A value of * or ! functionally means that password login for the account is disabled, a blank field means that there is no password
- A long password is the result of one-way-encrypting (hashing)
- When you input a password into su, it one-way-encrypts (hashes) it and compares the result against the stored value. If the result matches, su grants you access to the user.
- The cracking can be done via the famous John the Ripper.
- John the Ripper is a free password cracking software tool.

## References
No references used.

