## Level 29
There is a git repository at ssh://bandit29-git@bandit.labs.overthewire.org/home/bandit29-git/repo via the port 2220. The password for the user bandit29-git is the same as for the user bandit29. Clone the repo and find the password

## Requirements
- git
- git branch -a : lists the branches
- git checkout <branch_name>/git switch <branch_name> : switch branches

## Solution
Similar to the last level, make a directory and clone the provided github repository and checking out the README file
```bash
$ mkdir repo
$ cd repo
$ git clone ssh://bandit29-git@bandit.labs.overthewire.org:2220/home/bandit29-git/repo
$ cd repo
$ cat README.md
```
The readme file shows us the sentence "No passwords in production!" which sounds like there might be other branches that might have the password. So we check the other branches using `git branch -a`
```bash
$ git branch -a
```
We see a list of branches including a dev branch. So let's switch to that branch and check its contents
```bash
$ git checkout dev
$ cat README.md
```
After reading the readme file in the dev brach, we see that the password was indeed in the dev branch.
