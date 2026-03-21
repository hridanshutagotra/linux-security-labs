## Level 18
The password for the next level is stored in a file readme in the homedirectory. Unfortunately, someone has modified .bashrc to log you out when you log in with SSH.

## Requirements
- ssh or scp

## Theory
So this was a really interesting level. It basically involves a .bashrc file that is modified to log out when a user tries loggin in with ssh.
So what we can do here is either we just give it a command along with the ssh command, like cat or ls to check the contents on the port, or a more interesting way is by connecting via a pseudo terminal. I'll provide 2 solutions for this covering both methods.

## Solution 1
```bash
# We can provide the cat command to ssh to tell it what to do when it logs in
$ ssh bandit18@bandit.labs.overthewire.org -p 2220 cat readme
```

## Solution 2
```bash
# Alternatively, use can use -t /bin/sh with the ssh command which allows a 'pseudo terminal' to run on the target machine
$ ssh bandit18@bandit.labs.overthewire.org -p 2220 -t /bin/sh
