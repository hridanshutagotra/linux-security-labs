## Level 15
The password for the next level can be retrieved by submitting the password of the current level to port 30001 on localhost using SSL/TLS encryption.

## Requirements
- nc
- ncat 

## Solution
```bash
# we make use of ncat, which is a modern iteration of the nc command, and provides enhancements like being able to connect to ssl/tls encryption
$ ncat --ssl localhost 30001
