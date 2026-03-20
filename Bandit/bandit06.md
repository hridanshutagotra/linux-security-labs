## Level 6
The password for the next level is stored somewhere on the server and has all of the following properties:

    owned by user bandit7
    owned by group bandit6
    33 bytes in size

## Requirements
- find command

## Solution
```bash
# We can use the find command with certain flags to find the password 
$ find / -size 33c -user bandit7 -group bandit6 2>/dev/null

# 2>/dev/null sends all the error messages to dev/null which is known as the black hole in unix systems

# Then use the cat command to read the password file that find command found for us
$ cat /var/lib/dpkg/info/bandit7.password
