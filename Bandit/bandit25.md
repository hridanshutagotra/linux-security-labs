## Level 25 - 26
Logging in to bandit26 from bandit25 should be fairly easy… The shell for user bandit26 is not /bin/bash, but something else. Find out what it is, how it works and how to break out of it.

## Requirements
- more
- vim 

## Theory
- In this level, when you log into bandit25, we will see the sshkey for bandit26, all we neneed to do is to copy it to our local system using scp. Now, till here it was pretty straightforward, the problem now is as the description says, the shell for bandit26 is changed and it has a script running to logout as soon as we log in but it runs the `more` command before doing so. 
- We need to take advantage of that by making our terminal window smaller, changing its size. Make your terminal window smaller by changing its size which will make the more command go into command/interactive mode, at which point, we have to enter the `vim` terminal editor by pressing `v` on our keyboard. 
- Now once inside vim, there are a couple of things we can do. We start by typing the following command to change the shell back to bash: `:set shell=/bin/bash` and then use `:shell`. 
- Finally we have a shell and can get the password for the user

The solution for this level is more for teaching you how to think outside the box to get the password

## Solution
After managing to get into a shell using the above instrucitions, use the provided bandit27-do file to get the password for the next level
```bash
$ ./bandit27-do cat /etc/bandit_pass/bandit27

