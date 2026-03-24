## Level 30
There is a git repository at ssh://bandit30-git@bandit.labs.overthewire.org/home/bandit30-git/repo via the port 2220. The password for the user bandit30-git is the same as for the user bandit30 Clone the repo and find the password

## Requirements
- git
- git show
- git tag : to check tags

## Solution
Similar to the last level, make a directory and clone the provided github repository and checking out the README file
```bash
$ mkdir repo
$ cd repo
$ git clone ssh://bandit30-git@bandit.labs.overthewire.org:2220/home/bandit30-git/repo
$ cd repo
$ cat README.md
```
It does not give us any information. Checking the git tag, we find a point in history called 'secret', which looks promising.

```bash
$ git show secret
