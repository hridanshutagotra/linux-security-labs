## Level 28
There is a git repository at ssh://bandit28-git@bandit.labs.overthewire.org/home/bandit28-git/repo via the port 2220. The password for the user bandit28-git is the same as for the user bandit28. Clone the repo and find the password

## Requirements
- git
- git log : shows us the commit log
- git show <commit> : shows the content of a commit

## Solution
Similar to the last level, make a directory and clone the provided github repository and checking out the README file
```bash
$ mkdir repo
$ cd repo
$ git clone ssh://bandit28-git@bandit.labs.overthewire.org:2220/home/bandit28-git/repo
$ cd repo
$ cat README.md
```
Inside the readme file, it provides you the username but the password has been redacted. Now we use the `git log` command to check the repository's history for the previous commits, to see if a past version of the README file contained the password.
```bash
$ git log
```
The `git log` command shows that the README file contains 3 commits in its history. One of them is titled "fix info leak", which sounds like something we're looking for. Since that sounds promising, we check it using the show command
```bash
$ git show <the commit number to check>
```
And it should show you the old readme file with the password for bandit29
