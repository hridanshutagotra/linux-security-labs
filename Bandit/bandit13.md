## Level 13
The password for the next level is stored in /etc/bandit_pass/bandit14 and can only be read by user bandit14. For this level, you don’t get the next password, but you get a private SSH key that can be used to log into the next level.

## Requirements
- ssh
- scp : command to send data from a remote host to local host

## Solution
```bash
## you have to enter this command in your local machine, so it'll fetch the file from the remote host
$ scp -P 2220 bandit13@bandit.labs.overthewire.org:sshkey.private .

## the previous command will download the ssh private key to your machine, then login to the next level using that
$ ssh -i sshkey.private bandit14@bandit.labs.overthewire.org -p 2220
