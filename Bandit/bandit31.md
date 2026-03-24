## Level 31
There is a git repository at ssh://bandit31-git@bandit.labs.overthewire.org/home/bandit31-git/repo via the port 2220. The password for the user bandit31-git is the same as for the user bandit31. Clone the repo and find the password

## Requirements
- git
- git add
- git commit -m
- git push

## Solution
Similar to the last level, make a directory and clone the provided github repository and checking out the README file
```bash
$ mkdir repo
$ cd repo
$ git clone ssh://bandit31-git@bandit.labs.overthewire.org:2220/home/bandit31-git/repo
$ cd repo
$ cat README.md
```
The ‘README’ states that we have to push a file to the repository. So first, we create the file:
```bash
$ echo 'May I come in?' > key.txt
```
Now we use `git add` to add the file, then commit and push to the master branch to get the password
```bash
$ git add -f key.txt
$ git commit -a
$ git push -u origin master
