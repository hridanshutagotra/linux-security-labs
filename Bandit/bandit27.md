## Level 27
There is a git repository at ssh://bandit27-git@bandit.labs.overthewire.org/home/bandit27-git/repo via the port 2220. The password for the user bandit27-git is the same as for the user bandit27.
Clone the repo and find the password for the next level
## Requirements
- git

## Solution
First we create a directory for our project, then we clone it
```bash
$ mkdir repo
$ cd repo
$ git clone ssh://bandit27-git@bandit.labs.overthewire.org:2220/home/bandit27-git/
```
There will be a password prompt. Type in the password for this level and the repo will be cloned. Cd into the repo and read the README file for the password
```bash
$ cd repo
$ cat REALME
