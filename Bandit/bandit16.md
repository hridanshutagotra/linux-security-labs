## Level 16
The credentials for the next level can be retrieved by submitting the password of the current level to a port on localhost in the range 31000 to 32000. First find out which of these ports have a server listening on them. Then find out which of those speak SSL and which don’t. There is only 1 server that will give the next credentials, the others will simply send back to you whatever you send to it.

## Requirements
- Chmod
- nmap
- ncat

## Solution
```bash
# Scan the ports between 31000 to 32000 to check for open ports
$ nmap -sV localhost -p 31000-32000

# Use ncat to connect to the open ssl port that looks promising
$ ncat --ssl localhost 31790

# After entering the right password, the port will give you a private key, that you need to copy and save to your local system.
## after saving it to your local machine, use chmod to change permissions only for the user

$ chmod 700 sshkey.private
