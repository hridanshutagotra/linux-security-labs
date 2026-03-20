## Level 14
The password for the next level can be retrieved by submitting the password of the current level to port 30000 on localhost.

## Requirements
- telnet

## Solution
```bash
# Firstly, the password for the current level is located in /etc/bandit_pass/bandit14
$ cat /etc/bandit_pass/bandit14

# Now after retrieving the password, we use telnet to connect to it and submit the password
$ telnet localhost 30000
<Insert Password>
