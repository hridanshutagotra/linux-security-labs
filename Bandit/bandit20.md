## Level 20
There is a setuid binary in the homedirectory that does the following: it makes a connection to localhost on the port you specify as a commandline argument. It then reads a line of text from the connection and compares it to the password in the previous level (bandit20). If the password is correct, it will transmit the password for the next level (bandit21).

## Requirements
- setuid
- nc

## Theory
So basically, in this level you need to setup a listener server using the `-l` flag which means listening. So essentially we're gonna make a "onetime server" that sends one message and then disconnects, and we can use the pipe `|` operator and echo to input a message.

## Solution
```bash
# this is going to open the listener server and give the password to any server that listens to the connection
$ echo -n "enter_current_level_password" | nc -l -p 1234 &

# now execute the given setuid file and connect it to the server port we set up, ie, 1234
$ ./suconnect 1234

